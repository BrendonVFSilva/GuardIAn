# Guard.IAn - Detecção de Violência em Vídeos

## 📖 Descrição

O projeto Guard.IAn é um sistema de inteligência artificial para detecção de violência em vídeos. Utilizando uma Rede Neural Convolucional (CNN) baseada no modelo pré-treinado VGG-16, o sistema analisa frames de vídeo para classificar cenas como "Violentas" ou "Não Violentas".

O objetivo é fornecer uma ferramenta que possa ser integrada a sistemas de monitoramento para identificar comportamentos agressivos de forma automática.

## 📂 Estrutura do Projeto

Ao baixar este projeto, você terá a seguinte estrutura de pastas:
```
GuardIAn/
|
├── data/                 # Pasta principal para os vídeos
|   ├── Violence/         # ARRASTE SEUS VÍDEOS DE VIOLÊNCIA AQUI
|   └── NonViolence/      # ARRASTE SEUS VÍDEOS NORMAIS AQUI
|
├── GuardIAn_FINAL.ipynb  # Notebook com todo o código
|
└── README.md             # Este arquivo
```

## 🚀 Como Executar

1.  **Clone ou baixe o repositório.**

2.  **Adicione os vídeos:**
    - Baixe os vídeos que deseja usar para o treinamento. (Se tiver um link público para o dataset, coloque aqui).
    - Arraste os arquivos de vídeo para dentro das pastas `data/Violence` e `data/NonViolence` que já existem no projeto.

3.  **Instale as bibliotecas:**
    ```bash
    pip install tensorflow opencv-python numpy matplotlib
    ```

4.  **Execute o Notebook:**
    Abra e rode o `GuardIAn_FINAL.ipynb`. O código irá ler os vídeos das pastas, treinar o modelo e salvá-lo automaticamente em uma nova pasta chamada `models`.
