Previsão de Resultados de Partidas de Futebol - Série A do Brasil
📌 Visão Geral

Este projeto utiliza Machine Learning para prever os resultados de partidas da Série A do Campeonato Brasileiro (dados de 2012 em diante). Foram testados diferentes algoritmos de classificação para determinar se uma partida terminará em vitória do time da casa (H), empate (D) ou vitória do time visitante (A).
📊 Dados Utilizados

O dataset contém informações sobre:

    Resultados (H, D, A)

    Número de gols (HG = Home Goals, AG = Away Goals)

    Odds de apostas (PSCH, PSCD, PSCA)

    Médias e máximos de odds (AvgCH, AvgCD, AvgCA, MaxCH, MaxCD, MaxCA)

Tratamento dos dados:

    Substituição de valores nulos por 0

    Codificação da coluna Res (H=1, D=0, A=2)

    Seleção das melhores features usando SelectKBest

    Normalização com MinMaxScaler

🤖 Modelos Testados

Foram avaliados os seguintes algoritmos:
1. Regressão Logística (Multinomial)

    Acurácia: 63.66%

    F1-Score (macro): 48.67%

    Melhor parâmetro: C=0.1

2. Support Vector Classifier (SVC)

    Acurácia: 63.46%

    F1-Score (micro): 63.46%

    Melhor parâmetro: C=10

3. Decision Tree (Otimizada com GridSearchCV)

    Acurácia: 57.19%

    F1-Score (micro): 57.19%

    Melhores parâmetros:

        max_depth=80

        max_features=3

        min_samples_leaf=5

        min_samples_split=8

4. Naive Bayes (GaussianNB)

    Acurácia: 55.87%

    F1-Score (micro): 55.87%

📌 Conclusões

✅ O melhor modelo foi o SVC, com 63.46% de acurácia.
✅ Vitórias em casa (H) foram mais fáceis de prever (48.38% dos casos).
🔍 Acurácia próxima de 63-64% indica que o modelo tem um desempenho razoável, mas pode ser melhorado com:

    Mais features (estatísticas dos times, escalações, etc.)

    Técnicas de ensemble (Random Forest, XGBoost)

    Dados mais recentes e completos

🔧 Tecnologias Utilizadas

    Python (Pandas, NumPy, Matplotlib, Seaborn)

    Scikit-learn (LogisticRegression, SVC, DecisionTree, GaussianNB, GridSearchCV)

    Jupyter Notebook (Análise e Visualização)

📂 Estrutura do Projeto
Copy

/projeto-futebol-prediction/  
├── data/  
│   └── BRA.csv (dados das partidas)  
├── models/  
│   └── (modelos treinados)  
├── analysis.ipynb (Jupyter Notebook com o código)  
└── README.md (este arquivo)  

🚀 Próximos Passos

    Testar Redes Neurais ou XGBoost

    Adicionar dados em tempo real (API de futebol)

    Desenvolver uma aplicação web para previsões

🔗 Repositório: GitHub
✉️ Contato: [seu-email@exemplo.com]

📅 Última atualização: Março 2024

Esse README fornece uma visão geral do projeto, destacando metodologia, resultados e possíveis melhorias. Adapte conforme necessário! ⚽📊
