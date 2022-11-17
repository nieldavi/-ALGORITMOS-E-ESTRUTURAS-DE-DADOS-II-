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
![Alt text](https://github.com/nieldavi/ALGORITMOS-E-ESTRUTURAS-DE-DADOS  II/blob/main/week%2010/sample%20data/NORTE_degree_assortativity.png)

## Degree Nodeste
![Alt text](https://github.com/nieldavi/ALGORITMOS-E-ESTRUTURAS-DE-DADOS-II/blob/main/week%2010/sample%20data/NORDESTE_degree_assortativity.png)

## Degree Sul
![Alt text](https://github.com/nieldavi/ALGORITMOS-E-ESTRUTURAS-DE-DADOS-II/blob/main/week%2010/sample%20data/SUL_degree_assortativity.png)
## Degree Sudeste
![Alt text](https://github.com/nieldavi/ALGORITMOS-E-ESTRUTURAS-DE-DADOS-II/blob/main/week%2010/sample%20data/SUDESTE_degree_assortativity.png)
## Degree Centro-Oeste
![Alt text](https://github.com/nieldavi/ALGORITMOS-E-ESTRUTURAS-DE-DADOS-II/blob/main/week%2010/sample%20data/CENTRO-OESTE_degree_assortativity.png)

