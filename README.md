# 📊 Previsão de Estoque Inteligente na AWS com [SageMaker Canvas](https://aws.amazon.com/pt/sagemaker/canvas/)

Bem-vindo ao desafio de projeto "Previsão de Estoque Inteligente na AWS com SageMaker Canvas.

## 📋 Pré-requisitos

Antes de começar, certifique-se de ter uma conta na AWS. Se precisar de ajuda para criar sua conta, confira nosso repositório [AWS Cloud Quickstart](https://github.com/digitalinnovationone/aws-cloud-quickstart).

## 🎯 Objetivos Deste Desafio de Projeto (Lab)

![image](https://github.com/digitalinnovationone/lab-aws-sagemaker-canvas-estoque/assets/730492/72f5c21f-5562-491e-aa42-2885a3184650)

## 🚀 Passo a Passo - O que foi realizado nos testes.

### 1. Selecionar Dataset

-   Foi escolhido o upload do dataset (dataset-1000-com-preco-promocional-e-renovacao-estoque.csv) no SageMaker Canvas. O mesmo foi disponibilizado pela Dio, para treinar o modelo para previsão de esqtoque.

### 2. Construir/Treinar (BUILD)

-   Foi selecionado a coluna (QUANTIDADE_ESTOQUE) para prever.
-   Na configuração do tipo de modelo (Model Type), foi selecionado a coluna (ID_PRODUTO). E foi mantida a configuração padrão.
-   Para treinamento foi selecionado a opção Construção rápida (Quick Build), demorou em média 10 minutos.

### 3. Analisar (ANALYZE)

-   Após o treinamento, foi examinado as métricas de performance e ficaram com esses valores.
-   ### Resultado do Avg. wQL: 0.060.
-   Average Weighted Quantile Low Loss (Avg. wQL): Avalia a previsão como um todo, calculando a média da precisão em pontos de distribuição específicos chamados quantis para os quantis P10, P50 e P90. Um          valor menor indica um modelo mais preciso.
-   ### Resultado do MAPE: 0.148.
-   Mean Absolute Percent Error (MAPE): É o erro percentual (diferença percentual do valor médio previsto e real) calculado em média sobre todos os pontos de tempo. Um valor menor indica um modelo mais            preciso com MAPE=0 como um modelo perfeito sem erros.
-   ### Resultado do WAPE: 0.100.
-   Weighted Absolute Percent Error (WAPE): Mede o desvio geral dos valores previstos dos valores observados e é definido pela soma do erro absoluto normalizado pela soma da meta absoluta. Um valor menor          indica um modelo mais preciso com WAPE=0 como um modelo perfeito sem erros.
-   ### Resultado do RMSE: 5.765.
-   Root Mean Square Error (RMSE): É a raiz quadrada dos erros quadrados médios. Um RMSE menor indica um modelo mais preciso com RMSE=0 como um modelo perfeito sem erros.
-   ### Resultado do MASE: 0.301.
-   Mean Absolute Scaled Error (MASE): É a média do erro absoluto da previsão normalizada pelo erro absoluto médio de um método de previsão de linha de base simples. Um valor menor indica um modelo mais           preciso com MASE < 1 como um modelo estimado para ser melhor do que a linha de base e um MASE > 1 como um modelo estimado para ser pior do que a linha de base.

### 4. Prever (PREDICT)

-   Para o uso das pedições foi usada a opção SINGLE PREDICTION.
-   ### NO 1º TESTE FOI O PRODUTO 1003. DEMANDA HISTÓRICA: 59, 08/02/2024.
-   DATA: 09/02/2024 | P10 (PESSIMISTAS): 44.529 | P50 (NORMAIS): 48.299 | P90 (OTIMISTAS): 55.986 
-   ### NO 2º TESTE FOI O PRODUTO 1000. DEMANDA HISTÓRICA: 24, 08/02/2024.
-   DATA: 09/02/2024 | P10 (PESSIMISTAS): 10.316 | P50 (NORMAIS): 15.166 | P90 (OTIMISTAS): 20.894
-   ### NO 3º TESTE FOI O PRODUTO 1024. DEMANDA HISTÓRICA: 79, 08/02/2024.
-   DATA: 09/02/2024 | P10 (PESSIMISTAS): 61.623 | P50 (NORMAIS): 65.627 | P90 (OTIMISTAS): 71.093
