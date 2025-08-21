# 🧠 Rede Neural - Classificação de Pacientes com Câncer  

## 👨‍💻 Integrantes  
- **Felipe Yabiko Nogueira** – RA: 22002265  
- **Henrique Ladeira Alves** – RA: 23016926  
- **Paulo Henrique** – RA: 22021948  
- **Yuri Rodrigues Viegas** – RA: 22021857  

---

## 📖 Descrição  
Este projeto implementa e avalia **modelos de aprendizado de máquina** para prever o **status de sobrevivência (SurvivalStatus)** de pacientes com câncer a partir de um conjunto de dados clínicos e demográficos sintéticos.  

A tarefa é de **classificação binária** (*Alive* ou *Deceased*), com ênfase no **Recall**, uma vez que em problemas médicos é fundamental reduzir ao máximo os falsos negativos.  

---

## ⚙️ Tecnologias Utilizadas  
- **Python 3**  
- **Google Colab**  
- **Bibliotecas principais**:  
  - `pandas`, `numpy`, `matplotlib`, `seaborn`  
  - `scikit-learn` (KNN, MLP, PCA, métricas)  
  - `kagglehub` (para download do dataset)  

---

## 📂 Etapas do Projeto  

1. **Carregamento dos Dados**  
   - Dataset: [China Cancer Patients (Synthetic) – Kaggle](https://www.kaggle.com/datasets/ak0212/china-cancer-patient-records).  

2. **Análise Exploratória (EDA)**  
   - Distribuição das classes alvo.  
   - Tratamento de valores ausentes.  
   - Visualização de correlações.  

3. **Pré-Processamento**  
   - Remoção de colunas irrelevantes.  
   - Codificação de variáveis categóricas (`OneHotEncoder`, `LabelEncoder`).  
   - Normalização com `StandardScaler`.  

4. **Redução de Dimensionalidade (PCA)**  
   - Avaliação da variância explicada acumulada.  
   - Definição de componentes para manter 95% da variância.  

5. **Treinamento de Modelos**  
   - **K-Nearest Neighbors (KNN)**  
   - **Multi-Layer Perceptron (MLP)**  
   - Ajuste de hiperparâmetros via **GridSearchCV** com validação cruzada.  

6. **Avaliação dos Modelos**  
   - Métricas: Accuracy, Precision, Recall, F1-Score, ROC-AUC.  
   - Matrizes de confusão e curvas ROC.  
   - Comparação com e sem PCA.  

---

## 📊 Resultados Principais  

- **Melhor modelo:** `MLP sem PCA`  
  - Accuracy: **77,1%**  
  - Recall: **77,1%**  
  - F1-Score: **79,0%**  
- O PCA reduziu de **53 → 42 variáveis**, mas **não trouxe ganhos significativos** em desempenho.  
- O **Recall** foi priorizado, garantindo maior sensibilidade para identificar casos de risco.  

---

## ▶️ Como Executar  

1. Clone este repositório:  
   ```bash
   git clone https://github.com/SEU_USUARIO/SEU_REPOSITORIO.git
   cd SEU_REPOSITORIO
