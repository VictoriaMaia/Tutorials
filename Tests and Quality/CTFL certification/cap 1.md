[PT-BR]

# Capítulo 1 Fundamentos de Teste

- [Capítulo 1 Fundamentos de Teste](#capítulo-1-fundamentos-de-teste)
  - [1.1 O que é teste?](#11-o-que-é-teste)
    - [FL-1.1.1 Identificar objetivos típicos de teste](#fl-111-identificar-objetivos-típicos-de-teste)
    - [FL-1.1.2 Diferenciar teste de depuração](#fl-112-diferenciar-teste-de-depuração)
  - [1.2 Por que os testes são necessários?](#12-por-que-os-testes-são-necessários)
    - [FL-1.2.1 Exemplificar por que os testes são necessários](#fl-121-exemplificar-por-que-os-testes-são-necessários)
    - [FL-1.2.2 Relembrar a relação entre testes e garantia de qualidade](#fl-122-relembrar-a-relação-entre-testes-e-garantia-de-qualidade)
    - [FL-1.2.3 Distinguir entre causa raiz, erro, defeito e falha](#fl-123-distinguir-entre-causa-raiz-erro-defeito-e-falha)



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

>A pessoa erra gerando um defeito que produz a falha

A pessoa (desenvolvedor ou não) erra na sua atividade, seja ela desenvolver uma aplicação ou definir um requisito, por exemplo. Existem muitos motivos para que esse erro surja como: pressa, complexidade do requisito, ambiguidade no que foi solicitado, etc

 ↓

gerando um defeito (bug). É algo errado ou faltando. Pode ser um requisito com defeito, ou um código defeituoso. Como foi dito antes, o teste pode ser feito em qualquer estágio de desenvolvimento, então o defeito não necessariamente tem que ser um código errado. É algo diferente do que foi definido como correto. 

 ↓
 
que produz a falha. A falha é o resultado negativo do erro e do defeito, porém, fatores externos e/ou não controláveis podem gerar também a falha, como condições ambientais, falta de energia, etc.

 ↓

Encontrando o defeito pode ser feita a investigação para encontrar a causa raiz do problema. A causa raiz é o motivo fundamental para a ocorrência de um problemas. 
Lembra da depuração? Na depuração pode ser feita a investigação para encontrar a causa raiz.


