[PT-BR]

Essa explicação é baseada em:

- [CTFL Syllabus v4.0](https://bstqb.online/docs/syllabus_ctfl_4.0br.pdf)
- [Curso Preparatório para Certificação em Testes de Software CTFL (ISQTB) do professor Leonardo Carvalho - UDEMY](https://www.udemy.com/course/preparatorio-ctfl/?couponCode=OF83024E)

# Capítulo 2 Testes ao longo do Ciclo de Vida de Desenvolvimento de Software


- [Capítulo 2 Testes ao longo do Ciclo de Vida de Desenvolvimento de Software](#capítulo-2-testes-ao-longo-do-ciclo-de-vida-de-desenvolvimento-de-software)
  - [2.1 Testes no contexto de um Ciclo de Vida de Desenvolvimento de Software](#21-testes-no-contexto-de-um-ciclo-de-vida-de-desenvolvimento-de-software)
    - [2.1.1 Explicar o impacto do ciclo de vida de desenvolvimento de software escolhido nos testes.](#211-explicar-o-impacto-do-ciclo-de-vida-de-desenvolvimento-de-software-escolhido-nos-testes)
    - [2.1.2 Relembrar as boas práticas de teste que se aplicam a todos os ciclos de vida de desenvolvimento de software.](#212-relembrar-as-boas-práticas-de-teste-que-se-aplicam-a-todos-os-ciclos-de-vida-de-desenvolvimento-de-software)


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



