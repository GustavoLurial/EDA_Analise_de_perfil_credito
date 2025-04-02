# Análise Exploratória Perfil de crédito
![image](https://github.com/user-attachments/assets/b2b12755-213a-4aaa-8310-b098e8f482f6)

Este projeto consiste na análise de dados fictícios concedidos pela PoD Academy, com objetivo de entender o perfil de clientes Inadimplentes e Adimplentes
## Etapas:

### **1 - Entendimento do negócio**

O problema apresentado traz o desafio de prever a **capacidade de um cliente para reembolsar um empréstimo**. Neste cenário, a empresa PoD Bank se esforça para expandir o acesso ao crédito para uma clientela com **histórico de crédito insuficiente ou inexistente**. Utilizando uma variedade de fontes de dados, incluindo registros de transações bancárias, histórico de pagamentos, e informações socioeconômicas, o objetivo é construir um **modelo preditivo que possa avaliar a probabilidade de inadimplência de um cliente**.

Este problema é crucial porque ajuda a empresa a **minimizar os riscos de crédito** ao mesmo tempo em que possibilita o acesso a **empréstimos para indivíduos que tradicionalmente não teriam essa oportunidade**. Portanto, trata-se de um equilíbrio entre responsabilidade financeira e inclusão social

- **Público**: clientes que irão solicitar empréstimo na Pod Bank. Em nossa tabela, esse público é representado por um número do emprestimo - cada linha um emprestimo.

#### **Para esse estudo será realizado uma EDA para identificar padrões no perfil das pessoas Inadimplentes e Adimplentes**
- Definição de uma pessoa inadimplente: Uma pessoa inadimplente é aquela que não paga suas dívidas no prazo acordado.

### **2 - Entendimento dos Dados**
Para a resolução dessa análise será usado uma base de dados de pessoas que solicitaram crédito ao banco disponibilizada pela PoD Academy (dados fictícios para fins didáticos)
Temos como Target a coluna TARGET, onde 1 significa inadimplente e 0 adimplente, o dicionário de dados estará em anexo junto do notebook

#### **2.3 - Dicionário de Dados**
Está disponível em um arquivo xlsx

### **3 - Importações, Pré processamento e limpeza**
Nessa etapa realizei a limpeza excluindo colunas com cardinalidades iguais a 1 e com número de nulos muito grande, apenas uma coluna com missing alto foi mantida (EXT_SOURCE_1) pois ela é uma coluna que eu desconfiei que poderia ser útil
Aqui eu também não realizei a substituição dos valores nulos por valores simbólicos pois queria ter certeza se a aparição de nulos poderia ser um indicativo para inadimplência.

### **4 - Análise Exploratória dos dados (EDA)**

Aqui fiz todas as análises estatísticas Univariadas e Multivariadas dividindo em Numéricas e Categóricas.

### **5 - Insights**
**Adimplentes**
- Possuem uma média salarial maior, pois possuem uma % maior de pessoas com Higher education, indicando que pessoas com mais escolaridades conseguem ganhar mais e controlar melhor as suas finanças. Eles são ligeiramente mais  velhos, indicando que a idade pode ser um fator importante também
- Além disso as variáveis EXT_SOURCE que indicam pontuações de fontes externas possuem uma média maior e uma variação muito baixa entre elas (1, 2 e 3), com um desvio padrão baixo também
- 75% dos adimplentes estão empregados por até 7.7 anos e com uma média de 5.4 anos, indicando que pessoas com mais tempo no mesmo emprego estão mais estabilizadas e conseguem pagar as parcelas

**Inadimplentes**
- Possuem uma média salarial menor,pois possuem uma % maior de pessoas que fizeram até o segundo grau
- São pessoas ligeiramente mais novas
- As variáveis EXT_SOURCE indicam uma média mais baixa e uma variação maior, com um desvio padrão alto, indicando que o score deles em outras plataformas não são estão bons
- 75% dos inadimplentes estão empregados por até 5.9 anos com uma média de 4 anos

- As outras variáveis não apresentaram informações relevantes que pudessem ajudar na distinção do perfil de pessoas devedoras ou não

**Considerações**
- Importante levar em consideração que pessoas com baixa escolaridade possuem um salário menor e consequentemente são mais propensas a serem inadimplentes;
- Pessoas mais novas e com relativamente pouco tempo de emprego (sem ter mudado) também são mais propensas a serem inadimplentes;
- Pessoas com scores mais baixos e com grande variação entre essas fontes tendem a ser inadimplentes também
