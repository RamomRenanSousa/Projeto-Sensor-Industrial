# Detector de Falhas em Máquinas Industriais

Este projeto consiste em um modelo de Aprendizado de Máquina para prever e detectar falhas em equipamentos industriais com base em leituras de sensores.

## 📌 Visão Geral
O objetivo é identificar padrões nas variáveis operacionais das máquinas para prever falhas antes que elas ocorram, auxiliando na manutenção preventiva.

## 📊 Conjunto de Dados
O conjunto de dados utilizado (`dataset_sensores_industriais_200_registros.csv`) possui 200 registros e as seguintes colunas:
- `temperatura`: Temperatura registrada no equipamento.
- `vibracao`: Nível de vibração medido pelos sensores.
- `pressao`: Pressão interna do sistema.
- `tempo_operacao`: Tempo contínuo de operação.
- `falha`: Variável alvo (0 = Operação Normal, 1 = Falha).

## 🛠️ Etapas de Desenvolvimento

1. **Inspeção de Dados**:
   - Análise de estrutura, tipos de dados e verificação de duplicatas.
   - Identificação da distribuição das classes de falha.

2. **Tratamento de Dados Faltantes e Outliers**:
   - Imputação de valores nulos nas variáveis numéricas (`temperatura`, `vibracao` e `pressao`) utilizando a mediana.
   - Identificação de *outliers* pelo método da Amplitude Interquartil (IQR).
   - Ajuste (*capping*) dos valores atípicos aos limites inferior e superior.

3. **Modelagem e Experimentos**:
   - Divisão do dataset em conjunto de treino e teste (50% / 50%).
   - Aplicação e treinamento do algoritmo de **Árvore de Decisão** (`DecisionTreeClassifier`, `max_depth=5`).
   - Avaliação e comparação de desempenho com e sem padronização de atributos via `StandardScaler`.

## 🚀 Resultados
- O modelo de **Árvore de Decisão** atingiu uma **acurácia de 94%** no conjunto de teste.

## 🧰 Tecnologias Utilizadas
- **Linguagem**: Python
- **Manipulação de Dados**: Pandas, NumPy
- **Visualização**: Matplotlib, Seaborn
- **Machine Learning**: Scikit-Learn

## 💻 Como Executar

1. Clone este repositório:
   ```bash
   git clone [https://github.com/seu-usuario/seu-repositorio.git](https://github.com/seu-usuario/seu-repositorio.git)
   git clone [https://github.com/](https://github.com/)
