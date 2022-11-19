UNIVERSIDADE FEDERAL DO RIO GRANDE DO NORTE - UFRN

DCA0209 - ALGORITMOS E ESTRUTURA DE DADOS II

Trabalho 02 - Unidade 02

Componentes do grupo:

* Francisco Daniel Davi
* Luiz Henrique Araújo Dantas

Neste repositório estaremos abordando uma prática realizada na disciplina de Algoritmos e Estrutura de Dados II (DCA0209), disciplina do Curso de Engenharia de Computação da Universidade Federal do Rio Grande do Norte, por orientação do professor Ivanovitch Medeiros Dantas da Silva.

O problema que estamos tratando se refere à malha áerea brasileira, tomando de base o repositório e o dataset disponibilizado no link do Github de Alvaro F. P. P.<https://github.com/alvarofpp/dataset-flights-brazil>, podemos realizar uma análise pertinente à assortatividade, graus de vértice entre vizinhos, clustering e simular alguns cenários de voos entre alguns aeroportos do país, que iremos mostrar logo mais.

Para realizar esse projeto temos que utilizar as seguintes bibliotecas: NetworkX, nxivz, matplotlib, pandas e seaborn.

Iremos realizar uma modificação no dataset que é a inserção de mais uma linha de código referente à região do país, para que possamos identificar a região do país que o aeroporto pertence.

Todas as imagens geradas nessa analise estão disponíveis na pasta sample date para donwload. 

Então vamos lá

#  1-Assortividade 

A primeira analise feita no dataset foi a da assortividade da rede estuda com o objetivo de entender como os nós estão conectados entre si agrupados pelas regiões brasileiras. Para facilitar nosso entendimento plotamos o grafico baixo. 



![Alt text](https://github.com/nieldavi/ALGORITMOS-E-ESTRUTURAS-DE-DADOS-II/blob/main/week%2010/sample%20data/assortividade.png)

Além disso, calculou-se o coeficiente de assotividade dado um nó obtendo um valor de `0,367` e a matriz de coenficiente por região que está no arquivo notebook. Essa essa informações podemos afirmar que a rede é assortiva, ou seja tende a interir com os mesmo nós.

# Assortividade de Degree

A próxima analise feita foi a entre o grau e o números de vizinhos. Em rede nós com alto grau tendem a se conectar com nós de alto grau  e graus de baixo nó graus tendem a se concetar com  nós de baixo grau, essa caracteristacas são chamada de rede sortiva e rede de dissortativa respectivamente. Além disso plotamos os gráficos abaixo:

![Alt text](https://github.com/nieldavi/ALGORITMOS-E-ESTRUTURAS-DE-DADOS-II/blob/main/week%2010/sample%20data/download.png)

## Degree Norte
![Alt text](https://github.com/nieldavi/ALGORITMOS-E-ESTRUTURAS-DE-DADOS-II/blob/main/week%2010/sample%20data/NORTE_degree_assortativity.png)


## Degree Nodeste
![Alt text](https://github.com/nieldavi/ALGORITMOS-E-ESTRUTURAS-DE-DADOS-II/blob/main/week%2010/sample%20data/NORDESTE_degree_assortativity.png)

## Degree Sul
![Alt text](https://github.com/nieldavi/ALGORITMOS-E-ESTRUTURAS-DE-DADOS-II/blob/main/week%2010/sample%20data/SUL_degree_assortativity.png)
## Degree Sudeste
![Alt text](https://github.com/nieldavi/ALGORITMOS-E-ESTRUTURAS-DE-DADOS-II/blob/main/week%2010/sample%20data/SUDESTE_degree_assortativity.png)
## Degree Centro-Oeste
![Alt text](https://github.com/nieldavi/ALGORITMOS-E-ESTRUTURAS-DE-DADOS-II/blob/main/week%2010/sample%20data/CENTRO-OESTE_degree_assortativity.png)

# Componentes conectados
Agora  vamos obsevar como os componentes estão conectados dentro da rede trafego aerea brasileir. Nosso primeiro passo para essa análise é verificar os componentes conectados e foram obtidos 5 componentes. 

Apos isso, fizemos uma função para extrair os componentes do dataset e depois extraimos as quantidade de componentes por reginão do brasil em forma de porcentagem obtendo os seguintes valores:
`Norte: 25.6619%`

`Nordeste: 18.7373%`

`Sul: 14.2566%`

`Sudeste: 23.4216%`

`Centro-Oeste: 17.9226%`

# Cenários simulados

Agora vamos simular as viagens nos destinho do dataset entre as regiões do pais. Logo, as viagens simuladas serão as seguintes:
* Cidade no Norte (1) e uma cidade no Sul (2)
* Cidade no Sul (2) e uma cidade no Nordeste (3)
* Cidade no Nordeste (3) e uma cidade no Centro-Oeste (4)
* Cidade no Centro-Oeste (4) e uma cidade no Sudeste (5


Para analizar o caminho mais curto para chegar ao destino, utilizaremos a função `nx.shortest_path()`, que nos auxiliará mostrando o nome de cada um dos aeroportos que será visitado durante a viagem.
Nossos resultados foram o seguintes:
 * As cidades de Manaus e Porto Alegre não são cidades que estão na mesma região mas que podem ser visitadas a partir de um único voo.
 * As cidades de Porto Alegre e São Gonçalo do Amarante não são cidades que estão na mesma região mas que podem ser visitadas a partir de um único voo.
 * Saindo de São Gonçalo do Amarante/RN para Dourados/MS, temos que fazer uma conexão no aeroporto de Confins. O aeroporto SBCF está localizado no estado de Minas Gerais, na região Sudeste, para ir do SBSG para o SBDO temos que fazer uma conexão nesse aeroporto, abaixo estão alguns detalhes da localização do aeroporto.
* Partindo de Dourados/MS para o Rio de Janeiro/RJ, notamos que o voo passa pelo aeroporto de Confins, também na região sudeste, para poder chegar ao seu destino final.

# Coeficiente de Clusterização

Por fim, para essa análise fizemos para o  dataset total e para cada região do pais. Para o dataset total utilizamos o seguinte código:
`nx.average_clustering(G_br)`

E utlizando o mesmo principio para as regiões do Brasil, obtemos os seguintes coeficientes:

`Norte: 0.6159`

`Sul: 0.5979`

`Nordeste: 0.4380 `

`Sudeste: 0.6186 `

`Centro-Oeste: 0.5618 `

Portanto, podemos afirmar que, aregião nordeste possui o menor índice de clusterização dentre todas as outras regiões, podemos afirmar que, como ela está mais próximo do valor 0, a sua organização da malha aérea se aproxima da topologia estrela.
