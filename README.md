# Segmentação de Clientes (Clustering)

### 1. O Problema de Negócio
O time de marketing de um shopping center precisa entender o comportamento dos seus clientes para criar campanhas personalizadas. Como a base de dados não possui rótulos prévios, utilizamos técnicas de Aprendizado Não Supervisionado para encontrar padrões de consumo ocultos.

### 2. Os Dados
Utilizou-se o dataset "Mall Customer Segmentation" (Kaggle).
* Variáveis principais: Annual Income (Renda Anual) e Spending Score (Nota de Gastos de 1-100).

### 3. Metodologia
* Pré-processamento: Padronização dos dados com StandardScaler para colocar renda e pontuação na mesma escala numérica.
* Definição de K: Aplicação do Método do Cotovelo (Elbow Method), identificando que o número ideal de clusters para este conjunto de dados é 5.
* Algoritmo: Execução do K-Means para agrupar os dados baseado na proximidade vetorial.

### 4. Resultados (Perfis Identificados)
Foram identificados 5 grupos distintos de consumidores, permitindo as seguintes estratégias:

1.  VIPs (Renda Alta / Gasto Alto): O público de maior valor agregado. Estratégia sugerida: Atendimento exclusivo, pré-vendas e produtos de luxo.
2.  Gastadores (Renda Baixa / Gasto Alto): Consumidores com propensão ao consumo acima da renda. Estratégia sugerida: Oferta de linhas de crédito e parcelamento facilitado.
3.  Poupadores (Renda Alta / Gasto Baixo): Possuem capital mas são cautelosos. Estratégia sugerida: Marketing focado em proposta de valor, qualidade superior e exclusividade técnica.
4.  Padrão (Renda Média / Gasto Médio): Representam a média da base. Estratégia sugerida: Programas de fidelidade para incentivar o aumento do ticket médio.
5.  Econômicos (Renda Baixa / Gasto Baixo): Consumidores sensíveis a preço. Estratégia sugerida: Liquidações de estoque e cupons de desconto.

### 5. Ferramentas Utilizadas
* Linguagem: Python
* Bibliotecas: Pandas, Scikit-learn, Matplotlib e Seaborn.
