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
   
Lembra que eu disse que o teste era uma forma de economia? Então, quando mais cedo os testes encontrarem defeitos, mais economia de tempo e dinheiro será gerada e menos defeitos subsequentes irão aparecer no processo final de desenvolvimento.

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
>"validar se esse software atende as necessidades dos usuários e dos stakeholders."
