# AAE
Este repositório contém uma implementação do Adversarial Autoencoder (AAE), um modelo híbrido que combina autoencoders e redes adversariais. Ao contrário dos autoencoders tradicionais, o AAE usa uma rede discriminadora adversarial, melhorando a qualidade das representações geradas e das imagens reconstruídas.

Este repositório inclui:

- Pré-processamento dos dados MNIST: As imagens são normalizadas e formatadas para otimizar o treinamento do modelo.
- Arquitetura do Autoencoder: Um modelo composto por um encoder para mapear as imagens para o espaço latente e um decoder para reconstruí-las a partir deste espaço latente.
- Rede Discriminadora Adversarial: Uma rede treinada para distinguir entre amostras reais (da distribuição normal) e amostras geradas pelo autoencoder, garantindo que o espaço latente siga uma distribuição desejada.
- Função de Perda Wasserstein: Utilizada para melhorar a estabilidade do treinamento, juntamente com uma penalidade de gradiente para regularizar o modelo.
- Treinamento e Avaliação: O modelo foi treinado por 100 épocas, com uma série de verificações e ajustes para otimizar o desempenho tanto do autoencoder quanto do discriminador adversarial.

Objetivo:

O objetivo deste projeto foi avaliar a capacidade do Adversarial Autoencoder em remover ruídos de imagens. Graças à sua habilidade de representar os dados em um vetor latente, o autoencoder consegue focar nas características essenciais comuns a todas as imagens do banco de dados. Assim, quando uma imagem ruidosa é passada para o autoencoder já treinado, ele é capaz de restaurar a imagem original, removendo o ruído presente.
