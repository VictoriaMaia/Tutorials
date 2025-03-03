[PT-BR]

Essa explicação é baseada em:

- [CTFL Syllabus v4.0](https://bstqb.online/docs/syllabus_ctfl_4.0br.pdf)
- [Curso Preparatório para Certificação em Testes de Software CTFL (ISQTB) do professor Leonardo Carvalho - UDEMY](https://www.udemy.com/course/preparatorio-ctfl/?couponCode=OF83024E)

# 3 Teste Estático

- [3 Teste Estático](#3-teste-estático)
  - [3.1 Noções básicas de Teste Estático](#31-noções-básicas-de-teste-estático)
    - [3.1.1 Reconhecer os tipos de produtos que podem ser examinados pelas diferentes técnicas de teste estático.](#311-reconhecer-os-tipos-de-produtos-que-podem-ser-examinados-pelas-diferentes-técnicas-de-teste-estático)
    - [3.1.2 Valor do teste estático](#312-valor-do-teste-estático)


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