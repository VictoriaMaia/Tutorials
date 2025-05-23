#TODO Add some usable examples related a real tests
#TODO And examples following differents structures (e.g. Test scenarios inside a class or a file)
#TODO Add pytest.ini example
#TODO Add sections to be more organized
#TODO Add inital description

- [Some commands and tips to run your tests in pytest framework.](#some-commands-and-tips-to-run-your-tests-in-pytest-framework)
  - [Pytest configurations](#pytest-configurations)
  - [Refence:](#refence)


# Some commands and tips to run your tests in pytest framework.

The simple command that run all tests:

`pytest`

Or using the specific file or specific folder that you want execute:

`pytest <path>/<test_file.py>`
`pytest <folder_name>`

Exemplo: 
`pytest My_tests/test_login.py`
`pytest My_tests`

If your test is organized with test class like this:

```
    class TestClass():
        def test_scenario_1(self)
        def test_scenario_2(self)
```

and your want test a specific scenario run:

`pytest My_tests/tests.py::TestClass::test_scenario_name`


In pycache have informations about the failed tests, so you can execute only the failures using the command:

`pytest --last-failed `


These are the flags that you can use and what each one do:

|Flag                    | Description                                                          |
|-----                   | -----------                                                          |
| -v                     | Show more details about the test execution                           |
| -s                     | Show the prints of the tests                                         |
| --lf or --last-failed  | Only re-run the failures                                             |
| --ff or --failed-first | Run the failures first and then the rest of the tests                |
| -timeout <value>       | Set a timeout in seconds                                             |
| -m <label>             | Run a group of tests. You can use logical operators                  |
| -k <test_name>         | Filter for modules and test functions. You can use logical operators |
| --tb=no                | You modify the traceback printing, no traceback at all               |
| -x                     | Stop after first failure                                             |
| --maxfail              | Stop after specified 'maxfail'                                       |
| -q                     | Quiet, not verbose                                                   |
| --co or --collect-only | Only collect the tests, don't execute them                           |
| --setup-show           | Show the which fixture the test use. **M** is a fixture used in the module and **F** is a fixture used in a function                                                           |


It's not a command, but it's very usefull to know:

If you want skip a test add "@pytest.mark.skip()" mark before the test. If you want describe the reason of the skip, just fill the reason parameter.

```
import pytest

@pytest.mark.skip(reason="Skip explanation")
def test_to_skip():
    ...
```

You can skip using a conditional "@pytest.mark.skipif(conditional, reason="Skip explanation")":

```
import pytest

@pytest.mark.skipif(sys.version_info > (3,6), reason="Don't work in this python version")
def test_to_skip():
    ...
```

If you want mark the test creating a group of tests, you'll use the markers too:

```
import pytest

@pytest.mark.group_label
def test_with_group():
    ...
```

To avoid warning about your custom markers just added it in pytest.ini:
> remembering to add this file in yout root folder of the project

```
[pytest]
markers=
    label_1: Description
    label_2: Description
```

To add all test scenarios in a file to a same group, you need create a mark in top of file like this:

```
import pytest
pytestmark = [pytest.mark.label]


def test_1():
    ...

def test_2():
    ...
```

If it have some bug know and not yet fixed or some feature not yet implemented but you have the scenario implemented you add a mark informing that is expected to fail given an reason, like that:

```
import pytest

@pytest.mark.xfail(raises=IndexError, reason="It is a known issue")
def test_with_group():
    ...
```

You want add the expected raises to verify if failing given an know issue.


Some outcomes:
- Passed (.)
- Failed (F)
- Skipped (s)
- XFail (x)
- XPass (X)
- Error (E)


Some tests can receive parameters, and the input parameters can be a list of everything:

```
import pytest

# @pytest.mark.parametrize(<variable>, <values>)

@pytest.mark.parametrize('test_input', [82,78,45])
def test1(test_input):
    ...

@pytest.mark.parametrize("inp, out", [(2,4), (3,27)]):
def test2(inp, out):
    ...


data = [
    ([2,3,4], 'sum', 9),
    ([2,3,4], 'prod', 24)
]

@pytest.mark.parametrize("values, op, result", data):
def test3(values, op, result):
    ...

```

If you need to do some task before or after the tests like connect database, or delete temporary folder, you should use the fixture. You can put fixtures in individual test files or, in conftest.py for making fixtures available in multiple test files.

NOTE: You can use the setup_method/teardown_method to do the same action, but the fixture is more flexible and can do more configurations.

```
# This example the test receive an list that was created before the test

import pytest

@pytest.fixture()
def setup_list():
    city = ['C1', 'C2', C3']
    return city # this return is optional. The test can access the city variable

def test(setup_list):
    ...
```

You can use markers to use the fixture, like this:

```
import pytest

@pytest.fixture()
def setup():
    # using the marker you don't need return value. The test function cannot use the return values

@pytest.mark.usefixtures("setup")
def test():
    ...
```

If you need a teardown, you can use the yield tool. The yield stop the function returning the variable and the code will execute the test. After the test finish the yield returns to finish your execution.

```
import pytest

weekdays1 = ['mon', 'tue', 'wed']

@pytest.fixture()
def setup():
    wk1 = weekdays1.copy()
    wk1.append('thur')
    yield wki 
    print("\n After yield")
    wk1.pop()


def test(setup):
    assert setup == ['mon', 'tue', 'wed', 'thur']
```

You can use more that one fixtures, just pass them as parameter in your test function.

To organize the test project better, you can create a "conftest.py" file and create the fixtures in this file. The fixtures will be centralized in a directory for all tests to access. 

It should not be imported by test files!
 
You can define some variables in this conf file, using the "pytest_configure". Please check if this function was not deprectead.

```
import pytest

def pytest_configure():
    pytest.weekdays1 = ['mon', 'tue', 'wed']


@pytest.fixture()
def setup():
    wk1 = pytest.weekdays1.copy()
    wk1.append('thur')
    yield wki 
    print("\n After yield")
    wk1.pop()
```

Fixtures have a scope, you can set the fixture to use in all module or just in a function. You just need pass scope as parameter.

Fixtures are created when first requested by a test, and are destroyed based on their scope:

- function (default scope)(is a test): is destroyed at the end of the test
- class (is all tests inside a same class): is destroyed during teardown of the last test in the class
- module (is all tests inside a same file): is destroyed during teardown of the last test in the module
- package (is all tests inside a same folder): is destroyed during teardown of the last test in the package 
- session (is a test session, all tests): is destroyed at the end of the test session 

Remember: Fixtures can be overriden from test module level!


You can access variables and informations in fixtures that they was defined in a test file:

```
import pytest

@pytest.fixture()
def setup(request):
    var = getattr(request.module, "var_name")
    fixture_scope = str(request.scope)
    test_function_that_call_this_fixture = str(request.function.__name__)
    module_that_have_the_test_that_call_this_fixture = str(request.module.__name__)
```

You can use factories as fixture, returning a function in fixture to test can use it:

```
import pytest

@pytest.fixture()
def setup():
    def get_structure(name):
        if name == 'list':
            return [1,2]
        elif name == 'tuple':
            retunr (1,2)
    return get_structure


def teste(setup):
    assert type(setup('list')) == list
```

Parametrizing from fixtures. It was execute the same way of the test using parametrizing, the test will run to all values returned in fixtures. Example:

```
import pytest

@pytest.fixture(params = [(1,2), [1,2]])
# you can use ids to identify the parameters:
# @pytest.fixture(params = [(1,2), [1,2]], ids=['tuple', 'list'])
def setup(request):
    return request.param


def teste(setup):
    assert type(setup) in [tuple, list]
```


You can pass arguments to test, one of the ways to do this is creating functions inside a conftest.py file like this:

```
import pytest
# import os  # **

qa_config = 'qa.prop'
prod_config = 'prod.prop'

def pytest_addoption(parser):
    parser.addoption("--cmdopt", default='QA')


@pytest.fixture()
def CmdOpt(pytestconfig):
    opt = pytestconfig.getoption("cmdopt)
    if opt == 'Prod'
        f = open(prod_config, 'r')
        # f = open(os.path.join(os.path.dirname(__file__),prod_config), 'r') # **
    else:
        f = open(qa_config, 'r')
        # f = open(os.path.join(os.path.dirname(__file__),qa_config), 'r') # **
    
    yield f
```

In a test file:

```
def test(CmdOpt):
    print(CmdOpt.readline())
```

To run:

$ pytest -v root/test_filename.py --cmdopt=Prod -s

If the test that you want run is an internal folder like this:

|- root
|--  specific_test_folder
|---   test_file.py
|---   qa.prop
|---   prod.prop
|--  conftest.py

The command will failed because it not found the files. So to fix this just add the line with ** above

## Pytest configurations

You can set some configurations of pytest. There are several configurations that you can choose and some types of config files, so it more easy you see these documentations: 

- [Configuration file formats](https://docs.pytest.org/en/stable/reference/customize.html)
- [Configuration options](https://docs.pytest.org/en/stable/reference/reference.html#configuration-options)

You can run to see the options:

$ pytest --help


You can define utils file to read necessary data files to tests. Just create an folder to add your data files and in the utils create the functions to read and return the data. In the test you use the python.mark.parametrize passing the parameters that will returned and the function name that was created in utils.


> Explanation: The configparser lib is used to read and write config files in ini format. It is util to save path, passwords, parameters, etc.

Usefull:

-> config_file_that_have_credentials.ini
```
[gmail]
user = email_user
```

-> utils_file_that_read_and_share_informations_of_the_conf_file.py
```
import configparser
from pathlib import Path 

cfgFile = 'config_file_that_have_credentials.ini'
cfgFileDir = 'config'

config = configparser.ConfigParser()
BASE_DIR = Path(_file__).resolve().parent.parent
CONFIG_FILE = BASE_DIR.joinpath(cfgFileDir).joinpath(cfgFile)

config.read(CONFIG_FILE)

def getGmailUser():
    return (config['gmail']['url'])
```

Or using a Class:
```
import configparser
from pathlib import Path 

class ConfigFileParser():
    cfgFile = 'config_file_that_have_credentials.ini'
    cfgFileDir = 'config'
    config = configparser.ConfigParser()

    def __init__(self, cfg=cfgFile):
        self.cfgFile = cfg
        self.BASE_DIR = Path(_file__).resolve().parent.parent
        self.CONFIG_FILE = BASE_DIR.joinpath(cfgFileDir).joinpath(cfgFile)
        self.config.read(CONFIG_FILE)

    def getGmailUser(self):
        return (self.config['gmail']['url'])
```



-------------------------------------
## Refence: 

[Doc pytest cache](https://docs.pytest.org/en/latest/how-to/cache.html)

[Complete Python Pytest Framework Course](https://www.udemy.com/course/python-automation-pytest/?couponCode=ST5MT020225)
