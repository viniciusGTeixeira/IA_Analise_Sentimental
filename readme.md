# Facial Emotion Detection

Este projeto utiliza aprendizado de máquina para detectar emoções faciais em imagens e vídeos. Ele usa uma rede neural convolucional (CNN) treinada com o dataset FER-2013.

## Estrutura do Projeto

- `train_model.py`: Script para treinar o modelo de detecção de emoções.
- `detect_emotion.py`: Script para detectar emoções em tempo real a partir de uma webcam.

## Requisitos

1. **Python 3.x**: Certifique-se de ter Python 3.x instalado. Recomenda-se criar um ambiente virtual para o projeto.

2. **Instalação das Dependências**: Instale as bibliotecas necessárias usando o arquivo `requirements.txt`. Execute o comando abaixo para instalar as dependências:

    ```bash
    pip install -r requirements.txt
    ```

    O arquivo `requirements.txt` pode ser gerado com:

    ```bash
    pip freeze > requirements.txt
    ```

3. **Arquivos Grandes**: Alguns arquivos, como bibliotecas e pacotes, podem ser grandes e não devem ser versionados no Git. Para garantir que seu ambiente de desenvolvimento esteja corretamente configurado, você pode precisar instalar as seguintes dependências:

    - **TensorFlow**: Arquivo `libtensorflow_cc.2.dylib` é muito grande e deve ser instalado via pip.
    - **NumPy**: Arquivo `libopenblas64_.0.dylib` pode ser instalado via pip.
    - **OpenCV**: Arquivo `cv2.abi3.so` deve ser instalado via pip.
    - **Clang**: Arquivo `libclang.dylib` deve ser instalado via pip.

    Certifique-se de instalar essas bibliotecas através do ambiente virtual e não incluí-las no repositório Git.

4. **Git LFS**: Se você precisar versionar arquivos grandes, considere usar Git Large File Storage (LFS). Mais informações estão disponíveis em [Git LFS](https://git-lfs.github.com).

## Como Executar o Projeto

1. **Treinar o Modelo**: Execute o script `train_model.py` para treinar o modelo de detecção de emoções:

    ```bash
    python train_model.py
    ```

    Este script treina o modelo com o dataset FER-2013 e salva o modelo treinado como `emotion_detection_model.h5`.

2. **Detectar Emoções**: Execute o script `detect_emotion.py` para começar a detecção de emoções em tempo real usando a webcam:

    ```bash
    python detect_emotion.py
    ```

    Certifique-se de que o modelo treinado (`emotion_detection_model.h5`) está disponível no mesmo diretório.

## Observações

- **Pasta `emotion_env/`**: Esta pasta contém o ambiente virtual e não deve ser versionada. Crie o ambiente virtual e instale as dependências conforme indicado acima.

- **Arquivos Grandes**: Certifique-se de que arquivos grandes, como bibliotecas e pacotes, são instalados através do ambiente virtual e não são adicionados ao repositório Git.

## Licença

Este projeto está licenciado sob a [Licença Não Comercial](LICENSE). Apenas pessoas autorizadas podem acessar e utilizar o código fonte. Veja o arquivo [LICENSE](LICENSE) para mais detalhes.

