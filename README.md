
# Projeto Final - Processamento de Imagens
Classificação de Imagens via Abordagem Clássica: Extração de Características GLCM e Classificação com SVM

# Equipe

Victor Hugo Favo Moreira RA 2503581 \
Matheus Kodi Yamamura RA 2503557

# Descrição do(s) descritor(es) implementado
GLCM (Gray-Level Co-Occurrence Matrix)
O descritor GLCM extrai características de textura de imagens analisando a distribuição espacial de intensidades de pixels. Ele calcula uma matriz de co-ocorrência que representa a frequência de pares de pixels com valores específicos em uma determinada direção e distância. A partir dessa matriz, são extraídas as seguintes características:

Contraste: Mede a variação local de intensidade.

Correlação: Indica a dependência linear entre pixels.

Energia: Reflete a uniformidade da textura.

Homogeneidade: Captura a proximidade da distribuição de elementos na matriz.

No projeto, o GLCM foi implementado usando a biblioteca mahotas, com configurações padrão para direção e distância.


# Classicador e acurácia
Foram testados quatro classificadores com as características extraídas pelo GLCM:

![image](https://github.com/user-attachments/assets/4e4dc805-4646-41e0-95d5-41c57b9b71f8)


# Instruções de uso (opcional)
1. Pré-requisitos
2. Ambiente de execução no Google Colab. 
\
Montagem do Google Drive com a estrutura de pastas especificada. 
## Estrutura de Diretórios
/content/drive/MyDrive/Colab Notebooks/VC/Extracao_Classificacao/  
├── datasets/  
│   └── covid19/  
│       ├── train/  
│       └── test/  
├── features/  
├── modelos/  
└── resultados/  

## Passos para Execução

1. Montagem do Google Drive

from google.colab import drive  
drive.mount('/content/drive')  

2. Antes de iniciar o código principal, inicie uma nova célula ( ctrl + M B) e digite:
- !pip install mahotas

3. Interface do Usuário
- Selecione o dataset desejado na aba DATASET.

- Na aba EXT. CARACTERÍSTICAS, marque GLCM e clique em Extrair Características.

- Na aba TREINAMENTO, selecione os classificadores (SVM, RF, MLP, KNN) e clique em Treinar.

- Na aba CLASSIFICAÇÃO, selecione os modelos treinados e clique em Classificar para gerar matrizes de confusão e relatórios.

4. Resultados
- As métricas (matriz de confusão e relatório de classificação) serão salvas em resultados/
