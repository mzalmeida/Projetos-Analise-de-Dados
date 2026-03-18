# Projeto 06 - Market Basket Analysis 🛒

## 📌 Descrição
Este projeto tem como objetivo aplicar **Market Basket Analysis** utilizando o algoritmo **Apriori** para identificar padrões de compra e regras de associação entre produtos.  
A análise permite descobrir quais itens são frequentemente comprados juntos, fornecendo insights valiosos para estratégias de marketing, promoções cruzadas e recomendações de produtos.

---

## ⚙️ Tecnologias Utilizadas
- **Python 3.x**
- **Pandas** para manipulação de dados
- **Apriori Algorithm** para mineração de regras de associação
- **Datetime** para medir tempo de execução
- **Jupyter Notebook ** (ambiente de desenvolvimento)

---

## 📂 Estrutura do Projeto
- **Pré-processamento dos dados**  
  - Criação de transações no formato adequado para o Apriori.
  - Conversão para tuplas e DataFrames.

- **Execução do Apriori**  
  - Definição de parâmetros como `min_support` e `min_confidence`.
  - Geração de itemsets frequentes e regras de associação.

- **Cálculo das métricas**  
  - Suporte (Support)  
  - Confiança (Confidence)  
  - Lift  

- **Construção de DataFrames finais**  
  - Organização das regras com nomes dos produtos.  
  - Ordenação por métricas (Confidence e Lift).  
  - Seleção das regras mais relevantes (Top 10).

---

## 📊 Principais Resultados
- Identificação de pares de produtos com maior **confiança** (probabilidade de compra conjunta).  
- Identificação de pares com maior **lift** (associações estatisticamente mais fortes).  
- Criação de tabelas organizadas para análise e interpretação dos resultados.  

Exemplo de métricas calculadas:
- **Support_A**: proporção de transações que contêm o produto A.  
- **Support_B**: proporção de transações que contêm o produto B.  
- **Support_AB**: proporção de transações que contêm A e B juntos.  
- **Confidence_AB**: probabilidade de encontrar B dado que A está presente.  
- **Lift_AB**: força da associação entre A e B.  

---

📈 Aplicações Práticas- Recomendações de produtos: "Clientes que compram X também compram Y".
- Promoções cruzadas: Combinar produtos frequentemente comprados juntos.
- Layout de loja: Organização estratégica de prateleiras.
👨‍💻 AutorProjeto desenvolvido por Mateus como parte do Projeto 06 - Market Basket Analysis.