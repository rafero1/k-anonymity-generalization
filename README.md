# K-Anonimato com Generalização
O objetivo do projeto é realizar a anonimização do dataset de entrada ([Dataset_Covid_CE.csv](Dataset_Covid_CE)) usando um algoritmo k-anonimato com técnica de generalização de valores. 4 versões anonimizadas do dataset foram geradas, para cada valor de k em k = {2, 4, 8, 16}. No final, alguns gráficos foram plotados para ajudar a visualizar a diferença entre os datasets anonimizados para o original.

O projeto foi realizado em python, no ambiente jupyter notebook, e com ajuda das bibliotecas pandas, re, plotnine e matplotlib.

#### Funcionamento:

1. agrupar registros pelos semi-identificadores
1. realizar generalização dos atributos de grupos com tamanho < k
    1. atributos são generalizados com base na quantidade de valores únicos, de maior para o menor
1. repetir até possuir < k número de registros não-anonimados
1. puxar dos registros já anonimados k - n registros para novamente realizar generalização, até todo grupo formado possuir tamanho >= k