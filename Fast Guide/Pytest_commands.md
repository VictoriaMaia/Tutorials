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
| --co or --collect-only | Onyly collect the tests, don't execute them                          |


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


-------------------------------------
### Refence: 

[Doc pytest cache](https://docs.pytest.org/en/latest/how-to/cache.html)

[Complete Python Pytest Framework Course](https://www.udemy.com/course/python-automation-pytest/?couponCode=ST5MT020225)
