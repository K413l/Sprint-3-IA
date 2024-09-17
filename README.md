# Sprint-3-IA
Sprint 3 IA

Previsão de Risco de Crédito com IA
Este repositório contém uma solução de IA para previsão de risco de crédito utilizando o modelo Random Forest. O projeto visa prever o risco de inadimplência de clientes, utilizando dados financeiros históricos de crédito. A implementação abrange desde o pré-processamento de dados até o treinamento e avaliação do modelo de machine learning.

Índice
Introdução
Metodologia
1. Carregamento dos Dados
2. Pré-processamento
3. Modelo
4. Avaliação
Como Usar
1. Requisitos
2. Instruções de Execução
Contribuição
Licença
Introdução
A previsão de risco de crédito é uma tarefa essencial em instituições financeiras para identificar clientes que possam ter dificuldades em honrar seus compromissos de crédito. Utilizando dados históricos, construímos um modelo de machine learning capaz de prever se um cliente é de alto risco ou baixo risco.

Metodologia
1. Carregamento dos Dados
Utilizamos o dataset German Credit Data, disponível no repositório de aprendizado de máquina da UCI. Este dataset contém 21 variáveis que representam características de clientes e sua classificação de risco de crédito (0 para baixo risco e 1 para alto risco).

URL do dataset: German Credit Data
2. Pré-processamento
Realizamos o pré-processamento dos dados, que incluiu:

Limpeza de dados: Verificação e tratamento de dados ausentes e inconsistências.
Normalização: Aplicação de escalonamento em variáveis numéricas (como idade e valor do crédito) para garantir que todas as features estejam na mesma escala.
Codificação de variáveis categóricas: Transformação de variáveis categóricas em numéricas utilizando One-Hot Encoding.
3. Modelo
O modelo escolhido foi o Random Forest, uma técnica que combina múltiplas árvores de decisão para melhorar a precisão e reduzir o overfitting.

Hiperparâmetros principais:
n_estimators: 100 (número de árvores)
random_state: 42 (para reprodutibilidade)
4. Avaliação
O modelo foi avaliado usando as seguintes métricas:

Acurácia: A porcentagem de previsões corretas.
Matriz de confusão: Para avaliar os falsos positivos e falsos negativos.
Relatório de Classificação: Métricas como precision, recall, e F1-score.
Exemplo de código usado para avaliação:

python
Copy code
from sklearn.metrics import accuracy_score, confusion_matrix, classification_report

# Previsão nos dados de teste
y_pred = model.predict(X_test)

# Avaliação do modelo
print("Accuracy:", accuracy_score(y_test, y_pred))
print(confusion_matrix(y_test, y_pred))
print(classification_report(y_test, y_pred))

# Como Usar
# 1. Requisitos

Certifique-se de ter os seguintes pacotes instalados:

Python 3.7+
Pandas
NumPy
Scikit-learn
Você pode instalar as dependências usando o seguinte comando:

pip install -r requirements.txt

# 2. Instruções de Execução

Clone este repositório:
git clone https://github.com/seuusuario/repositorio-previsao-credito.git

Navegue até o diretório do projeto:
cd repositorio-previsao-credito

Execute o script principal para treinar o modelo:
python main.py
