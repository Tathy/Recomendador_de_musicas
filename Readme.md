# :musical_note: Recomendador de músicas - Clusterização com K-Means

[Link do Google Colab](https://colab.research.google.com/drive/15bEzof9Zjm9bev_pLIhkR6JatkJ-vtix?usp=sharing)

**Sobre os Dados:** Retirados da [API do Spotify](https://developer.spotify.com/) e previamente tratados para utilização no curso pela instrutora [Sthe Monica](https://github.com/sthemonica). Os datasets utilizados não contêm mais todas as variáveis especificadas na API Web e foram coletados em 2020.

## Resumo

Foi utilizado o K-Means para aproveitar o conceito de distâncias dos clusters. Músicas consideradas mais parecidas terão distâncias menores entre si, isso definirá tanto o cluster que cada música está, quanto a ordem em que elas serão recomendadas para os usuários.

Sendo assim, a partir de uma música, encontra-se o cluster ao qual ela pertence e calcula-se a distância entre esta música e todas outras pertencentes ao mesmo cluster. As faixas são ordenadas da menor distância para a maior e a recomendação segue esta ordem.



## Tratamentos dos dados

Foram removidos dos datasets features que não eram diretamente relacionadas ao estilo musical ou que não precisavam ser avaliados na recomendação de músicas.



## Clusterização por gênero

A Clusterização foi feita agrupando os gêneros musicais em 5 clusters.

O modelo explicou cerca de 50% dos dados e 5 das 11 features originais no dataset de gêneros musicais.

![Clusterização por gênero musical](https://github.com/Tathy/Recomendador_de_musicas/blob/main/imgs/clustering_genres.png?raw=true)



## Clusterização por música

Uma segunda clusterização foi feita agrupando músicas em 50 clusters, de forma a explicar por volta de 70% do dataset.

![Clusterização por música](https://github.com/Tathy/Recomendador_de_musicas/blob/main/imgs/clustering_songs.png?raw=true)

![Clusterização por música 3D](https://github.com/Tathy/Recomendador_de_musicas/blob/main/imgs/clustering_songs_3d.png?raw=true)



### Exemplo de recomendação

É gerado uma playlist com as músicas recomendadas em ordem de semelhança, com o nome da música e o álbum ao qual pertence.

O exemplo abaixo foi gerado para a música "Ed Sheeran - Shape of You".

![Exemplo de recomendações](https://github.com/Tathy/Recomendador_de_musicas/blob/main/imgs/clustering_genres.png?raw=true)


## Referências

Este projeto foi feito com base em um curso da Alura, [Machine Learning: lidando com dados de muitas dimensões](https://cursos.alura.com.br/course/reducao-dimensionalidade).

O dataset também é o disponibilizado no curso.

[API do Spotify (track)](https://developer.spotify.com/documentation/web-api/reference/#/operations/get-track)
