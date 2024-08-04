# 📊 Previsão de Estoque Inteligente na AWS com [SageMaker Canvas](https://aws.amazon.com/pt/sagemaker/canvas/)

Bem-vindo ao desafio de projeto "Previsão de Estoque Inteligente na AWS com SageMaker Canvas.

## 📋 Pré-requisitos

Antes de começar, certifique-se de ter uma conta na AWS. Se precisar de ajuda para criar sua conta, confira nosso repositório [AWS Cloud Quickstart](https://github.com/digitalinnovationone/aws-cloud-quickstart).

## 🎯 Objetivos Deste Desafio de Projeto (Lab)

![image](https://github.com/digitalinnovationone/lab-aws-sagemaker-canvas-estoque/assets/730492/72f5c21f-5562-491e-aa42-2885a3184650)

## 🚀 Passo a Passo

### 1. Selecionar Dataset

-   Foi escolhido o upload do dataset (dataset-1000-com-preco-promocional-e-renovacao-estoque.csv) no SageMaker Canvas. O mesmo foi disponibilizado pela Dio, para treinar o modelo para previsão de esqtoque.

### 2. Construir/Treinar

-   Foi selecionado a coluna (QUANTIDADE_ESTOQUE) para prever.
-   Na configuração do tipo de modelo (Model Type), foi selecionado a coluna (ID_PRODUTO). E foi mantida a configuração padrão.
-   Para treinamento foi selecionado a opção Construção rápida (Quick Build), demorou em média 10 minutos.

### 3. Analisar

-   Após o treinamento, foi examinado as métricas de performance e ficaram com esses valores. (Avg. wQL: 0.060 | MAPE: 0.148 | WAPE: 0.100 | RMSE: 5.765 | MASE: 0.301)
-   LEGENDA:
-   Average Weighted Quantile Low Loss (Avg. wQL) avalia a previsão como um todo, calculando a média da precisão em pontos de distribuição específicos chamados quantis para os quantis P10, P50 e P90. Um valor menor indica um modelo mais preciso.
-   Mean Absolute Percent Error (MAPE) é o erro percentual (diferença percentual do valor médio previsto e real) calculado em média sobre todos os pontos de tempo. Um valor menor indica um modelo mais preciso com MAPE=0 como um modelo perfeito sem erros. 
-   //PAREI AQUI
-   Verifique as principais características que influenciam as previsões.
-   Faça ajustes no modelo se necessário e re-treine até obter um desempenho satisfatório.

### 4. Prever

-   Use o modelo treinado para fazer previsões de estoque.
-   Exporte os resultados e analise as previsões geradas.
-   Documente suas conclusões e qualquer insight obtido a partir das previsões.

## 🤔 Dúvidas?

Esperamos que esta experiência tenha sido enriquecedora e que você tenha aprendido mais sobre Machine Learning aplicado a problemas reais. Se tiver alguma dúvida, não hesite em abrir uma issue neste repositório ou entrar em contato com a equipe da DIO.
