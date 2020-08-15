# Projeto Wrangle_act - Nanodegree de Fundamentos de DataScience II - Udacity

## Introdução
O objetivo do projeto foi a análise de um conjunto de dados baseado nos arquivos de tweets do usuário do Twitter @dog_rates, também conhecido como WeRateDogs. WeRateDogs
é uma conta no Twitter que classifica os cães das pessoas com um comentário bem humorado sobre o cão.
O projeto foi subdividido em quatro etapas: coleta, avaliação, limpeza e análise. O resultado obtido por meio da análise foi a verificação de quais seriam as raças mais populares
entre os usuários da rede, buscando constatar a relação da incidência das raças com os tweets e retweets, utilizando essas variáveis, como as mais relevantes para a produção da informação
(raças mais populares).
### Instalação

Este projeto requer **Python 3.7** e as seguintes bibliotecas Python instaladas:

- [NumPy](http://www.numpy.org/)
- [Pandas](http://pandas.pydata.org/)
- [Matplotlib](http://matplotlib.org/)
- [scikit-learn](http://scikit-learn.org/stable/)
- [seaborn](https://seaborn.pydata.org/)



Você também precisará ter software instalado para rodar e executar um [iPython Notebook](http://ipython.org/notebook.html)

### Código

O código é fornecido no arquivo notebook `final_project_1.ipynb`. Você também precisará usar o o arquivo de dados `heart.csv` para executar o notebook. 

### Execução

Em um terminal ou janela de comando, navegue até o diretório raiz de projeto 'final_project_1.ipynb'/` (que contém este README) e execute os seguintes comandos:

```bash
ipython notebook final_project_1.ipynb
```  
ou
```bash
jupyter notebook final_project_1.ipynb
```

Isso abrirá o o software e arquivo de projeto iPython Notebook em seu navegador.

## Etapas

### Coleta
Nessa etapa foi realizada a coleta dos dados utilizando o arquivo 'twitter-archiveenhanced.csv' para utilização em um dataframe Pandas. Por meio da API Tweepy foram obtidos
dados de cada tweet para armazenamento em um arquivo chamado tweet_json.txt, onde guardamos os dados JSON de cada tweet.

### Avaliação
Após a coleta dos dados foi realizada a avaliação por meio de funções das bibliotecas pandas e numpy onde foram constatados os seguintes problemas abaixo transcritos:
#### Qualidade:
- No conjunto de dados tweet_archive existem nomes que provavelmente estão
equívocados ('a', 'the', 'an', ...);
- Em tweet_archive há entradas sem nome;
- Dados do tipo incorreto em tweet_archive (tweet_id, in_reply_to_status_id,
in_reply_to_user_id, retweeted_status_id, retweeted_status_user_id e timestamp);
- Em tweet_archive existem entradas incorretas envolvendo as colunas 'text' e
'rating_numerator';
- Em tweet_image existem tweets que não correspondem a fotos de cachorros;
- No conjunto tweet_image existem nomes em maiúsculo e minúsculo nas raças nas
colunas 'p1', 'p2' e p'3';
- Há dados nos conjuntos tweet_image e df_tweet do tipo incorreto;
- Existem dados de tweets e retweets (Só queremos classificações originais (não
retweets)).”
#### Arrumação:
- No conjunto tweet_archive as informações das colunas doggo, floofer, pupper e puppo
trazem informação qualitativa e exclusiva que pode ser representada em apenas uma
coluna;
- Os dados dos conjuntos tweet_archive, tweet_image e df_tweet podem formar um só
conjunto. Após unificar, excluir as entradas em que não há fotos.”

### Limpeza
Nesta etapa foi realizada a abordagem em cada um dos problemas acima indicados por meio das correções necessárias seguindo a sequência: definição, código e teste.

### Análise
Com o auxílio de visualizações geradas por meio das bibliotecas matplotlib e seaborn os dados limpos foram utilizados para produção de informação.
