[PT-BR]

Essa explicação é baseada em:

- [CTFL Syllabus v4.0](https://bstqb.online/docs/syllabus_ctfl_4.0br.pdf)
- [Curso Preparatório para Certificação em Testes de Software CTFL (ISQTB) do professor Leonardo Carvalho - UDEMY](https://www.udemy.com/course/preparatorio-ctfl/?couponCode=OF83024E)

# Capítulo 1 Fundamentos de Teste

- [Capítulo 1 Fundamentos de Teste](#capítulo-1-fundamentos-de-teste)
  - [1.1 O que é teste?](#11-o-que-é-teste)
    - [FL-1.1.1 Identificar objetivos típicos de teste](#fl-111-identificar-objetivos-típicos-de-teste)
    - [FL-1.1.2 Diferenciar teste de depuração](#fl-112-diferenciar-teste-de-depuração)
  - [1.2 Por que os testes são necessários?](#12-por-que-os-testes-são-necessários)
    - [FL-1.2.1 Exemplificar por que os testes são necessários](#fl-121-exemplificar-por-que-os-testes-são-necessários)
    - [FL-1.2.2 Relembrar a relação entre testes e garantia de qualidade](#fl-122-relembrar-a-relação-entre-testes-e-garantia-de-qualidade)
    - [FL-1.2.3 Distinguir entre causa raiz, erro, defeito e falha](#fl-123-distinguir-entre-causa-raiz-erro-defeito-e-falha)
  - [1.3 Princípios de teste](#13-princípios-de-teste)
    - [FL-1.3.1 Explicar os sete princípios de teste](#fl-131-explicar-os-sete-princípios-de-teste)
  - [1.4 Atividades de teste, Testware e Papeis de teste](#14-atividades-de-teste-testware-e-papeis-de-teste)
    - [FL-1.4.1 Resumir as diferentes atividades e tarefas de teste e FL-1.4.3 Diferenciar testware que dá suporte às atividades de teste](#fl-141-resumir-as-diferentes-atividades-e-tarefas-de-teste-e-fl-143-diferenciar-testware-que-dá-suporte-às-atividades-de-teste)
    - [FL-1.4.2 Explicar o impacto do contexto no processo de teste](#fl-142-explicar-o-impacto-do-contexto-no-processo-de-teste)
    - [FL-1.4.4 Explicar o valor de manter a rastreabilidade](#fl-144-explicar-o-valor-de-manter-a-rastreabilidade)

## 1.1 O que é teste?

### FL-1.1.1 Identificar objetivos típicos de teste

Para começar precisamos entender, o que é teste? Dado que você está trabalhando com uma equipe de desenvolvimento e que essa equipe está desenvolvendo um software (seja ele qual for), o teste é quem vai avaliar esse software alvo.

Essa avaliação ajuda a reduzir o risco da falha, descobrir os defeitos e validar se esse software atende as necessidades dos usuários e dos stakeholders.

Então podemos definir alguns dos objetivos do teste como:

- Detectar falhas e defeitos
- Garantir uma cobertura de testes ao software alvo
- Reduzir o nível de risco de qualidade
- Verificar se os requisitos foram atendidos

### FL-1.1.2 Diferenciar teste de depuração

A depuração diferente do teste vai se preocupar em encontrar as causas das falhas dos defeitos encontrados pelos testes e corrigi-las. Resumindo a depuração aplica 3 passos:

1) Reproduzir a falha
2) Diagnosticar a causa
3) Corrigir

## 1.2 Por que os testes são necessários?

### FL-1.2.1 Exemplificar por que os testes são necessários

A gente já sabe que o teste vai validar o software alvo. Então pensando assim podemos afirmar que o teste é necessário como uma forma de controle de qualidade. Eles ajudam a atingir os objetivos acordados dentro do escopo do projeto.

Só que essa qualidade não é válida apenas quando o software é desenvolvido, tem a possibilidade de aplicar essa validação de qualidade nos vários estágios do processo de desenvolvimento o que acaba sendo um meio econômico de detectar defeitos, já que quanto antes encontrar, mais rápido se concerta e o defeito não chega ao usuário.

### FL-1.2.2 Relembrar a relação entre testes e garantia de qualidade

A gente viu que os testes são um tipo de controle de qualidade. O controle de qualidade ou Quality Control (QC), é uma abordagem orientada ao produto, ou seja, o objetivo dessa abordagem é garantir a qualidade do produto em si. Os resultados dos testes dessa abordagem são usados para gerar as correções dos defeitos encontrados por eles.

> Lembrando que essa abordagem é responsabilidade de todo o time de desenvolvimento.

Agora, a garantia de qualidade ou Quality Assurance (QA) é uma abordagem preventiva, ela é voltada ao processo como um todo. Então, qualquer aprimoramento de processo, qualquer ação que faça as etapas de desenvolvimento melhorarem em qualidade é uma ação dessa abordagem. Os métodos incluem: testes, verificação de modelos, prova de exatidão, simulação e prototipagem. Os resultados dos testes dessa abordagem são usados para fornecer feedback sobre a performance dos processos de desenvolvimento.

### FL-1.2.3 Distinguir entre causa raiz, erro, defeito e falha

Um dos pontos que eu acho que às vezes ficam mais confusos é a diferença desses tópicos. Mas uma frase que ajuda a entender o fluxo é:

> A pessoa erra gerando um defeito que produz a falha

Um dos pontos que eu acho que às vezes ficam mais confusos é a diferença desses tópicos. Mas uma frase que ajuda a entender o fluxo é:

A pessoa erra gerando um defeito que produz a falha

A pessoa (desenvolvedor ou não) erra. Ocorreu um erro ou um engano na hora de fazer a atividade seja uma atividade de definir requisitos ou a atividade de desenvolver. Existem muitos motivos para que esse erro surja como: pressa, pressão no prazo, falta de conhecimento, infraestrutura complexa, mudanças na tecnologia, etc.

↓

gerando um defeito (bug). É algo errado ou faltando. Se o erro ocorreu no começo do ciclo de desenvolvimento ele gerou um defeito na documentação, ou nas definições de requisitos, por exemplo. Se o erro foi na implementação de um código, o defeito acontece na execução do sistema fazendo com que ele atue de maneira errada.

↓

que produz a falha. A falha é o resultado do erro e do defeito, porém, fatores externos e/ou não controláveis podem gerar também a falha, como condições ambientais, falta de energia, etc. E existem falhas que ocorrem apenas em circunstâncias tão específicas que nunca aparecem.

↓

Quando ocorre a falha começa a investigação para descobrir a causa raiz. A causa raiz é o motivo fundamental que gerou aquela falha.
Lembra da depuração? No processo de depuração pode ser feita a investigação para encontrar a causa raiz.

## 1.3 Princípios de teste

### FL-1.3.1 Explicar os sete princípios de teste

Temos 7 princípios de teste:

1) O teste mostra a presença de bugs, não a ausência de defeitos.

Sim, os testes não vão fazer milagre no software, eles vão reduzir a probabilidade de defeitos ficarem escondidos e chegarem ao usuário final, mas não implica dizer que a aplicação ao fim do desenvolvimento e validação vai estar livre de defeitos.

2) Testes exaustivos são impossíveis.

Testar tudo não dá. Existem infinitas combinações para testar os fluxos de execução do seu sistema, não teria tempo suficiente para validar todos. Além do mais, o desenvolvimento de projeto sempre tende a ter o tempo curto para que seja entregue ao mercado o mais rápido possível.

Por isso existem várias técnicas de testes para tentar ter uma boa cobertura de testes. E por isso é tão importante o ponto de você conseguir se adaptar aos diferentes contextos, para que consiga distinguir as melhores estratégias para seu trabalho.

3) Testes antecipados economizam tempo e dinheiro.

Lembra que eu disse que o teste era uma forma de economia? Então, quando mais cedo incluir testes no processo de desenvolvimento e eles encontrarem defeitos, maior é a economia de tempo e dinheiro.

4) Os defeitos se agrupam.

Seguindo a ideia dos 80/20*, um pequeno grupo geralmente é o responsável por conter a maioria dos defeitos descobertos ou é responsável pela maioria das falhas.

*Princípio de pareto ou 80/20. Aplicando esse princípio em desenvolvimento de software seria equivalente a dizer que 20% das funções são as responsáveis por 80% dos defeitos que aparecem.

5) Os testes se degradam.

Essa degradação está relacionada a muitos fatores, mas um importante fator que faz você entender essa degradação dos testes são as mudanças no projeto. Todo projeto sofre com mudanças, seja de tecnologia utilizada, ou mudança na forma como a aplicação funciona. Com essas mudanças os testes que antes faziam a validação pode não está mais fazendo sentido e por isso degradou.

Exemplo prático. Imagine que a funcionalidade de login não precisava de senha com 8 caracteres, mas agora a feature sofreu uma alteração e é necessário ter o mínimo de 8 caracteres. Os testes que fazem a validação do login vão precisar de atualização, porque da forma como foram implementados podem não pegar o comportamento que agora é necessário (ter o mínimo de 8 caracteres).

Então o melhor a ser feito é sempre revisar os cenários mapeados, validar se ainda fazem sentido ou não, se necessário atualizá-los ou removê-los.

6) Os testes dependem do contexto.

Não tem regra universal que se adeque a todas as situações, sempre vai depender do contexto do seu projeto.
Ta, mas o que seria esse contexto?
Tudo relacionado ao projeto, exemplo:

- Qual o produto a ser desenvolvido (ele é crítico? Precisa de uma bateria maior de testes?, ele é complexo? Precisa de tecnologias específicas para testar?)
- Qual o nível de conhecimento técnico da equipe de desenvolvimento?
- Qual o tipo de empresa que você está trabalhando (é muito burocrática?, precisa de documentos mais específicos?, é uma startup? precisa de mais pressa nas validações por ter um tempo mais curto?)

7) Falácia da ausência de defeitos.

Esse tópico é voltado ao outro ponto de qualidade. Não adianta meu sistema ser perfeito, não ter um bug crítico, funcionar do jeito que especificamos SE ele não atende o cliente ou o usuário final. Se não atender as necessidades no qual ele foi projetado para resolver, o software é classificado como ruim.

E esse ponto também tem que ser validado na parte de qualidade, lembra da seção 1.1? Quais eram os objetivos típicos dos testes? entre os citados existe esse ponto:

> "validar se esse software atende as necessidades dos usuários e dos stakeholders."

## 1.4 Atividades de teste, Testware e Papeis de teste

Lembrando que o processo de teste não é universal, não tem um jeito único para fazer. Por isso existem atividades de teste que formam um processo de teste e que ajudam os testes a alcançarem os seus objetivos. Para cada atividade de teste, existe um testware. O testware é basicamente o resultado, o que a atividade produz no final.

Como essas atividades vão ser usadas e se vão ser usadas vai depender do contexto no qual você está inserido.


### FL-1.4.1 Resumir as diferentes atividades e tarefas de teste e FL-1.4.3 Diferenciar testware que dá suporte às atividades de teste

As atividades de teste e seus testware são:

> Lembrando que elas podem ser executadas em paralelo ou sequencialmente

-----------
-----------

**Planejamento** de teste
- Definição: 
  - Nesta atividade vão ser definidos os objetivos dos testes e as estratégias.
  - É aqui que vai haver uma seleção da abordagem dos testes, como vão atingir o objetivo respeitando as restrições que há no projeto.
  - Lembrando que o planejamento não é escrito em pedra, sem que precisar ele pode ser alterado!  
- Testware:
  - A produção do plano de teste, onde vai ser definido todo o processo de teste. Dentro desse documento tem:
    - cronograma de testes
    - registro de riscos (uma lista de riscos com suas probabilidades, impactos e informações)
    - critérios de entrada e saída

-----------
-----------

**Análise** de teste ou **O que testar?**
- Definição: 
  - A análise é feita sobre a base de testes* para identificar os recursos testáveis, os riscos e níveis de cada risco, definir e priorizar as condições de teste. 
  - Essas análises são feitas baseadas nas técnicas de teste
  - Essa análise de teste também 
- Testware:
  - Relatório de defeitos referentes aos defeitos encontrados na base de dados. Essa análise já é uma forma de validação sobre a base de dados, então se for encontrado algum defeito durante essa atividade, ele constitui um resultado e deverá ser reportado.
  - Condições de testes definidas e priorizadas
  - Critérios de aceite

*Base de testes é qualquer material, seja um requisito, uma função, um fluxo de execução em que meu teste vai se basear para validar os objetivos.

-----------
-----------

**Modelagem** de teste ou **Como testar?**
- Definição:
  - Nessa atividade é feito a elaboração das condições de teste, identificação de itens de cobertura, definição das técnicas de teste que serão usadas, identificação de qualquer infraestrutura e ferramenta necessária para o teste.
- Testware:
  - Casos de teste e suas priorizações
  - Carta de teste*
  - Itens de cobertura
  - Requisitos para os testes, seja requisito de dados (o que de dados precisamos para testar) ou de ambiente (as ferramentas, software, hardware necessários)

*Carta de teste são utilizadas em testes exploratórios para guiar a execução. O teste exploratório vai ser explicado em detalhes em outra seção!

-----------
-----------

**Implementação** de teste 
- Definição:
  - Nessa atividade a gente viu que baseado nas atividades anteriores o que vai testar e como, mas agora precisamos agir e executar o planejamento feito. Então, nessa atividade vai ser feito:
    - a criação dos scripts de teste, sejam eles automatizados ou manuais, 
    - criação e aquisição do material de teste,
    - organização dos procedimentos de testes, os passos para a realização de cada cenário
    - organização do conjuntos de testes 
    - priorização e organização dos testes em um cronograma de execução.
- Testware:
  - Procedimentos de teste. Os passo a passo do testes com todos os detalhamentos necessários
  - Scripts de automação
  - Conjuntos e dados de teste
  - Cronograma de execução
  - Elementos do ambiente de teste. Basicamente a descrição do ambiente, o que é necessário pra ele ter para que os testes executem


-----------
-----------

**Execução** de teste
- Definição:
  - Execução dos testes de acordo com o cronograma. A execução pode ser manual ou automatizada, 
  - Comparação dos resultados dos testes com o que era esperado
  - Geração de resultados para analisar as anomalias e reporte de possíveis falhas.
- Testware:
  - Registros de teste
  - Relatórios de defeitos encontrados

-----------
-----------

**Conclusão** de teste
- Definição:
  - A cada marco do projeto (lançamento, fim da iteração, etc) é feito a conclusão dos testes que incluem:
    - Identificar todos os materiais de testes e entregar as equipes apropriadas
    - Encerrar o ambiente de teste em um estado acordado
    - Analisar as atividade de teste para identificar as lições aprendidas e as melhorias futuras
    - E gerar um relatório de conclusão dos testes para ser enviado ao stakeholders. Esse relatório geralmente mostra uma visão geral do que tivemos de resultados, exemplo: quantidade de bugs encontrados, quantos testes foram desenvolvidos, etc.
- Testware:
  - Relatório de teste
  - Itens de ação e lições aprendidas para a melhoria dos próximos projetos ou próximas entregas.

-----------
-----------

**Monitoramento e controle** de teste
- Definição:
  - Essa atividade é feita em paralelo com todas as outras. Todas as atividades de testes podem e devem ser monitoradas para haver uma verificação contínua e uma comparação com o progresso do plano e se necessário tomar ações necessárias como por exemplo atualizações ou mudanças no que foi definido em algumas das atividades para atingir os objetivos.
  - É nessa etapa também que ocorre a comunicação contínua com os stakeholders por meio de relatórios. O progresso deve ser sempre comunicado, principalmente para validar como está o progresso do projeto com as expectativas dos clientes.
- Testware:
  - Relatórios de progresso de teste
  - Documentação de diretrizes de controle
  - Informação sobre os riscos identificados

-----------
-----------


### FL-1.4.2 Explicar o impacto do contexto no processo de teste

Já foi informado aqui que o contexto é quem vai lhe direcionar para qual processo de teste será feito. Essa seção vai falar especificamente desse ponto, qual o impacto e quais pontos do contexto temos que estar de olho.

- Stakeholders: Os testes são financiados pelos stakeholders, eles querem que o projeto no qual estão investindo tenha qualidade e gere bons resultados financeiros. Então o objetivo final do teste, novamente falando, é atender as necessidades desses stakeholders. Logo, eles são parte do seu contexto, você tem que entender quais as necessidades deles, o que eles têm de expectativa do produto ou de informação, se eles são stakeholders que gostam de participar e cooperar, ou apenas querem ver os relatórios, etc.

- Membros da equipe: Uma coisa importante para lembrar é: as atividades de teste são parte integrante dos processos de desenvolvimento. Os testes não são feitos de forma isolada, ou seja, a qualidade é responsabilidade de todo o time que está projetando e desenvolvendo o software. Com isso em mente você tem que entender como é o seu time, quais habilidades, conhecimentos, nível de experiência eles possuem, se eles tem disponibilidade, se precisam de treinamento, etc.

- Domínio do negócio: Qual área o projeto está encaixado? Ele está na área de saúde, bancária? A partir desse entendimento você consegue definir a criticidade que seus testes devem ter. Quais são os riscos que você deve identificar, precisa tomar cuidado com alguma norma legal específica?, etc.

- Fatores técnicos: Aqui estão os pontos mais específicos do projeto em si. Qual o tipo de software, a arquitetura do projeto, as tecnologias utilizadas, etc

- Restrições do projeto: Um ponto bastante importante e que vai definir o quanto você consegue fazer. Esse ponto será analisado:
  -  o escopo: dado todo o seu planejamento o que você pensou em testar, 
  -  o tempo: quanto tempo você tem de desenvolvimento e de teste?, e o que você consegue testar dentro desse prazo? Você tem que analisar que não adianta ter um escopo enorme se não vai ter tempo pra executar tudo, 
  -  orçamento: Você precisa de alguma ferramenta paga? O projeto tem recurso financeiro para arcar com tudo? Ou você precisa usar o que tem disponível?, 
  -  recursos: Quais as ferramentas que você tem disponível para executar os seus testes? E como você pode usar elas?
  - etc.

- Fatores organizacionais: Esse ponto é sobre a empresa que você trabalha. Como é a estrutura organizacional da empresa, quais as políticas existentes, as práticas utilizadas nos projetos. Resumindo, você precisa analisar se precisa fazer algo para executar seu planejamento respeitando todas as regras da empresa que você trabalha?

- Ciclo de vida do desenvolvimento de software: Quais são as práticas de desenvolvimento do seu projeto? É um ciclo ágil? Em que você pode atuar em todas as etapas, ou é o tradicional? E você vai atuar apenas no final do ciclo? Quais as práticas de engenharia que estão utilizando?

- Ferramentas: Quais as ferramentas que você tem disponível, a usabilidade delas, etc.


Todos esses pontos vão fazer você definir:

- Estratégia de teste
- Técnicas de testes
- Grau de automação (vai conseguir automatizar, ou o quanto de automação será feito)
- Nível de cobertura 
- Nível de detalhe da documentação de teste (será necessária uma documentação complexa com muitos detalhes?)
- Relatórios (as informações geradas, a frequência, etc)
- etc.


### FL-1.4.4 Explicar o valor de manter a rastreabilidade

A rastreabilidade é um ponto importante no projeto. Ela pode:  
  - dar suporte a avaliação da cobertura de teste: Se conseguimos dizer quais casos de teste temos para quais requisitos, conseguimos avaliar a cobertura dos nosso testes.
  - dar suporte a avaliação dos riscos: Se conseguimos dizer quais resultados dos testes estão relacionados com os riscos mapeados, conseguimos avaliar se o risco ainda esta presente e qual o tamanho dele no projeto.
  - determinar o impacto das mudanças nas features: Se você consegue rastrear quais cenários estão relacionados as features que irão sofrer mudanças, você consegue avaliar qual o impacto dessa mudança, se será necessário atualizar, remover ou adicionar cenários e o esforço para esse trabalho. 
  - auxiliar auditorias de testes, mostrando o histórico dos testes, qual a frequência que o cenário mostra defeitos, quais cenários mostraram os defeitos críticos e assim por adiante.
  - facilitar os relatórios de progresso e de conclusão dos testes
  - fornecer informações para a avaliação da qualidade do produto como: a capacidade do processo, o progresso do projeto em relação aos objetivos, etc.


Mas o que é a rastreabilidade? É a informação que conseguimos ter sobre a origem e destino de uma item do processo de teste. Por exemplo:

Base de teste <-> testware

A partir da base de teste foi gerade algum testware com cenário de teste. Ou seja, conseguimos dizer o destino do que foi gerado com aquela base de teste. 

E a partir do testware eu consigo dizer de qual base de teste ele veio. Ou seja, conseguimos dizer qual a origem daquele cenário gerado.

Nesse exemplo temos a rastreabilidade dos dois caminhos, a origem e o destino, tanto a base de teste -> testware, quanto testware -> base de teste. 


Conseguimos manter a rastreabilidade em todo o processo de teste:

![alt text](<images/Screenshot 2024-10-14 100439.png>)

- Base de teste <-> testware vimos no exemplo acima
- testware <-> resultados: Conseguimos dizer quais resultados são de quais testwares e quais testwares geraram quais resultados
- resultados de teste <-> defeitos: Conseguimos dizer quais defeitos foram encontrados de quais resultados de teste e conseguimos dizer quais resultados acharam os defeitos.

E se olhar para mais passos, vai seguir a mesma lógica. Se olhar-mos para base de teste <-> defeitos, podemos dizer quais partes da base de teste tiveram quais defeitos e vice-versa.


