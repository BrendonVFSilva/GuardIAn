# Guard.IAn - Detecção de Violência com Análise Temporal

## 📖 Descrição

O Guard.IAn é um sistema de Inteligência Artificial projetado para detectar violência em vídeos. O projeto utiliza uma arquitetura híbrida de Deep Learning, combinando uma **Rede Neural Convolucional (VGG-16)** para extração de características visuais de cada frame, com uma **Rede Neural Recorrente (LSTM)** para analisar a sequência temporal dessas características.

Essa abordagem permite que o modelo não apenas "veja" o que está acontecendo em um instante, mas também entenda o "contexto" de como a cena evolui ao longo do tempo, o que é crucial para diferenciar interações normais de agressões reais. O sistema implementa uma análise por **janela deslizante** para simular o monitoramento em tempo real.

## ✨ Funcionalidades

* **Extração de Características com VGG-16:** Utiliza um modelo pré-treinado robusto para converter frames de vídeo em vetores de características de alta qualidade.
* **Análise Temporal com LSTM:** Aprende a reconhecer padrões em sequências de frames para classificar um clipe de vídeo como "Violento" ou "Não Violento".
* **Análise por Janela Deslizante:** Processa vídeos longos de forma contínua, analisando pequenos trechos (janelas) em sequência para detectar violência no momento em que ocorre.
* **Modelo Pré-Treinado Incluso:** O repositório já contém um modelo treinado (`guardian_model.h5`), pronto para uso imediato.

## 📂 Estrutura do Projeto

```
GuardIAn/
|
├── data/
|   ├── Violence/
|   |   └── coloque_videos_de_treino_aqui.txt
|   └── NonViolence/
|       └── coloque_videos_de_treino_aqui.txt
|
├── models/
|   └── guardian_model.h5  <-- Modelo pré-treinado
|
├── videos_para_testar/
|   └── coloque_seus_videos_de_teste_aqui.txt
|
├── GuardIAn.ipynb <-- O notebook principal
|
└── README.md
```

## 🚀 Como Executar

### Pré-requisitos

As seguintes bibliotecas são necessárias. Instale-as usando `pip`:
```bash
pip install tensorflow opencv-python numpy matplotlib scikit-learn
```

### Usando o Modelo Pré-Treinado (Recomendado)

1.  **Clone o repositório:**
    ```bash
    git clone [https://github.com/SEU_USUARIO/GuardIAn.git](https://github.com/SEU_USUARIO/GuardIAn.git)
    cd GuardIAn
    ```
2.  **Adicione um vídeo para teste:**
    Coloque um ou mais arquivos de vídeo (ex: `.mp4`) dentro da pasta `videos_para_testar`.

3.  **Execute o Notebook:**
    Abra o notebook e siga estes passos:
    * Execute as células desde `### Importação de Bibliotecas` até `### Extração de Características com VGG-16`.
    * **Pule** as células `### Construção de modelo LTSM` e `### Treinamento do Modelo`.
    * Execute a célula que contém `model = load_model('models/guardian_model.h5')`.
    * Execute a célula final, `### Testes com vídeos aleatórios...`, para ver a análise do(s) seu(s) vídeo(s).

### Re-Treinando o Modelo (Opcional)

1.  **Prepare o Dataset:** Coloque seus vídeos de treinamento nas pastas `data/Violence` e `data/NonViolence`.
2.  **Execute o Notebook Completo:** Rode todas as células do notebook em ordem. Ao final, um novo modelo será treinado e salvo como `guardian_model.h5` na pasta `models`.

## 🛠️ Tecnologias Utilizadas

* **TensorFlow / Keras**
* **OpenCV**
* **Scikit-learn**
* **NumPy**
* **Matplotlib**
