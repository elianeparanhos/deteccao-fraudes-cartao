
# 🛡️ Detecção de Fraudes em Transações Bancárias

![Gráfico de Análise de Fraude](grafico_fraude.png)

## 1. O Desafio do Negócio
O objetivo deste projeto foi desenvolver um modelo de Inteligência Artificial capaz de identificar transações fraudulentas em cartões de crédito. O principal desafio enfrentado foi o **desbalanceamento de dados**, onde as fraudes representavam apenas 3% do volume total, exigindo técnicas avançadas para que o modelo não ignorasse as anomalias.

## 2. Pilares Técnicos e Tecnologias
* **Linguagem:** Python
* **Bibliotecas:** Pandas (Tratamento), Scikit-Learn (Machine Learning), Matplotlib/Seaborn (Visualização).
* **Algoritmo:** Random Forest Classifier com pesos balanceados.

## 3. Desenvolvimento e Estratégia
* **Análise de Sinal vs Ruído:** Identifiquei que variáveis aleatórias impedem o aprendizado da IA. Realizei ajustes para destacar padrões de comportamento fraudulento (como valores atípicos).
* **Tratamento de Classes:** Utilizei o parâmetro `class_weight='balanced'` para garantir que o modelo desse a devida importância aos casos raros de fraude.
* **Engenharia de Atributos:** Transformação de variáveis categóricas (Localidade) em numéricas via `LabelEncoder`.

## 4. Performance do Modelo (Métricas de Segurança)
Diferente de projetos comuns, aqui foquei no **Recall**, pois em fraudes o custo de deixar um criminoso passar (Falso Negativo) é muito superior ao de revisar uma compra legítima.
* **Recall (Fraude):** 1.00 (O modelo capturou 100% das tentativas de fraude no conjunto de teste).
* **Precision:** 1.00 (Zero alarmes falsos registrados nesta rodada).

## 5. Conclusão
Este projeto demonstra a capacidade de lidar com problemas de segurança cibernética e dados desbalanceados, focando em métricas que realmente impactam o ROI e a segurança do cliente final.
