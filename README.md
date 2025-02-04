# ProjetoRH01
Primeiro projeto - Curso Engenharia de Dados - Impacta Tecnologia

Este projeto tem como objetivo analisar dados de recursos humanos para prever a rotatividade de funcionários por meio de algoritmos de aprendizado de máquina. As etapas do processo incluem:  

### 1. **Importação e Análise Exploratória dos Dados**  
- A base de dados é carregada utilizando a biblioteca Pandas, e as primeiras observações são examinadas para uma visão inicial.  
- A distribuição de funcionários que permaneceram ou deixaram a empresa é analisada, tanto no contexto geral quanto segmentada por departamento e faixa salarial.  

### 2. **Pré-processamento dos Dados**  
- Valores ausentes são identificados e, no caso da variável `nivel_satisfacao`, substituídos pela média.  
- Variáveis categóricas são transformadas em valores numéricos por meio da técnica one-hot encoding (`pd.get_dummies()`).  
- Os dados são normalizados com MinMaxScaler para manter todas as variáveis na mesma escala.  

### 3. **Modelagem e Treinamento**  
- São testados dois algoritmos: KNN (K-Nearest Neighbors) e Árvore de Decisão.  
- O conjunto de dados é dividido entre treino (80%) e teste (20%) para avaliar o desempenho dos modelos.  
- O modelo KNN obteve uma taxa de acerto de cerca de 95%, enquanto a Árvore de Decisão se destacou com uma precisão de 98%.  

### 4. **Validação Cruzada**  
- A validação cruzada é aplicada para garantir a confiabilidade dos modelos. A Árvore de Decisão apresentou uma média de acurácia superior a 97%, demonstrando melhor desempenho.  

### 5. **Análise da Importância das Variáveis**  
- A relevância de cada atributo dentro do modelo de Árvore de Decisão é verificada, destacando `nivel_satisfacao`, `ult_avaliacao` e `num_projetos` como os fatores mais influentes na previsão da rotatividade.  

### 6. **Salvamento e Implantação do Modelo**  
- O modelo de Árvore de Decisão é treinado utilizando todos os dados disponíveis e salvo no formato `pickle`, permitindo sua reutilização em aplicações futuras.  

Este projeto é uma ferramenta estratégica para empresas interessadas em compreender os principais fatores que afetam a retenção de funcionários e tomar decisões baseadas em dados para reduzir a taxa de rotatividade.
