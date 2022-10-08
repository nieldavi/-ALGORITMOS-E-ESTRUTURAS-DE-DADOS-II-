# The Reddit Climate Change Dataset
:mortar_board:
Esse projeto consiste numa adpatação do projeto guaido da plataforma DataQuest `Building Fast Queries on a CSV`. Foi utilizado o projeto 
`The Reddit Climate Change`.
Além disso, esse trabalho tem como colaboradores:
* :construction_worker: Francsico Daniel Davi
* :construction_worker: Luiz Henrique Araújo Dantas 
---
Para implementação do projeto foi criado 3 funções principais:
## Função 1: Encontrando id 
Existe umas versão para essa função. A primeira versão é `get_row_id_search` e  percorre todos as linhas do dataset até encontrar o id desejado. Já a segunda versão é a `get_row_in_dic`, na qual usa a estrutura dicionário para  procurar o id. As duas funções retornam a linha na qual o id foi passado com parametro.

## Função 2: Encontrando linha a partir da coluna sentiment
Para essa segunda função, a `find_sentiment`, usamos uma função auxiliar `mensagem_range`que retorna o indece da linha partir de um valor de sentiment, para comportor na função principal. A função `find_sentiment` tem como parametro um limite superior e inferior e retorna as linhas entre os valores passados.

## Função 3: Encontrando somas de scores 
A terceira função também tem duas versões. A função `sum_sentiments`, dado um valor alvo percore todo o dataset até encontrar um valor que dado dois scores seja igual a s suam soma. 
Já função `sum_sentiments_in_dic` utiliza a estrtura de um dicionário para obter o mesmo resultado mais de forma mais ágil.

## Referências
* [Building Fast Queries on a CSV](https://github.com/dataquestio/solutions/blob/master/Mission481Solution.ipynb).
* [The Reddit Climate Change Dataset](https://www.kaggle.com/datasets/pavellexyr/the-reddit-climate-change-dataset).
