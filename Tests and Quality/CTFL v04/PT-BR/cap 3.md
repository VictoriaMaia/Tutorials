[PT-BR]

Essa explicação é baseada em:

- [CTFL Syllabus v4.0](https://bstqb.online/docs/syllabus_ctfl_4.0br.pdf)
- [Curso Preparatório para Certificação em Testes de Software CTFL (ISQTB) do professor Leonardo Carvalho - UDEMY](https://www.udemy.com/course/preparatorio-ctfl/?couponCode=OF83024E)

# 3 Teste Estático

- [3 Teste Estático](#3-teste-estático)
  - [3.1 Noções básicas de Teste Estático](#31-noções-básicas-de-teste-estático)
    - [3.1.1 Reconhecer os tipos de produtos que podem ser examinados pelas diferentes técnicas de teste estático.](#311-reconhecer-os-tipos-de-produtos-que-podem-ser-examinados-pelas-diferentes-técnicas-de-teste-estático)
    - [3.1.2 Valor do teste estático](#312-valor-do-teste-estático)
    - [3.1.3 Diferenças entre testes estáticos e testes dinâmicos](#313-diferenças-entre-testes-estáticos-e-testes-dinâmicos)
  - [3.2 Processo de feedback e revisão](#32-processo-de-feedback-e-revisão)
    - [3.2.1 Benefícios do feedback antecipado e frequente dos stakeholders](#321-benefícios-do-feedback-antecipado-e-frequente-dos-stakeholders)
    - [3.2.2 Atividades do processo de revisão](#322-atividades-do-processo-de-revisão)
    - [3.2.3 Funções e responsabilidades nas revisões](#323-funções-e-responsabilidades-nas-revisões)
    - [3.2.4 Tipos de revisão](#324-tipos-de-revisão)


## 3.1 Noções básicas de Teste Estático 

Primeiro vamos definir o que é teste estático. Estático remete a parado. Então você pode usar essa associação.

No teste estático o software não é executado, é analisado todos os produtos desenvolvidos dentro do projeto (incluindo o software), seja de forma manual como uma revisão ou usando alguma ferramenta como verificadores ortográficos ou ferramentas de legibilidade, como por exemplo, SonarQube.

O objetivo desse teste é o mesmo: melhorar a qualidade, detectar defeitos, avaliar características como legibilidade, integridade, correção, testabilidade e consistência. 


### 3.1.1 Reconhecer os tipos de produtos que podem ser examinados pelas diferentes técnicas de teste estático.

Todo e qualquer produto que possa ser lido, compreendido e que possam ser verificados é um produto que pode ser examinado pelo teste estático.

Exemplos de produtos que podem ser objeto de teste:
- Documento de especificação de requisitos
- Código fonte do software desenvolvido
- Plano de teste
- Casos de teste
- Lista de pendências do produto
- Carta de teste
- Documentação do projeto
- Contratos
- Modelos
- Especificações
- História de usuários
- Arquitetura
- Contratos
- Etc..


Temos a revisão, em que pode ser aplicadas para garantir que o texto estejam completos e compreensíveis e que estão incluindo todos os critérios de aceite. 

E temos a análise estática que inclui verificações sobre a escrita, geralmente essas análises são incorporadas às estruturas de CI e ajudam a avaliar a capacidade de manutenção e segurança.


### 3.1.2 Valor do teste estático

O teste estático pode trazer como valor:

- Ele pode detectar defeitos nas primeiras fases do SDLC, cumprindo o princípio do teste antecipado
- Pode identificar defeitos que não foram detectados nos testes dinâmicos como por exemplo: código inacessível, padrões de projeto não implementados conforme foi planejado, e defeitos em documentações
- Pode gerar uma maior confiança nos produtos de trabalho
- As histórias de usuário podem melhorar a medida que o testador revisa e tirar possíveis dúvidas
- Os stakelholders também pode se certificar de que os requisitos estão de fato descrevendo suas necessidades 
- Os custos gerais são menores quando feito o teste estático por possibilitar a correção de defeitos antecipadamente. Exemplo: Se é evitado uma definição esta mal descrita, consequentemente é evitado que ocorra toda uma implementação errada e uma necessiade de correção no futuro.


### 3.1.3 Diferenças entre testes estáticos e testes dinâmicos

Existem alguma diferenças entre os dois testes:

- Existem tipos de defeitos que só conseguem ser encontrados nos testes estáticos e outros nos testes dinâmicos, por mais diferentes que sejam eles se complementam.
- O teste estático pode ajudar o teste dinâmico validando partes de código que são difíceis de alcançar ou raramente executáveis.
- O teste estático encontra defeitos diretamente, então o que ele encontrar de errado ou incompleto já é considerado um defeito. O teste dinâmico não, ele causa uma falha e essa falha depois de analisada é associada a um defeito.
- Como visto antes, o teste estático é aplicado pode medir a qualidade de produtos de trabalho que não são executáveis (ex: avaliar a capacidade de manutenção do código), enquanto o teste dinâmico só é aplicado e pode medir a qualidade de produtos executáveis (ex: avaliar a qualidade da eficiência de performance).

Existem defeitos que são mais fáceis de serem encontrados nos testes estáticos:

- Defeitos nos requisitos (p. ex., inconsistências, ambiguidades, contradições, omissões, imprecisões, duplicações)
- Defeitos de projeto (p. ex., estruturas de banco de dados ineficientes, modularização deficiente)
- Certos tipos de defeitos de codificação (p. ex., variáveis com valores indefinidos, variáveis não declaradas, código inacessível ou duplicado, complexidade excessiva do código)
- Desvios dos padrões (p. ex., falta de adesão às convenções de nomenclatura nos padrões de codificação)
- Especificações incorretas da interface (p. ex., número, tipo ou ordem de parâmetros incompatíveis)
- Tipos específicos de vulnerabilidades de segurança (p. ex., estouro de buffer)
- Lacunas ou imprecisões na cobertura da base de testes (p. ex., testes ausentes para um critério de aceite)


## 3.2 Processo de feedback e revisão

### 3.2.1 Benefícios do feedback antecipado e frequente dos stakeholders

Incluir o stakeholder no processo é crucial para que o projeto dê certo. Você incluí-los e receber feedback frequentes e o mais antecipado que conseguir vai fazer com que evite mal-entendidos sobre os requisitos, retrabalho, perda de prazos e até mesmo nos últimos casos fracasso total do projeto. 

Ter eles incluídos nos processos principalmente no começo onde estão definindo tudo, você consegue garantir o máximo possível que o produto está sendo desenvolvido atendendo as expectativas deles. E no final isso é o que mais importa já que os projetos são feitos apenas para eles.


### 3.2.2 Atividades do processo de revisão

Existe um processo de revisão genérico que fornece uma estrutura de como fazer esse processo dividido em etapas.

> Lembrando que analise a sua situação para definir se esse processo se encaixa ou não na sua realidade.

As atividades são:

- Planejamento: Assim como todo planejamento, é nessa atividade que você vai arquitetar e organizar tudo. Vai definir o que será revisado, quais as características de qualidade a serem avaliadas, os critérios de saída, as informações de apoio que os revisores irão precisar para entender o contexto, o esforço aplicado a essa revisão e os prazos a serem cumpridos.

- Início da revisão: O objetivo é garantir que todos os envolvidos estejam preparados para começar a revisão. Inclui garantir que todos tenham acesso ao produto de trabalho que será revisado e a tudo que eles precisem e que todos os participantes entendam suas devidas funções e responsabilidades dentro da revisão.

- Revisão individual: É a revisão em si. Cada revisor irá fazer a sua revisão de forma individual, avaliando a qualidade do produto seguindo o que foi definido no planejamento. Ao fim da revisão os avaliadores irão registrar todas as anomalias, recomendações e perguntas que eles identificaram.

- Comunicação e análise de problemas: Todas as anomalias precisam ser analisadas e discutidas, porque nem toda anomalia necessariamente é um defeito. Para cada defeito encontrado deve ser tomada uma decisão sobre o status e ações necessárias para corrigi-lo. Nessa atividade também é decidido qual o nível de qualidade do produto que foi revisado e quais ações de acompanhamento são necessárias

- Correção e relatório: Para cada defeito é criado um relatório para que as ações corretivas possam ser acompanhadas. Quando no fim os critérios de saída que foram definidos no planejamento forem atingidos, o produto poderá ser aceito. Todos os resultados da revisão são relatados.


### 3.2.3 Funções e responsabilidades nas revisões

Esse processo de revisão que foi abordado na seção anterior é feito com vários participantes, cada participante pode ter um ou mais papeis, que podem ser:

- Gerente: é quem decide o que deve ser revisado. E é ele quem fornece os recursos necessários como: equipe e tempo para a revisão.
- Autor: é quem cria e corrige o produto de trabalho em análise
- Moderador ou Facilitador: é quem garante o andamento da revisão de forma eficaz. Ele é quem vai mediar, gerenciar o tempo e possibilitar que todos possam falar livremente, mas garantindo que o foco estará presente.
- Relator ou Registrador: É como se fosse quem faz a ata da reunião. Ele vai reunir as anomalias dos revisores e registrar as informações da revisão
- Revisor: É quem vai revisar. Pode ser uma pessoa que trabalha no projeto, um especialista no assunto ou qualquer outra parte interessada em fazer essa revisão.
- Líder da revisão: É quem vai assumir a responsabilidade geral pela revisão, ele decide quem estará envolvido, e organiza quando e onde a revisão é realizada.




### 3.2.4 Tipos de revisão