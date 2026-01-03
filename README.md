📊 Avaliação de Métricas de Classificação com Redes Neurais (MNIST)

Este repositório contém a implementação completa de uma Rede Neural Convolucional (CNN) para o reconhecimento de dígitos manuscritos (Dataset MNIST), com foco principal na extração manual e validação de métricas de performance.

🚀 Sobre o Processo

O projeto foi estruturado de forma modular em 5 células principais dentro de um ambiente Google Colab, garantindo que cada etapa (desde a preparação dos dados até a análise final) fosse executada e validada individualmente.

🛠️ Ferramentas Utilizadas

O projeto faz uso das bibliotecas mais robustas do ecossistema de Data Science em Python:

* TensorFlow & Keras: Para a construção da arquitetura CNN e geração da matriz de confusão (tf.math.confusion_matrix).

* Pandas: Utilizado para a estruturação dos dados da matriz em DataFrames, facilitando a visualização.

* NumPy: Essencial para manipulação matricial e normalização dos dados.

* Matplotlib & Seaborn: Empregados na visualização de dados e geração do Heatmap da matriz de confusão.

🧬 Estrutura do Código

1. Célula 1 - Ambiente: Instalação do TensorFlow e importação das bibliotecas base.

2. Célula 2 - Dados: Carregamento do dataset MNIST, normalização dos pixels (escala 0-1) e reshape das imagens.

3. Célula 3 - Arquitetura: Definição de uma CNN com camadas Conv2D, MaxPooling2D, Flatten e Dense. O modelo utiliza otimizador Adam e perda sparse_categorical_crossentropy.

4. Célula 4 - Matriz de Confusão: Geração das previsões e criação da matriz de confusão normalizada com 2 casas decimais.

5. Célula 5 - Métricas Manuais: Implementação das fórmulas matemáticas para extrair os resultados finais.

📏 Métricas Implementadas

Para uma avaliação rigorosa, foram utilizadas as seguintes fórmulas (seguindo a ordem de implementação no código):

* Sensibilidade (Recall): $VP / (VP + FN)$

* Especificidade: $VN / (FP + VN)$

* Acurácia: $(VP + VN) / N$

* Precisão: $VP / (VP + FP)$

* F-score: $2 \times (Precisão \times Sensibilidade) / (Precisão + Sensibilidade)$

📈 Resultados Obtidos

Após o treinamento de 5 épocas, o modelo apresentou os seguintes resultados (extraídos da Célula 5):

Métrica

Valor Obtido

Sensibilidade

0.9959

Especificidade

0.9996

Acurácia

0.9992

Precisão

0.9959

F-Score

0.9959

Estes números confirmam que a rede neural aprendeu a distinguir os dígitos com um índice de erro quase nulo, demonstrando alta robustez tanto na detecção quanto no descarte de falsos positivos.

Projeto desenvolvido por Fred. Realizado como parte da formação em Machine Learning da DIO (Digital Innovation One), patrocinado pela BairesDev.
