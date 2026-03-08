# 🚗 Previsão de Preço de Venda de Veículos

## 📌 Descrição
Este projeto tem como objetivo prever o **preço de venda de veículos** a partir de suas características, utilizando **Regressão Linear** com a biblioteca **scikit-learn**.  
Ele transforma dados brutos em uma matriz adequada para o modelo, aplica pré-processamento em variáveis categóricas, treina diferentes versões de modelos e avalia o desempenho.  

---

## ⚙️ Funcionalidades
- Separação de variáveis independentes (Modelo, Quilometragem, Idade_Veiculo) e variável alvo (Preco_Venda).
- Pré-processamento de dados categóricos com **OneHotEncoder**.
- Treinamento de modelos de regressão linear.
- Avaliação de desempenho com o coeficiente de determinação **R²**.
- Previsão de preços de venda para novos veículos.
- Persistência do modelo treinado com **joblib** para reutilização futura.

---

## 🛠️ Tecnologias e Bibliotecas Utilizadas
- **Python 3.x**
- **pandas** → manipulação e organização dos dados.
- **scikit-learn** → criação e treinamento dos modelos de regressão linear.
  - `LinearRegression`
  - `ColumnTransformer`
  - `OneHotEncoder`
- **joblib** → salvar e carregar modelos treinados.
- **Jupyter Notebook** → ambiente de desenvolvimento e documentação.

---

## 📊 Estratégias Utilizadas
1. **Organização dos dados**  
   - Separação entre variáveis independentes (`x`) e variável alvo (`y`).

2. **Pré-processamento**  
   - Transformação da coluna categórica "Modelo" em variáveis binárias (dummies) com `OneHotEncoder`.

3. **Treinamento de modelos**  
   - Criação de diferentes versões de regressão linear:
     - Modelos simples com variáveis numéricas.
     - Modelos expandidos com variáveis categóricas transformadas.

4. **Avaliação de desempenho**  
   - Uso do coeficiente de determinação **R²** para medir a qualidade do ajuste.

5. **Previsões**  
   - Estimativa do preço de venda de veículos com base em suas características.

6. **Persistência do modelo**  
   - Salvamento do modelo treinado em arquivo `.pkl` com `joblib.dump`.
   - Carregamento posterior com `joblib.load`.

---

📈 Exemplo de Uso
Previsão de preço para um carro do segundo modelo, com 86.000 km rodados e 7 anos de uso:

---

🎯 Motivação
Este projeto mostra como aplicar Machine Learning em um problema prático:
- Automatizar a avaliação de veículos.
- Oferecer preços justos e consistentes.
- Escalar análises para milhares de registros.
- Servir como base para sistemas mais complexos de precificação.

---

📂 Estrutura do Projeto
├── modelo/                  # Pasta onde o modelo treinado é salvo
│   └── modelo_treinado.pkl
├── notebook.ipynb           # Jupyter Notebook com todo o código
├── README.md                # Documentação do projeto



✅ Conclusão
Este projeto demonstra como dados categóricos e numéricos podem ser combinados em um modelo de regressão linear para prever preços de veículos.
Ele é um exemplo prático de como estatística e machine learning podem ser aplicados para resolver problemas reais de mercado.

---


   