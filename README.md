# FirstMultiLayer
Multilayer Perceptron

Projeto inicial de uma MLP para classificação de dados.

Para resolução deste problema através da MLP, foram separadas em algumas etapas para sua implementação. As entradas foram definidas na função principal e os respetivos tamanhos que cada camada teria de neurônios, sendo que a camada escondida teria log2N neurônios que são
estabelecidos na função principal.

Definiu-se uma arquitetura da matriz de pesos como um vetor de matrizes, onde cada uma dessas matrizes são referentes aos pesos de uma camada (no caso duas). Utilizou-se o backpropagation onde os forward são realizados obtendo os valores de net e função aplicada a net de cada neurônio e em cada camada, armazenando esses valores em uma matriz de respostas.

Após esta fase os erros parciais e globais são recalculados e respectivamente os deltas para cada camada e cada neurônio e obtido através das funções delta_hidden e delta_saida. Assim, os pesos são atualizados para cada camada começando pela oculta e se propagando até chegar na camada de entrada. O processo se repete pelo número de amostras que foram colocadas como entrada, caso o erro global continue maior que o threshold esta fase se inicia novamente e o back propagation é realizado de novo procurando os valores corretos para os pesos de cada camada. O algoritmo consegue convergir para um valor de pesos que e, dependendo do threshold, consegue chegar ao aproximado em uma taxa de erro perto de 0. Para obter erro próximo de zero é preciso utilizar várias épocas.
