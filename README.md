Projeto OdontoPrev - Detecção de Padrões Comportamentais
Descrição
Este projeto tem como objetivo identificar padrões comportamentais dos beneficiários da OdontoPrev para melhorar o atendimento e reduzir custos relacionados a sinistros odontológicos. A análise baseia-se em dados simulados enriquecidos, utilizando técnicas de machine learning para classificar o risco de sinistro dos pacientes.

Evolução do Projeto
Versão Inicial
Dados simples com poucas variáveis (Paciente_ID, Historico_Tratamento, Faltas).

Modelo RandomForest treinado apenas com a variável Faltas.

Avaliação básica com relatório de classificação e matriz de confusão textual.

Classificação de risco simples baseada na probabilidade predita.

Melhorias e Evoluções Implementadas
Dados enriquecidos e realistas:

Inclusão de novas variáveis como Idade, Sexo, Frequencia_Consultas e Tipo_Plano.

Simulação da variável alvo Sinistro baseada em regras lógicas que refletem situações reais.

Análise exploratória aprimorada:

Visualizações para distribuição das classes e relação entre variáveis e sinistro (boxplots, countplots).

Pré-processamento robusto:

Codificação One-Hot para variáveis categóricas.

Escalonamento (StandardScaler) para variáveis numéricas.

Uso de ColumnTransformer para pipeline modular e limpa.

Tratamento de desequilíbrio de classes:

Aplicação do SMOTE para gerar amostras sintéticas da classe minoritária (sinistro) no conjunto de treino.

Avaliação avançada do modelo:

Matriz de confusão plotada com heatmap.

Curva ROC com cálculo da AUC para avaliar o desempenho.

Importância das features plotada para interpretar o modelo.

Classificação detalhada do risco:

Classificação em níveis: Baixo Risco, Risco Moderado e Alto Risco, com base na probabilidade predita.

Comparação com rede neural:

Implementação de rede neural simples com TensorFlow/Keras para comparar desempenho.

Avaliação similar (relatório, matriz de confusão, curva ROC, gráficos de treinamento).

Tecnologias e Bibliotecas Utilizadas
Python 3.8+

Pandas para manipulação de dados

NumPy para geração de dados e operações numéricas

Matplotlib e Seaborn para visualização de dados

Scikit-learn para machine learning:

Pré-processamento (OneHotEncoder, StandardScaler, ColumnTransformer)

Modelos (RandomForestClassifier)

Métricas e avaliação (classification_report, confusion_matrix, roc_curve, auc)

Imbalanced-learn (imblearn) para tratamento de desequilíbrio com SMOTE

TensorFlow/Keras para construção e treinamento da rede neural

Como Usar
Preparar o ambiente:

Instale as bibliotecas necessárias:

bash
Copiar
pip install pandas numpy matplotlib seaborn scikit-learn imbalanced-learn tensorflow
Executar o notebook ou script:

Gere os dados simulados enriquecidos.

Faça a análise exploratória.

Execute o pré-processamento e treinamento do modelo RandomForest com SMOTE.

Avalie e visualize os resultados.

Treine e avalie a rede neural para comparação.

Interpretar os resultados:

Observe as métricas de desempenho (accuracy, precision, recall, F1-score, AUC).

Analise as importâncias das features para entender os drivers do risco.

Use a classificação de risco para segmentar pacientes.

Estrutura do Código
Geração de dados: Cria dados com múltiplas variáveis e uma regra para simular Sinistro.

Análise exploratória: Gráficos para entender a distribuição e relações.

Pré-processamento: Pipeline com codificação e escalonamento.

Balanceamento: SMOTE aplicado no conjunto de treino.

Modelagem: Treinamento de RandomForest e rede neural.

Avaliação: Métricas, matriz de confusão, curva ROC, importância de features.

Classificação de risco: Probabilidades convertidas em categorias.

Possíveis Extensões
Implementar interface interativa com Streamlit ou Jupyter Widgets.

Testar outros algoritmos, como Gradient Boosting.

Usar dados reais para validação prática.

Implementar pipeline de deploy para uso em ambiente de produção.
