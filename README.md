# Projeto de Treinamento de Redes Neurais YOLOv5 e YOLOv8

## Introdução

Bem-vindo ao projeto de treinamento de redes neurais YOLOv5 e YOLOv8. Este repositório contém todo o código e documentação necessários para reproduzir o treinamento personalizado de modelos YOLO utilizando a plataforma Roboflow. O objetivo desta documentação é guiar novos pesquisadores para que eles possam replicar nosso trabalho de maneira rápida e eficiente.

## Pré-requisitos

Antes de começar, certifique-se de ter os seguintes itens instalados:

- Python 3.8 ou superior
- Jupyter Notebook
- Git
- Conta no Google Colab
- Conta na plataforma Roboflow

## Instruções de Instalação

Siga os passos abaixo para configurar o ambiente de desenvolvimento:

1. Clone este repositório:
    ```sh
    git clone https://github.com/eilucasbar/Percepcao-camaro.git
    cd Percepcao-camaro
    ```

2. Crie um ambiente virtual:
    ```sh
    python -m venv env
    source env/bin/activate  # No Windows use `env\Scripts\activate`
    			      # No Linux utilize `env/bin/activate`
    ```

## Uso

Para executar o projeto, siga os passos abaixo:

1. **Prepare os Dados:**
    - Acesse a plataforma Roboflow e prepare seu conjunto de dados rotulando as imagens necessarias para realizar o treinamento, existe uma média de 600 - 1000 imagens para cada segmento. As imagens devem ser coletadas em diferentes condições de iluminação, clima, ângulos, e cenários para garantir a robustez do modelo.
Deve-se garantir que as imagens cubram a variação de tamanho, orientação e oclusão dos objetos. 
    - Siga as instruções para gerar um link de exportação para o formato YOLOv5 ou YOLOv8.
    

2. **Treinamento no Google Colab:**
    - Acesse os notebooks específicos para treinamento no Google Colab:
      - [Treinamento YOLOv5](https://colab.research.google.com/github/roboflow/notebooks/blob/main/notebooks/train-yolov5-object-detection-on-custom-data.ipynb)
      - [Treinamento YOLOv8](https://colab.research.google.com/github/roboflow/notebooks/blob/main/notebooks/train-yolov8-object-detection-on-custom-dataset.ipynb)

    - Siga as instruções no notebook para configurar e iniciar o treinamento.
    - Utilize o link de exportação gerado pelo Roboflow para carregar os dados.
    - Para fazer o downloado da pasta de treinamento da sua rede neural, você deve utilizar o seguinte código no google Collab(utilizando como referencia o treinamento de uma yoloV5): ```sh [from google.colab import files
 import shutil
Compactar a pasta "yolov5" em um arquivo zip
shutil.make_archive('/content/yolov5', 'zip', '/content/yolov5')
Baixar o arquivo zip para a sua máquina local
files.download('/content/yolov5.zip')]
```


3. **Executar o Notebook:**
    - No Google Colab, siga as instruções no notebook para configurar o ambiente e executar o treinamento.
    - Certifique-se de ajustar os hiperparâmetros conforme necessário para seu conjunto de dados.

## Estrutura do Projeto

- `data/` : Contém os dados brutos e processados
- `notebooks/` : Contém os notebooks 
  - `yolov5_training.ipynb` : Notebook para treinamento do YOLOv5
  - `yolov8_training.ipynb` : Notebook para treinamento do YOLOv8
- `tests/` : Contém os testes realizados
- `README.md` : Este arquivo de documentação
- `requirements.txt` : Lista de dependências do projeto

## Contribuindo

Se você deseja contribuir com este projeto, por favor siga os passos abaixo:

1. Faça um fork do projeto
2. Crie uma branch para sua feature (`git checkout -b feature/nome-da-feature`)
3. Faça commit das suas alterações (`git commit -m 'Adiciona nova feature'`)
4. Faça push para a branch (`git push origin feature/nome-da-feature`)
5. Abra um Pull Request

## Licença

Este projeto está licenciado sob a Licença MIT. Veja o arquivo [LICENSE](LICENSE) para mais detalhes.

