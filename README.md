# test-icp-

Título: Estimativa de Trajetória de Veículo usando ICP em Point Clouds

Descrição:
Este projeto consiste em um código para estimar a trajetória de um veículo utilizando o algoritmo ICP (Iterative Closest Point) em nuvens de pontos (point clouds). As point clouds são dados extraídos de scans de um LiDAR e neste caso, utilizaremos um conjunto de 30 scans do KITTI Dataset.

O algoritmo ICP é implementado manualmente, sem o uso de bibliotecas de terceiros que já possuam a implementação do ICP. Isso demonstra a compreensão e aplicação do algoritmo pelos desenvolvedores.

O código carrega as nuvens de pontos de cada scan a partir de arquivos OBJ e, em seguida, estima a trajetória do veículo para cada par consecutivo de nuvens de pontos. Durante esse processo, as transformações são acumuladas e compostas para obter a trajetória final do veículo.

A implementação é verificada utilizando a ground-truth fornecida, que consiste em um arquivo .npy contendo matrizes de transformação em coordenadas homogêneas para cada uma das 30 posições do carro. A trajetória estimada é comparada com a ground-truth para avaliar a precisão do algoritmo.

Para visualizar a trajetória estimada, o código utiliza a biblioteca Matplotlib para exibir um gráfico 3D com os pontos da trajetória em todos os eixos (XYZ). Isso permite uma melhor compreensão da trajetória percorrida pelo veículo ao longo dos scans.

O objetivo deste projeto é fornecer uma implementação do algoritmo ICP para estimativa de trajetória em point clouds, além de demonstrar o conhecimento e a aplicação dos conceitos de transformações de corpo rígido e manipulação de nuvens de pontos.

Bibliotecas utilizadas: NumPy, Matplotlib, SciPy (dependendo da instalação)

Observações:

É importante observar que a implementação do ICP é feita manualmente, sem o uso de bibliotecas que já possuam o algoritmo implementado, como Open3D ou PCL.
O código utiliza as nuvens de pontos fornecidas nos arquivos OBJ, sem a necessidade de usar a biblioteca Trimesh para esse propósito.
A validação da implementação é realizada comparando a trajetória estimada com a ground-truth fornecida, verificando se os resultados estão próximos da realidade.
Sinta-se à vontade para explorar o código e adaptá-lo para suas necessidades. Ele serve como um ponto de partida para a estimativa de trajetória em nuvens de pontos usando o algoritmo ICP.
