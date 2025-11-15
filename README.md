# 🚀 Projeto de Parceria Final: Análise Preditiva de Propensão de Compra

## 1. Tópico: Coleta de Dados e Pré-processamento

O projeto baseou-se na análise de propensão à compra de carros. O foco foi garantir a qualidade e a escala dos dados para otimizar os modelos de classificação.

* **Tratamento de Dados:** Removeu-se o ID do usuário e aplicou-se o **Label Encoder** para converter a variável 'Gender'.
* **Padronização (`StandardScaler`):** Esta técnica foi crucialmente aplicada às variáveis contínuas ('Age' e 'EstimatedSalary') para equalizar a escala e permitir que o SVM convergisse e funcionasse de maneira eficaz.

---

## 2. Tópico: Modelagem Preditiva

Avaliamos três modelos-chave, com foco em otimizar o desempenho na previsão de intenção de compra (`Purchased`).

### Comparação de Performance (Acurácia)

| Modelo | Kernel/Otimização | Acurácia (Métrica Final) |
| :--- | :--- | :--- |
| **SVM** | Kernel Linear | **0.8750** |
| **SVM** | Kernel Polinomial (Poly) | **0.9250** |
| **XGBoost** | Otimizado (Tarefa Anterior) | **0.9100** |

---

## 3. Tópico: Conclusões e Resultados Finais

### 3.1. Visualização de Dados (Matriz de Confusão)

[INSIRA AQUI A IMAGEM DA MATRIZ DE CONFUSÃO]
*A Matriz de Confusão do modelo SVM Polinomial demonstra a alta precisão do modelo, com uma taxa de acerto de 92.5%, validando a eficácia da padronização e do kernel não-linear para esta base.*

### 3.2. Conclusão Final

O modelo que demonstrou o **melhor desempenho geral** foi o **SVM com Kernel Polinomial**, com uma acurácia de **$0.9250$**.

A chave para o sucesso do SVM foi a **Padronização dos Dados** (Etapa 4.5), que permitiu que o **Kernel Polinomial** superasse os modelos de *ensemble* (XGBoost) para esta tarefa.

### 3.3. Duelo de Modelos (Experiência em Competição)
A experiência em otimização de modelos foi consolidada com o desafio do Titanic, onde o modelo XGBoost Otimizado alcançou um score de **$0.53588$**.