[PT-BR]

Essa explicação é baseada em:

- [CTFL Syllabus v4.0](https://bstqb.online/docs/syllabus_ctfl_4.0br.pdf)
- [Curso Preparatório para Certificação em Testes de Software CTFL (ISQTB) do professor Leonardo Carvalho - UDEMY](https://www.udemy.com/course/preparatorio-ctfl/?couponCode=OF83024E)

# Capítulo 2 Testes ao longo do Ciclo de Vida de Desenvolvimento de Software


- [Capítulo 2 Testes ao longo do Ciclo de Vida de Desenvolvimento de Software](#capítulo-2-testes-ao-longo-do-ciclo-de-vida-de-desenvolvimento-de-software)
  - [2.1 Testes no contexto de um Ciclo de Vida de Desenvolvimento de Software](#21-testes-no-contexto-de-um-ciclo-de-vida-de-desenvolvimento-de-software)
    - [2.1.1 Explicar o impacto do ciclo de vida de desenvolvimento de software escolhido nos testes.](#211-explicar-o-impacto-do-ciclo-de-vida-de-desenvolvimento-de-software-escolhido-nos-testes)
    - [2.1.2 Relembrar as boas práticas de teste que se aplicam a todos os ciclos de vida de desenvolvimento de software.](#212-relembrar-as-boas-práticas-de-teste-que-se-aplicam-a-todos-os-ciclos-de-vida-de-desenvolvimento-de-software)
    - [2.1.3 Relembrar os exemplos de abordagens de desenvolvimento que priorizam o teste](#213-relembrar-os-exemplos-de-abordagens-de-desenvolvimento-que-priorizam-o-teste)
    - [2.1.4 Resumir como o DevOps pode ter um impacto nos testes](#214-resumir-como-o-devops-pode-ter-um-impacto-nos-testes)
    - [2.1.5 Explicar a abordagem shift-lef](#215-explicar-a-abordagem-shift-lef)
    - [2.1.6  Explicar como as retrospectivas podem ser usadas como um mecanismo de melhoria de processos.](#216--explicar-como-as-retrospectivas-podem-ser-usadas-como-um-mecanismo-de-melhoria-de-processos)
  - [2.2 Níveis de Teste e Tipos de Teste](#22-níveis-de-teste-e-tipos-de-teste)


## 2.1 Testes no contexto de um Ciclo de Vida de Desenvolvimento de Software

### 2.1.1 Explicar o impacto do ciclo de vida de desenvolvimento de software escolhido nos testes.

O ciclo de desenvolvimento de software (Software Development Life Cycle SDLC) diz como o projeto vai ser desenvolvido, qual modelo de desenvolvimento o projeto vai seguir, quais serão as atividades e como elas se relacionam de forma cronológica. Essa definição também direciona como os testes vão ser feitos. Então, os testes só podem ser pensados quando se entender como o projeto vai ser desenvolvido.

Cada modelo de desenvolvimento vai ter seu impacto. Mas lembrando que, independente do modelo, é de bom tom que sempre sejam feitos testes o quanto antes.

Existem vários tipos de modelos. Temos modelos de desenvolvimento sequencial (p. ex., modelo em cascata, modelo em V), modelos de desenvolvimento iterativo (p. ex., modelo em espiral, prototipagem) e modelos de desenvolvimento
incremental (p. ex., Processo Unificado), XP, TDD, ATDD, BDD, etc. No syllabus eles citam todos esses, mas nessa seção vamos ver os impactos nos testes apenas do modelo sequencial e o iterativo.

Primeiramente vendo em um contexto geral, o modelo selecionado pode impactar/definir:

- O escopo e cronograma das atividades de teste (p. ex., níveis de teste e tipos de teste);
- O nível de detalhamento da documentação de teste;
- A escolha das técnicas de teste e da abordagem de teste;
- A extensão da automação de testes;
- O papel e responsabilidades de um Testador;

Como assim? Vamos ver na prática olhando pros dois modelos citados anteriormente. 

-> Modelo sequencial. 

Primeiro de tudo, como funciona o modelo sequencial? Ele como o nome diz segue uma sequência e a atividade só inicia quando a atividade anterior termina. As atividades desse modelo são:


![alt text](<images/Screenshot 2024-11-06 200328.png>)

Então as atividades de testes em si vão ser iniciadas apenas quando as três primeiras atividades (Análise, Design e Desenvolvimento) terminarem. Isso já é um impacto, os testadores neste modelo, geralmente, não fazem testes dinâmicos no início do SDLC, porque não vai ter produto desenvolvido, não vai ter código para testar.

Mas não quer dizer que os testadores ficam parados, eles participam de revisões das primeiras atividades. Seja revisão de requisitos, de funcionalidades, de design. Essas revisões são testes e são atividades voltadas a qualidade. São nesses tipos de testes/revisões em que o testador pode ajudar a evitar desentendimentos ou definições dúbias que acabam gerando defeitos no desenvolvimento.

-> Modelo iterativo e incremental

Esse modelo visa desenvolver o projeto em versões pequenas e graduais. Se pensar bem no nome, faz sentido, o projeto vai ser desenvolvido de forma iterativa, com iterações e a cada iteração vai haver um incremento do produto.

Nesse modelo como vamos ter entregas o testador já consegue fazer testes estáticos e dinâmicos em todos os níveis, desde a definição até a implementação. Além de necessitar ter feedbacks rápidos e testes de regressão extensivos para validar que a entrega atual não impactou negativamente a entrega anterior.

-> Modelo ágil

Parecido com o modelo anterior, o modelo ágil vai ter entregas pequenas, mas ele foca na flexibilidade e entrega rápida do projeto. Então ele sempre está preparado para ter mudanças ao longo do desenvolvimento. 

Como nesse modelo se tem a preocupação de ser "ágil", de fazer entregas o quanto antes e que pode haver mudanças a qualquer momento, a documentação de teste deverá ser leve, para caso ocorra mudanças drásticas a atualização dessas informações não se torne uma atividade custosa.

Assim como o modelo anterior, já podemos ter desenvolvimento de código nas primeiras atividades, o que possibilita o uso de testes dinâmicos e nesse modelo a automação é mais que bem vinda. A automação vai ajudar a conseguir testar todas as versões desenvolvidas de forma rápida e que não acumule trabalho de uma versão para outra.

E fica só na automação? Não, os testes manuais que precisam ser feitos vão precisar usar técnicas baseadas na experiência (testes exploratórios, ou testes baseados em erros já conhecidos) para que o testador tenha um rumo bem definido, e que não precise gastar muito tempo.


### 2.1.2 Relembrar as boas práticas de teste que se aplicam a todos os ciclos de vida de desenvolvimento de software.

- Para cada atividade de desenvolvimento há uma atividade de teste correspondente. Para que todo o desenvolvimento esteja sujeito ao controle de qualidade
- Aplicar diferentes níveis de teste. Cada nível teste tem objetivos diferentes o que permite que você teste vários aspectos e evite redundância
- Durante a fase de desenvolvimento, a análise e a modelagem dos testes já podem ser feitas. Como o desenvolvimento já está botando em práticas as definições dos requisitos, os testadores já tem uma noção de como o sistema deve funcionar e com isso já podem ir modelando seus cenários, além de entender como fazer esses testes e começar a preparar o ambiente necessário.
- Os testadores podem se envolver na revisão dos produtos de trabalho assim que os rascunhos estiverem disponíveis para que seja feito a detecção defeitos seguindo a estratégia shift-left*. Avaliar o rascunho pode ajudar nas definições necessárias. Se a revisão começar com as primeiras versões, podem surgir dúvidas e ideias capazes de melhorar ainda mais o documento que está sendo feito.

*estratégia shift-left: Trazer o teste o mais à esquerda dos processos de desenvolvimento. Ou seja, nas etapas mais iniciais do processo.


### 2.1.3 Relembrar os exemplos de abordagens de desenvolvimento que priorizam o teste

Existem abordagens de desenvolvimento baseadas em testes, em que os testes é que vão direcionar como o desenvolvimento será feito. Cada uma dessas abordagens segue o princípio do teste antecipado pois o teste é definido e feito antes do código ser escrito. 

----
- TDD (Test Driven Development ou Desenvolvimento Orientado por Testes)
  
![alt text](<images/Captura de tela 2024-12-04 203714.png>)

  Essa imagem representa bem a ideia do TDD. O TDD também é conhecido como "red, green, refactor" ("vermelho, verde, refatoração").

  1) O teste é escrito antes de tudo. Se não tem sistema para executar o comportamento que foi criado o teste ele logicamente vai falhar. Por isso o vermelho, de falha.
  2) Ai vem o desenvolvimento da feature seguindo o cenário de teste, seguindo o comportamento desejado que vai fazer aquele teste passar. Depois da implementação o teste vai passar. Por isso o verde, de teste passou, o teste teve sucesso. 
  3) Ai em seguida vem a refatoração caso exista alguma atualização necessária no cenário. Ou a feature precisou ter mudanças na sua definição, ou precisou de mais cenários, etc. Nesse ponto terá a atualização necessária dos testes.
  4) E aí o ciclo volta a acontecer. É feito mais cenários, de outras features. O desenvolvedor vai entender o cenário e implementar o comportamento desejado. O teste vai começar a passar e depois será analisado se precisa ou não de atualização no código de teste ou no do produto.

Lembrando que: Esse tipo de abordagem é utilizando testes de componentes ou de unidades automatizadas.

---
- ATDD (Accept Test Driven Development ou Desenvolvimento Orientado por Testes de Aceite)

![alt text](<images/Captura de tela 2024-12-04 210103.png>)

  Segue a mesma ideia do TDD, mas agora seguindo testes de aceite como parte do processo de desenho do sistema. Então aqui subimos um pouco o nível dos testes. Qual o fluxo?

  1) Ocorre um debate sobre as histórias de usuário. O que será feito e aonde querem chegar.
  2) Há um refinamento da história de usuário com partes mais técnicas de como será desenvolvido e a criação dos testes seguindo essas histórias
  3) Em seguida vem a implementação seguindo os testes de aceite desenvolvidos. E aqui pode ou não utilizar o TDD nas partes mais técnicas do desenvolvimento, é opcional, mas recomendado. Lembre que existem níveis de testes. Eles não são excludentes, eu posso ter testes de aceites e testes de unidade, cada um validando uma parte do projeto.
  4) No fim temos uma apresentação dos resultados e com essa apresentação seguimos novamente o fluxo
  5) Terá as discussões se precisam alterar ou se vão fazer novas histórias, o refinamento das discussões e criação ou atualização dos cenários, a implementação para satisfazer os novos cenários e por fim novas apresentações para avaliações.

---
- BDD (Behavior Driven Development ou Desenvolvimento Orientado por Comportamento)

  Nesse modelo o teste vai expressar utilizando linguagem natural os comportamentos que serão validados de forma que os stakeholders entendam de forma fácil o que o cenário faz. Geralmente é utilizado o formato Dado/Quando/Então.

  Ex: 
    
    **Dado** que o usuário acessa a tela de login
    
    **Quando** o usuário insere as informações de usuário e senha corretamente
    
    **Então** o login deverá ser feito com sucesso 

Com isso podemos interpretar que não faz sentido utilizar o BDD em processos apenas de testes, já que ele é uma ferramenta auxiliar para o desenvolvimento. Se o seu time e o stakeholders não precisam analisar esses cenários, apenas o time de QA quem vai consumir essas informações, faz sentido utilizar outras ferramentas de testes que podem auxiliar melhor o QA e possibilitar adicionar mais detalhes técnicos


### 2.1.4 Resumir como o DevOps pode ter um impacto nos testes

Primeiro vamos entender o que é o DevOps. O DevOps não se resume apenas a ferramentas, ele é uma abordagem organizacional que ajuda a unir o desenvolvimento com as operações. Em outras palavras, o DevOps vai ajudar o time em toda a parte da infraestrutura e integração, então ele é quem estrutura pro código que os desenvolvedores criam para que possa ser disponibilizado de forma mais fácil para testes e para os ambientes de produção e ser integrado nas ferramentas necessárias.

Ganhos e Benefícios do DevOps:

- Autonomia da equipe: A equipe não precisa depender de equipes externas para resolver algum conflito de infraestrutura
- Feedback rápido: Com a integração do código desenvolvido para os ambientes de teste é mais fácil de se ter um feedback sobre esse código. Se tem bug, se as atualizações do código interferiram no funcionamento do que já existia verificando sempre se está tudo pronto para ir para produção.
- Integração Contínua (Continuous Integration CI). O CI é a integração contínua do código para os testes. Então, sempre que uma versão do código é terminada, os testes serão feitos de maneira automática, validando e fornecendo os feedbacks necessários. O CI promove uma abordagem shift-left incentivando os desenvolvedores a sempre enviar códigos de alta qualidade.
- Entrega Contínua (Continuous Delivery CD). O CD é a entrega contínua do código aos usuários.
- Promove processos automatizados. A ideia é que sempre tenha um processo de CI/CD automatizado para facilitar ambientes de testes estáveis e reduzir a necessidade de testes manuais repetitivos. (Não quer dizer que será erradicado de vez os testes manuais, porque testes manuais são importantes, mas aqueles que são repetitivos, sempre executam os mesmo passos, podem ser transformados em testes automatizados.)
- Reduz o risco de regressão. Já que sempre serão feitos testes a cada entrega do código de forma automatizada e devido a escala e ao alcance dessa automação, pode-se diminuir o risco de bugs escondidos que possam interferir no funcionamento do produto no futuro.

Todos esses benefícios permite que as equipes criem, testes e liberem os códigos de forma mais rápido e com uma maior qualidade


Riscos e Desafios do DevOps:

- O pipeline de entrega de DevOps deve ser definido e estabelecido. O Desafio aqui é o conhecimento necessário para fazer toda essa definição, quais ferramentas vão ser utilizadas, como o processo vai ser feito e como vão ser mantidas. Porque a manutenção também é importante, pois sempre haverá atualizações seja no processo ou nas ferramentas.
- A automação de testes pode requerer recursos adicionais e pode ser difícil de estabelecer e manter essa automação. Esse desafio é bem parecido com o anterior, a mesma preocupação de como fazer, o que escolher de ferramentas, como integrar, como manter, mas olhando para a automação dos testes em si.


> Lembrando que. Toda essa ideia de DevOps só é possível se tiver um alto nível de automação nos testes. 


### 2.1.5 Explicar a abordagem shift-lef

O shift-left é um sinônimo para testes antecipados. A ideia é ser uma abordagem que traz o teste para as etapas mais iniciais do SDLC, antes mesmo do código ser desenvolvido. Porém isso não implica dizer que depois da implementação não haverá testes, tem que ter os testes sim, a ideia é aumentar os testes adicionando no começo do processo.

Alguns exemplos de práticas do shift-left:

1. Revisar as especificações do projeto. Essas revisões podem trazer dúvidas e olhares sobres possíveis defeitos como ambiguidade, incompletude e inconsistências. E a ideia é a mesma, o quanto antes for encontrado um bug pode ser evitado.
2. Escrever os cenários de testes antes do código ser escrito e realizar esses testes durante a implementação do código
3. Utilizar CI/CD para poder testar o código sempre que uma entrega for feita. Esse acompanhamento do código-fonte.
4. Concluir a análise estática do código antes do teste dinâmico ou como parte do processo de automação como validação para o código ser aceito no repositório. Essa é a revisão do código e a utilização de ferramentas que analisam se o código está bem escrito segundo um conjunto de regras pré estabelecidas.
5. Realizar testes não funcionais sempre que possível. Geralmente esse tipo de teste é realizado em etapas posteriores.


Essa abordagem pode resultar em um esforço ou custos maiores no início do projeto, mas se espera que tenha como resultado uma economia nos esforços e custos no final. Ja que a ideia aqui é adiantar as validações ao máximo para que diminua o risco de ter bug no final. 


### 2.1.6  Explicar como as retrospectivas podem ser usadas como um mecanismo de melhoria de processos.

A retrospectiva é uma reunião pós entrega em que todo o time participa. Pode ser uma reunião a cada final do sprint ou a cada entrega importante, depende do modelo específico de SDLC que o projeto está seguindo.

Nessa reunião são discutido pontos sobre o trabalho realizado durante o período da entrega ou da sprint:
  - O que foi bem-sucedido? 
      Aqui é abordado pontos que você viu que foi legal. Exemplo: a ajuda que alguém te deu, você pode levantar como um ponto positivo. A equipe de desenvolvimento fez um teste super legal que trouxe benefícios pro projeto, é algo positivo. A comunicação entre time foi bem, se entenderam e o trabalho foi fluido, também é algo positivo. Então nesse ponto são todas as situações que você considera algo positivo dentro do período de tempo que está sendo analisado.

  - O que não foi bem?
      Aqui é o inverso do ponto anterior. O que não foi legal e poderia ter ocorrido de um jeito melhor? Exemplo: Os testes atrasaram horrores e a entrega não pode ser feita, é um ponto negativo. A comunicação do que deveria ser feito foi ruim e houve uns conflitos de atividade e entrega, é um ponto ruim. Os devs não estão testando, pode ser um ponto ruim. 

  - O que podemos fazer para melhorar?
      Não adianta nada só reclamar né? Não se resolve nada reclamando. Então para cada ponto negativo levantado, é discutido uma ação de melhoria, algo que resolva o problema abordado e que na próxima retrospectiva não apareça mais esse problema. 


Essa é a ideia bonitinha de como é uma retrospectiva. Agora o que exatamente essa reunião tem haver com testes e qualidade?

Como essa reunião reúne pontos em relação ao trabalho e todos do time participam é inevitável que apareça algum ponto de positivo ou negativo sobre os testes. E é aí que podemos utilizar esses feedbacks para melhorar o processo de qualidade. Os típicos benefícios que os testes podem adquirir são:

- Se algum ponto de melhoria for em relação ao processo de teste, podemos ter um aumento da eficácia/eficiência dos testes e da qualidade do material de teste.
- Se algum ponto for em relação a equipe, seja que a equipe precisa aprender sobre algo novo, ou se é necessário haver uma comunicação melhor ajuda a ter um melhor vínculo e aprendizado da equipe e uma melhor cooperação entre desenvolvimento e testes
- Se algum ponto for relacionado a qualquer elemento da base de teste, seja um requisito estranho ou um dado faltando, traz a melhoria na qualidade da base de teste.

Enfim, qualquer melhoria apresentada nesta reunião pode ser uma ação de melhoria no processo de teste e esses resultados normalmente fazem parte do relatório de conclusão do teste (vamos ver isso mais tarde 5.3.2). 



## 2.2 Níveis de Teste e Tipos de Teste