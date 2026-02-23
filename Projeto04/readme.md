# Projeto 04 - Análise de Dados para Campanhas de Marketing de Instituições Financeiras

## 📌 Descrição
Este projeto tem como objetivo realizar a análise exploratória e o tratamento de dados relacionados a campanhas de marketing de instituições financeiras.  
O trabalho envolveu desde a identificação de valores ausentes e inválidos até a geração de gráficos e exportação de um dataset final tratado.

---

## 🛠️ Etapas do Projeto

### 1. Tratamento da variável `salary`
- Problema identificado:
  - 26 registros com valor **0**.
  - 26 registros com valor **NaN**.
- Estatísticas:
  - Média: 57.008  
  - Mediana: 60.000  
  - Moda: 20.000
- Decisão:
  - Substituir valores **0** pela **mediana (60.000)** usando `replace()`.
  - Substituir valores **NaN** pela **mediana (60.000)** usando `fillna()`.
- Justificativa: a mediana é robusta contra outliers e representa melhor o centro da distribuição.

### 2. Diferença entre `replace()` e `fillna()`
- `replace(0, ...)` → corrige valores inválidos iguais a 0.  
- `fillna(...)` → corrige valores ausentes (NaN).  
- Ambos foram aplicados na coluna `salary`.

### 3. Tratamento da variável `response`
- Variável categórica binária: `"yes"` ou `"no"`.
- Moda: `"no"`.
- Decisão: imputar valores ausentes com `"no"`, mantendo a proporção real da base.

### 4. Tratamento da variável `month`
- Variável categórica (ex.: `"jan, 2017"`, `"feb, 2017"`).
- Não faz sentido usar média ou mediana.
- Decisão: imputar valores ausentes com a **moda** (`"may, 2017"`).

---

## 📊 Visualizações

### Scatter Plots
- **Saldo x Salário**:
```python
sns.scatterplot(x=df["balance"], y=df["salary"])
plt.title("Scatter Plot Entre Saldo e Salário")
plt.show()