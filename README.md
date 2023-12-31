# Visão Computacional com o YOLOV8

## Premisa:

O tutorial visa capacitar os leitores a entenderem os conceitos fundamentais da visão computacional, aprenderem a preparar conjuntos de dados de imagens, treinar modelos de reconhecimento de imagens e implantar esses modelos em aplicações reais.

A premissa do tutorial é fornecer um recurso abrangente e prático para ajudar os leitores a utilizar efetivamente a visão computacional no reconhecimento de imagens, utilizando o Google Colab e o Roboflow como ferramentas principais para o desenvolvimento e implementação dos modelos.

### O que está sendo utilizado:

1. [Google Colabs](https://colab.research.google.com/)

A premissa do Google Colaboratory, também conhecido como Google Colab ou simplesmente Colab, é fornecer um ambiente de notebook interativo baseado em nuvem que permite aos usuários escrever, executar e colaborar em código Python. O Colab é uma plataforma gratuita oferecida pelo Google que permite a execução de notebooks Jupyter na nuvem, eliminando a necessidade de configurar e manter uma infraestrutura local para desenvolvimento e execução de código.

Com o Google Colab, os usuários podem criar e compartilhar notebooks contendo código Python, além de texto explicativo, visualizações e outros elementos interativos. O ambiente de notebook é executado em máquinas virtuais hospedadas pelo Google, permitindo que os usuários escrevam e executem código em tempo real, sem a necessidade de instalar ou configurar bibliotecas ou dependências.

Além disso, o Google Colab fornece acesso a poderosos recursos computacionais, como GPUs e TPUs, permitindo que os usuários executem tarefas de aprendizado de máquina e processamento de dados em larga escala. Ele também oferece integração com várias bibliotecas populares de ciência de dados e aprendizado de máquina, como TensorFlow, PyTorch e scikit-learn.

![ColabsLogo](https://github.com/Datahuntl/VComputacional/assets/103469153/4d0775da-7d6a-4c09-80ba-c3e63b24555c)  

2. [Roboflow](https://roboflow.com/)

Roboflow é uma plataforma de visão computacional que fornece ferramentas e serviços para ajudar desenvolvedores a treinar, implantar e dimensionar modelos de aprendizado de máquina para tarefas de processamento de imagens. Ao utilizar o Roboflow, os desenvolvedores podem fazer upload de conjuntos de dados de imagens, realizar tarefas de pré-processamento para limpar e preparar os dados, treinar modelos de aprendizado de máquina usando algoritmos populares como redes neurais convolucionais (CNNs), e implantar os modelos treinados em aplicativos ou serviços em nuvem. A plataforma também oferece recursos avançados, como anotação de dados, aumentação de dados e monitoramento de desempenho dos modelos implantados.

![RoboflowLogo](https://github.com/Datahuntl/VComputacional/assets/103469153/12810202-022d-4684-b362-615670efa010)

3. [Python](https://www.python.org/)

A utilização do Python é simplesmente para o nosso código no Colabs, porém não se preocupe, pois estará tudo no nosso passo a passo.

![PythonLogo](https://github.com/Datahuntl/VComputacional/assets/103469153/91e57b34-2662-4bee-ac61-533a72f3f9ae)

## Topicos a serem abordados

### [Introdução:](https://github.com/Datahuntl/VComputacional/blob/main/Introdu%C3%A7%C3%A3o.md)

1. Visão Computacional e Reconhecimento de Imagens: uma visão geral
2. O que é o YOLO?
3. Aplicações práticas do reconhecimento de imagens

### [Utilização de um Dataset da Comunidade para treinar um Modelo:](https://github.com/Datahuntl/VComputacional/edit/main/Roboflow%20Universe.md)
1. Coleta e Preparação dos Dados do Roboflow
    - Explorando o Universo Roboflow e Projetos
    - Selecionando um projeto para utilizar
2. Treinamento do Modelo no Colab
   - Treinamento por dados locais

### [Utilização de um Dataset personalizado para treinar um modelo:](https://github.com/Datahuntl/VComputacional/blob/main/RoboflowCustom.md)

1. Coleta e Preparação dos Dados do Roboflow
   - Carregamento de conjuntos de dados de imagens no Roboflow
   - Anotação e rotulagem dos dados usando o Roboflow
2. Treinamento do Modelo no Colab
   - Treinamento por dados locais
