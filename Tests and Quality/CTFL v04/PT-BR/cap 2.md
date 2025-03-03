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
    - [2.2.1 Distinguir os diferentes níveis de teste.](#221-distinguir-os-diferentes-níveis-de-teste)
    - [2.2.2 Distinguir os diferentes tipos de teste.](#222-distinguir-os-diferentes-tipos-de-teste)
    - [2.2.3 Distinguir o teste de confirmação do teste de regressão.](#223-distinguir-o-teste-de-confirmação-do-teste-de-regressão)
  - [2.3 Teste de Manutenção](#23-teste-de-manutenção)


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

### 2.2.1 Distinguir os diferentes níveis de teste.

Os níveis de teste são grupos de atividades realizadas no software em um determinado estágio de desenvolvimento e para partes específicas do software. Eles não são excludentes, podem ser aplicados em um mesmo momento do projeto. 

Em modelos sequenciais do SDLC os níveis de teste geralmente são definidos de forma que os critérios de saída de um nível façam parte dos critérios de entrada do nível seguinte. Em modelos iterativos pode ser que essa ideia não se aplique.

Cada nível tem os seguintes atributos:
  - Objeto de teste (o que está sendo testado, é um componente, é o sistema como um todo, é uma funcionalidade específica?)
  - Objetivo do teste (o que você quer validar?)
  - Base de teste (o conteúdos que derivam os casos de teste)
  - Defeitos e falhas
  - Abordagem e responsabilidades
  - Ambiente de teste adequado

No syllabus existem 5 níveis de teste:

---
> Teste de componente / Teste de unidade

  Esse nível foca na parte menor do código. Um componente, uma função. Como é algo bem específico, então esses testes vão precisar utilizar do código para que se compreenda quais são os componentes, o que eles fazem e como podem ser testados. Por isso geralmente quem desenvolve esses testes são os desenvolvedores.
  
  Uma outra característica desse teste é que ele é rápido, ele vai validar o comportamento de uma função que faz algo específico. Então é sempre bom que esses testes sejam automatizados para que esses componentes sempre sejam testados em todas as atualizações. Por que? Além dos fatores que já exemplificamos, existe um risco a mais, como estamos tratando da menor parte do código, se algo nesses componentes estiver com mau funcionamento o erro pode se propagar para qualquer parte do sistema e fazer com que outras partes fiquem com comportamentos errados.

  ---
> Teste de integração de componentes / Teste de integração de unidades e Teste de integração de sistema

  O teste de integração em si, independente se é de componente ou de sistema, é validar a integração de duas ou mais partes, validar o funcionamento dessas partes quando elas estão juntas, interligadas. 

  Quando olhamos a integração de componentes, é um nível acima do teste anterior, mas ainda é um teste bem específico que depende do acesso ao código e pode ser executado pelos desenvolvedores.
    
  Já a integração de sistemas é um nível bem maior de abstração que o anterior, mas ainda tem um certo nível de especificidade, você como testador vai analisar os comportamentos dos sistemas quando eles trabalham juntos, olhando os detalhes que não chegam no usuário. Exemplo: digamos que você tenha que testar a integração de uma API com o banco de dados, então você vai fazer cenários para validar se a API está mandando e recebendo os dados de forma correta, se a integração com o banco está correto. Por isso não é necessário e às vezes nem tem permissão para acessar o código fonte desses sistemas.

  Esses testes podem ser feitos de forma automatizada e utilizados nas CI, sendo uma validação feita em todas as entregas contínuas. O motivo, facilitar o descobrimento do motivo de possíveis falhas, se você testar todas as integrações assim que são feitas, a identificação dos problemas será investigando apenas as mudanças mais recentes, porém se deixar pra testar tudo junto vai ser mais complicado tentar achar qual das integrações ou aonde exatamente no sistema esta a razão da falha encontrada.

---
> Teste de sistema
  
  Esse nível  de teste é bem mais abstrato, ele vai simular as ações dos usuários. É o teste mais comum que as pessoas veem sendo feito quando se fala de teste automatizado, onde aparece as telas do sistema sendo abertas e utilizadas de forma automática. Geralmente o teste vai executar um fluxo completo de ações, o chamado testes end-to-end, em que o testador vai definir os fluxos que o usuário pode fazer no sistema e executá-los validando os comportamentos funcionais e não funcionais do sistema, se eles estão de acordo como foram planejados e especificados.

  Esse nível de teste produz informações que serão utilizadas para tomar decisões de liberação. O sistema quando chega nesse nível de teste, subtende-se que já está bem avançado em questão de desenvolvimento e que está próximo da liberação para o mercado, então o teste de sistema é quem pode dar o feedback de que o sistema está pronto para as próximas etapas. 
  
  Ele também tem um risco, se os testes anteriores não tiverem sido feitos, ou não foram feitos de maneira correta, o teste de sistema pode pegar vários erros herdados de componentes ou de integrações e fazer com que o processo de correção seja mais custoso, já que o código vai precisar retornar a etapas que deveriam ter sido concluídas.

---

> Teste de aceite

  Esse é o último nível, nele não estamos atrás de encontrar defeitos, o foco é apresentar o sistema e garantir que esteja funcionando da maneira como especificado para o usuário final. Se for encontrado defeitos, eles são considerados de grandes riscos para o projeto por ter perdurado por todos os outros níveis e chegado até essa etapa.

  Então nesse nível quem vai executar os testes serão os clientes, usuários finais, proprietários do produto, operadores de sistemas e stakeholders. 
  
  Alguns dos testes de aceite são:
  - Aceite de usuário (User Acceptance Testing UAT): O objetivo é basicamente o que definimos, certificar que o sistema atenda as necessidades do usuário. A validação pode ser feita em ambiente de produção ou simulado, mas sempre usando os usuários como executores.
  - Aceite operacional: O objetivo é garantir que os operadores, os administradores do sistema conseguem manter ele funcionando adequadamente para os usuários no ambiente de produção. Vão validar se o usuário consegue fazer backups e restaurações, validar a performance do sistema, e vulnerabilidades de segurança.
  - Aceite contratual e normativo: Esse teste é voltado para sistemas que têm que seguir alguma regra ou lei. Então o objetivo é garantir que o sistema segue a conformidade contratual ou regulatória que foi definida na contratação do desenvolvimento do software. A execução e os resultados podem ser acompanhados por testemunhas ou agências reguladoras.
  - Teste Alfa e Beta: Mesma ideia, testar o sistema com usuários. A diferença é que o teste alfa é feito no local em que o sistema foi desenvolvido, e no teste beta o cliente recebe uma cópia do sistema para testar fora de onde foi desenvolvido.



### 2.2.2 Distinguir os diferentes tipos de teste.

- Teste Funcional
  
  Ele vai avaliar **o que** o sistema deve fazer. Então ele vai avaliar as funções que um componente ou sistema deve executar. Ou seja, está funcionando de acordo com o que foi definido?
  
  Algumas características:
    - A sua eficácia é medida através da cobertura funcional
    - Quem vai fazer esses testes vai precisar de conhecimentos sobre as regras de negócio


- Teste Não Funcional

  Ele vai avaliar **o quão bem** o sistema funciona. Ele vai avaliar as características do software, como: eficiência de performance, compatibilidade, usabilidade, confiabilidade, segurança, capacidade de manutenção e portabilidade. 

  São testes mais subjetivos, não é uma funcionalidade que tem que ter um comportamento específico, são mais características que o software deve ter mas que tem que ser definido o que é o "aceitável". Exemplo: Qual é a quantidade de tempo aceitável que o sistema deve demorar para responder? Ele tem que ser compatível com quais sistemas operacionais ou com quais versões de softwares terceiros? 

  Algumas características:
    - A sua eficácia é medida através da cobertura não funcional
    - Quem vai fazer esses testes vai precisar de conhecimentos sobre tecnologias que podem ser utilizadas para a validação dessas características e conhecimentos técnicos para identificar os possíveis problemas.


- Teste Caixa-Preta

  O nome é literal, o sistema vai se comportar como uma caixa preta, você não vai ver dentro do sistema, vai analisar ele pelo que ele te retorna de comportamento. 
  
  Então o teste de caixa preta é um tipo de teste que é baseado nas especificações do sistema (nas documentações, requisitos, etc) sem ter acesso às estruturas internas do software, como por exemplo o código fonte.

  O principal objetivo é verificar o comportamento do sistema em relação ao que está definido nas suas especificações. Se está se comportando como foi definido. O como está fazendo não entra aqui.


- Teste Caixa-Branca

  No de caixa branca é ao contrário, eu tenho acesso total às infraestruturas do sistema, ao código fonte e se baseando nessa estrutura interna do sistema é que os cenários de teste vão ser feitos.

  Algumas características:
    - A sua eficácia é medida através da cobertura estrutural. Quantos testes exercitam as partes do código ou os componentes, etc.
    - Quem vai fazer esses testes vai precisar de conhecimentos sobre como o código foi construído.
  
  ! O teste de componente, majoritariamente é feito utilizando teste de caixa branca

> Todos esses tipos de teste podem/devem ser aplicados em todos os níveis de teste


### 2.2.3 Distinguir o teste de confirmação do teste de regressão.

Sempre há alteração no sistema, seja para aprimorá-lo adicionando novas features, novos recursos, seja removendo um defeito encontrado. E sempre que há alteração é necessário testar para saber se está funcionando corretamente. Com isso temos os outros dois tipos de testes: o teste de confirmação e o de regressão.

- Teste de confirmação

  Característica principal: **Confirmar se um defeito foi corrigido com sucesso**. 
  
  Às vezes um defeito impacta em muitas features, então quando uma correção é feita, tem que fazer novamente a execução do cenário que encontrou o defeito, para garantir que o defeito foi corrigido e também executar novamente todos os cenários que falharam ou ficaram bloqueados por conta desse defeito.
  
  Além de retestar tudo, é bom adicionar novos testes para cobrir quaisquer alterações que foram necessárias serem feitas na correção do defeito.

  > Quando se tem pouco recurso (seja de tempo ou dinheiro) no projeto e não dá para fazer tudo o que foi dito, o teste de confirmação pode se contar em apenas executar novamente as etapas que reproduziram a falha para validar a correção.


- Teste de regressão

  Característica principal: **Garantir que o que funciona, continua funcionando**. Esse teste vai detectar efeitos colaterais do desenvolvimento.

  Qualquer alteração feita no sistema pode necessitar de alterações em outras partes. O software tem dependências, integrações que podem acabar precisando ser alteradas quando é feito uma atualização de alguma feature. Com isso em mente, o teste de regressão vai tentar detectar se alguma mudança (seja ela qual for) não impactou negativamente em nenhuma outra feature, vai tentar detectar que o que já está funcionando continuou funcionando com a mudança feita.

  Os testes de regressão são fortes candidatos a serem testes automatizados com uma CI, por ser um tipo de teste que precisa ser executado várias vezes. Cada mudança é necessário executar todos os cenários que já existiam e criar novos cenários para cobrir o que veio de novo. Então a cada iteração e versão do software é aumentado o número de casos de teste.


## 2.3 Teste de Manutenção

   Quando o software vai ao mercado, e seus clientes começam de fato a usá-lo é necessário começar a etapa de manutenção. O sistemas precisa ser mantido de forma funcional, sempre será preciso fazer algo. Então pode ser necessário fazer alguma ação de manutenção como:
  
    - Modificação: qualquer alteração como aprimoramentos, atualizações, correções, hotfixes, atualizações operacionais.
    - Atualização/Migração: migrações ou atualizações de plataforma ou ambiente operacional.
    - Aposentadoria: quando um sistema chega ao fim da sua vida útil. É necessário testes de arquivamento/retenção/restauração dos dados.
  
  Antes de fazer qualquer mudança é sempre bom fazer uma análise de impacto, para ajudar na decisão se deve ou não ser feita essa mudança, quais as possíveis consequências, os passos necessários, etc.

  Então o teste aqui vai ser aplicado para validar o sucesso da implementação de alguma manutenção e verificar se não teve nenhum efeito colateral no resto do sistema (no fim das contas aqui é o teste de regressão). O escopo desse tipo de teste depende do grau de risco da mudança, o tamanho da mudança, e o tamanho do sistema.
