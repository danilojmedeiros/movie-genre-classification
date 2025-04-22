# Classificação Multi-label de Gêneros de Filmes Baseada em Sinopses

## Conclusões

- **Insights dos Dados**: A distribuição do tamanho das sinopses mostra um pico em torno de 10² caracteres, com uma cauda longa estendendo-se até 10⁴ caracteres. O comprimento mediano das sinopses é aproximadamente 500 caracteres, indicando uma ampla variabilidade nos tamanhos. O número de gêneros por filme é predominantemente de 1 a 3, com uma queda acentuada além de 4 gêneros.
- **Desempenho do Modelo**: Três modelos foram avaliados - LinearSVC, Regressão Logística e LSTM. A Regressão Logística obteve a maior pontuação F1 Ponderada de 0,336516, sendo o modelo de melhor desempenho. O LinearSVC mostrou um Micro F1 Score competitivo de 0,315991, enquanto o LSTM teve o menor F1 Ponderado de 0,064134, sugerindo espaço para ajustes de hiperparâmetros.
- **Desafios**: A distribuição desbalanceada dos gêneros e a complexidade da classificação multi-label impactaram o desempenho do modelo, especialmente para gêneros menos frequentes.

## Sugestões de Melhorias

- **Aprimoramento dos Dados**: Incorporar recursos adicionais, como diretor, elenco ou década de lançamento, de forma mais eficaz para melhorar a precisão do modelo.
- **Otimização do Modelo**: Ajustar hiperparâmetros do modelo LSTM e experimentar outras arquiteturas como Transformers para melhorar o desempenho.
- **Balanceamento de Gêneros**: Aplicar técnicas como superamostragem de gêneros raros ou usar pesos de classe de forma mais agressiva para lidar com o desbalanceamento.
- **Pré-processamento de Texto**: Explorar técnicas avançadas de NLP para uma melhor representação e extração de características do texto.
- **Métricas de Avaliação**: Considerar a otimização de limiares para as previsões do LSTM para melhorar as pontuações F1 em todas as métricas.

## Arquivos

- `movie.metadata.tsv`: Contém metadados dos filmes, incluindo gêneros.
- `plot_summaries.txt`: Contém os resumos dos enredos.
- `README.md`: Este arquivo com conclusões e sugestões.