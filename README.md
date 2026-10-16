# Detector de Falhas em Máquinas Industriais

Este projeto consiste em um modelo de Aprendizado de Máquina para prever e detectar falhas em equipamentos industriais com base em leituras de sensores[cite: 1].

## 📌 Visão Geral
O objetivo é identificar padrões nas variáveis operacionais das máquinas para prever falhas antes que elas ocorram, auxiliando na manutenção preventiva[cite: 1].

## 📊 Conjunto de Dados
O conjunto de dados utilizado (`dataset_sensores_industriais_200_registros.csv`) possui 200 registros e as seguintes colunas[cite: 1]:
- `temperatura`: Temperatura registrada no equipamento[cite: 1].
- `vibracao`: Nível de vibração medido pelos sensores[cite: 1].
- `pressao`: Pressão interna do sistema[cite: 1].
- `tempo_operacao`: Tempo contínuo de operação[cite: 1].
- `falha`: Variável alvo (0 = Operação Normal, 1 = Falha)[cite: 1].

## 🛠️ Etapas de Desenvolvimento

1. **Inspeção de Dados**:
   - Análise de estrutura, tipos de dados e detecção de duplicatas[cite: 1].
   - Identificação da distribuição das classes de falha[cite: 1].

2. **Tratamento de Dados Faltantes e Outliers**:
   - Imputação de valores nulos nas variáveis numéricas (`temperatura`, `vibracao` e `pressao`) utilizando a mediana[cite: 1].
   - Identificação de *outliers* pelo método da Amplitude Interquartil (IQR)[cite: 1].
   - Ajuste (*capping*) dos valores atípicos aos limites inferior e superior[cite: 1].

3. **Modelagem e Experimentos**:
   - Divisão do dataset em conjunto de treino e teste (50% / 50%)[cite: 1].
   - Aplicação e treinamento do algoritmo de **Árvore de Decisão** (`DecisionTreeClassifier`, `max_depth=5`)[cite: 1].
   - Avaliação e comparação de desempenho com e sem padronização de atributos via `StandardScaler`[cite: 1].

## 🚀 Resultados
- O modelo de **Árvore de Decisão** atingiu uma **acurácia de 94%** no conjunto de teste[cite: 1].

## 🧰 Tecnologias Utilizadas
- **Linguagem**: Python[cite: 1]
- **Manipulação de Dados**: Pandas, NumPy[cite: 1]
- **Visualização**: Matplotlib, Seaborn[cite: 1]
- **Machine Learning**: Scikit-Learn[cite: 1]

## 💻 Como Executar

1. Clone este repositório:
   ```bash
   git clone [https://github.com/](https://github.com/)
