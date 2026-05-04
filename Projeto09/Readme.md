# Projeto: Extração de Insights de Comentários de Usuários

## 🚀 Sobre
Este projeto demonstra como empresas com presença digital podem extrair insights valiosos a partir de comentários de usuários sobre produtos, serviços, concorrentes e tendências de mercado.  
Os dados são **não estruturados** (texto livre), e por isso utilizamos um **Data Lake** para armazenamento bruto e o **MongoDB** como banco NoSQL para organizar e consultar os dados durante a análise.

## 🛠️ Tecnologias Utilizadas
- **Python** para manipulação e análise dos dados
- **Pandas / PySpark** para processamento em escala
- **NLTK / SpaCy / TextBlob** para NLP (processamento de linguagem natural)
- **MongoDB** para armazenamento e consultas flexíveis
- **Data Lake (Azure / AWS S3)** para dados brutos
- **Jupyter Notebook** para experimentação

## 📂 Estrutura do Projeto
- `/data` → Dados simulados de comentários
- `/notebook` → Scripts de experimentação
- `/insights` → Gráficos Demonstrativos

## ⚙️ Principais Comandos Utilizados
# 🔹 Resumo dos comandos utilizados no projeto

# 1. Agregações por categoria e tags
# cat_tags = posts.aggregate([...])
# -> Filtra posts com tags > 0, agrupa por categoria e conta quantos posts existem em cada.
# -> Usado para identificar quais categorias concentram mais posts com tags.

# 2. Conversão para DataFrame
# ct_df = pd.DataFrame(list(cat_tags))
# -> Transforma o cursor da agregação em um DataFrame Pandas para análise e visualização.

# 3. Agregações por imagens filtradas
# cat_fs = posts.aggregate([...])
# -> Filtra posts com "filteredPicture = True", agrupa por categoria e conta.
# -> Usado para ver quais categorias têm mais imagens filtradas.

# 4. Inicialização de campo
# datalake.posts.update_many({}, {'$set': {"length_of_des": 0}})
# -> Cria o campo "length_of_des" em todos os documentos, inicializando com 0.

# 5. Atualização do campo com tamanho real
# for data in posts.find({}):
#     posts.update_one({"_id": data['_id']}, {'$set': {'length_of_des': len(data['description'].split(' '))}})
# -> Calcula o número de palavras da descrição e atualiza o campo "length_of_des".

# 6. Agregações por descrições longas
# cat_des = posts.aggregate([...])
# -> Filtra posts com descrições >= 60 palavras, agrupa por categoria e conta.
# -> Usado para identificar categorias com descrições mais detalhadas.

# 7. Agregações por hora e categoria
# posts_hr = posts.aggregate([...])
# -> Agrupa posts por hora e categoria, contando quantos existem em cada combinação.
# -> Usado para analisar padrões de atividade ao longo do dia.

# 8. Conversão para DataFrame
# postshr_df = pd.DataFrame(list(posts_hr))
# -> Transforma o cursor em DataFrame Pandas.

# 9. Separação da coluna "_id"
# split_df = pd.DataFrame(postshr_df['_id'].to_list(), columns=['hour', 'category'])
# -> Divide a coluna "_id" (lista [hora, categoria]) em duas colunas distintas.

# 10. Junção dos dados finais
# df = pd.concat([split_df, postshr_df['count']], axis=1)
# -> Junta as colunas "hour", "category" e "count" em um DataFrame final.
# -> Esse formato é ideal para gráficos comparando quantidade de posts por hora e categoria.

