# Classificação de Clientes Inadimplentes em Empréstimos de Automóveis

Este projeto tem como objetivo construir um modelo de **classificação binária** para prever se um cliente se tornará **inadimplente** em um contrato de empréstimo de automóvel. Foram utilizadas técnicas de **aprendizado de máquina supervisionado**, além de estratégias de **validação, métricas de avaliação** e **balanceamento de dados**.

## 📁 Dados Utilizados

- Dataset disponível no GitHub: [`emp_automovel.csv`](https://raw.githubusercontent.com/TheGabrielVieira/validacao-modelos-metricas-de-avalia--o/refs/heads/main/data/emp_automovel.csv)
- A variável alvo é `inadimplente` (0 = adimplente, 1 = inadimplente)

---

## 📌 Tecnologias e Bibliotecas

- Python 3.11+
- [pandas](https://pandas.pydata.org/)
- [scikit-learn](https://scikit-learn.org/stable/)
- [imbalanced-learn (imblearn)](https://imbalanced-learn.org/)
- [matplotlib](https://matplotlib.org/) (para visualizações)
- Jupyter Notebook (opcional, mas recomendado)

---

## ⚙️ Instalação e Execução

1. **Clone este repositório:**
   ```bash
   git clone https://github.com/seu-usuario/seu-repositorio.git
   cd seu-repositorio
   ```

2. **Crie um ambiente virtual (recomendado):**
   ```bash
   python -m venv venv
   source venv/bin/activate  # no Windows: venv\Scripts\activate
   ```

3. **Instale as dependências:**
   ```bash
   pip install -r requirements.txt
   ```

4. **Execute o projeto:**
   - Você pode abrir o notebook Jupyter no VSCode ou Jupyter Lab:
     ```bash
     jupyter notebook
     ```

---

## 🧠 Etapas do Projeto

1. Leitura e visualização dos dados
2. Treinamento de modelo inicial com `DecisionTreeClassifier`
3. Separação entre treino, validação e teste
4. Avaliação com métricas:
   - Acurácia
   - Precisão
   - Recall
   - F1-Score
   - Matriz de confusão
   - Curva ROC e AUC
   - Curva Precision x Recall
5. Validação cruzada com `KFold` e `StratifiedKFold`
6. Cálculo de intervalo de confiança para as métricas
7. Balanceamento dos dados:
   - Oversampling com `SMOTE`
   - Undersampling com `NearMiss`
   - Pipeline com `imblearn.pipeline`
8. Avaliação final no conjunto de teste

---

## 📊 Resultados e Considerações

- O projeto prioriza **Recall** como métrica principal, dado o problema de inadimplência (foco em **detectar corretamente os inadimplentes**).
- O uso de técnicas de balanceamento ajudou a lidar com o desbalanceamento da base.
- A Validação Cruzada e o cálculo de **intervalo de confiança** aumentam a robustez da avaliação do modelo.

---

## ✅ Requisitos

Veja o arquivo [`requirements.txt`](./requirements.txt) para a lista completa de dependências. As principais são:

```
scikit-learn==1.5.2
imbalanced-learn==0.12.3
pandas
matplotlib
```

---

## 📌 Observações

- Este projeto pode ser expandido com outras técnicas de modelagem (como Random Forest, XGBoost).
- Pode-se usar GridSearchCV para ajuste de hiperparâmetros no pipeline.

---

## 📬 Contato

Caso tenha dúvidas ou sugestões, sinta-se à vontade para abrir uma _issue_ ou entrar em contato comigo pelo GitHub.
