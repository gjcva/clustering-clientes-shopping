# Segmentação de Clientes (Clustering)

### 1. O Problema de Negócio
O time de marketing de um shopping center busca otimizar suas campanhas publicitárias. O objetivo é entender o comportamento dos clientes para criar ofertas personalizadas e aumentar a conversão. Como a base de dados não possui rótulos comportamentais prévios, utilizamos técnicas de Aprendizado Não Supervisionado.

### 2. Os Dados
Foi utilizado o conjunto de dados "Mall Customer Segmentation" (fonte: Kaggle). As variáveis selecionadas para a modelagem foram:
* Annual Income (Renda Anual em milhares de dólares).
* Spending Score (Pontuação de Gastos atribuída pelo shopping, escala 1-100).

### 3. Metodologia
O projeto seguiu o seguinte pipeline de dados:
1. **Pré-processamento:** Aplicação de `StandardScaler` para padronizar as escalas de renda e pontuação, garantindo que o algoritmo calcule as distâncias corretamente.
2. **Definição de K:** Utilização do "Método do Cotovelo" (Elbow Method), que indicou que o número ideal de clusters para esta base é 5.
3. **Modelagem:** Aplicação do algoritmo K-Means para segmentação dos clientes.

### 4. Resultados Visuais
O gráfico abaixo demonstra a separação clara dos 5 perfis de consumo identificados pelo modelo:

<img width="892" height="794" alt="image" src="https://github.com/user-attachments/assets/263d9d64-1093-4a2d-bcc9-8ff1db28c744" />

### 5. Análise dos Perfis e Estratégias Sugeridas
Com base na clusterização, definiram-se 5 personas para ação de marketing:

* **Grupo 1 - VIPs (Renda Alta / Gasto Alto):** Clientes de alto valor.
  * *Ação:* Atendimento exclusivo, acesso antecipado a coleções e produtos de luxo.
* **Grupo 2 - Gastadores (Renda Baixa / Gasto Alto):** Consumidores com propensão ao gasto acima da renda.
  * *Ação:* Oferta de cartões de crédito da loja e parcelamento facilitado.
* **Grupo 3 - Poupadores (Renda Alta / Gasto Baixo):** Possuem capital, mas são cautelosos.
  * *Ação:* Marketing focado em custo-benefício, qualidade superior e exclusividade discreta.
* **Grupo 4 - Padrão (Renda Média / Gasto Médio):** Representam a massa de clientes.
  * *Ação:* Programas de fidelidade e acumulação de pontos para aumentar a frequência.
* **Grupo 5 - Econômicos (Renda Baixa / Gasto Baixo):** Consumidores sensíveis a preço.
  * *Ação:* Campanhas de liquidação e cupons de desconto agressivos.

### 6. Ferramentas Utilizadas
* Linguagem: Python 3.
* Bibliotecas: Pandas, Numpy, Scikit-learn (KMeans, StandardScaler), Matplotlib e Seaborn.
