# Utilização de um Dataset personalizado para treinar um modelo

## Premisa:

O objetivo de utilizar um dataset personalizado, como coloca-lo no Roboflow, anota-los e treina-los no Colab.

![RoboflowLogo](https://github.com/Datahuntl/VComputacional/assets/103469153/12810202-022d-4684-b362-615670efa010)
![ColabsLogo](https://github.com/Datahuntl/VComputacional/assets/103469153/4d0775da-7d6a-4c09-80ba-c3e63b24555c)

## Coleta e Preparação dos Dados do Roboflow

### 1. Carregamento de conjuntos de dados de imagens no Roboflow

Na sua área de trabalho no Roboflow vamos criar um projeto novo selecionando a opção "Create new Project".

![image](https://github.com/Datahuntl/VComputacional/assets/103469153/3f0f6f0d-41d9-42ef-8713-65808e6bc5dd)

Selecione o tipo do projeto, o que você está detectando e o nome do projeto, mantendo a lincesa a mesma.

![image](https://github.com/Datahuntl/VComputacional/assets/103469153/928156da-39ec-41eb-9d03-3ea71ad9b366)

Ao criar o nosso projeto vamos para a parte de "Upload" ou Descarregar arquivos ou pasta no seu projeto.

![image](https://github.com/Datahuntl/VComputacional/assets/103469153/032d31d1-ceaa-46b5-9862-530bbe531710)

#### Anotação e rotulagem dos dados usando o Roboflow

Após fazermos o upload de todas as imagens que queremos anotar vamos começar a anota-las, que fica na parte de "Annotate".

![image](https://github.com/Datahuntl/VComputacional/assets/103469153/0b33280a-aeb1-4749-98a3-efabc6af28ed)

A parte "Unassigned" são imagens que foram descarregadas no seu projeto porem não tem alguem como o Anotador da "task". A parte Annotating são tasks que estão sendo anotadas e a parte Dataset é o conglomerado seu de todas as imagens rotuladas.

Para você atribuir alguem a fazer uma task é o seguinte, primeiro selecione qual task você quer atribuir:

![image](https://github.com/Datahuntl/VComputacional/assets/103469153/485c5531-7df7-4538-9ff6-19cdb30797e5)

Após, selecione qual das pessoas dentro do seu projeto vão anotar a task, o roboflow divide a task igualmente caso várias pessoas façam a anotação de uma task.

![image](https://github.com/Datahuntl/VComputacional/assets/103469153/d1b38df9-1b1d-45a7-bb65-9c16aa833ddc)

E agora você tem uma task atribuida pronta para ser anotada.

Durante a anotação de imagens é de suma importancia que você utilize apenas Bounding Boxes ou Poligonos de segmentação, pois o YOLOV8 não consegue treinar um dataset mixado.

![image](https://github.com/Datahuntl/VComputacional/assets/103469153/f5f2a888-2eb2-41bc-8d66-42ccdd31d3b8)

#### Criando uma Versão do Dataset

Agora que temos o nosso dataset anotado vamos criar uma versão dele no Roboflow para que ele seje treinado no YOLO. Para criar uma versão do seu Dataset será necessário ir na aba de "Generate" como na imagem a seguir:

![image](https://github.com/Datahuntl/VComputacional/assets/103469153/8e96da00-c2c8-43ea-a7cb-5960152c0e30)

Ao selecionar a opção "Generate New Version" você ira ver quantas imagens você tem no total e opções de Pre-Processamento ou Augmentação que você pode colocar no seu dataset, e no final você vai gerar a primeira versão do seu Dataset!

![image](https://github.com/Datahuntl/VComputacional/assets/103469153/c7e98845-6089-4f42-b367-2f84bd72265a)

### 2. Treinamento do Modelo no Colab

   #### Treinamento por dados locais

No treinamento de dados locais você vai precisar fazer o download do dataset, clicando na opção "Get Snippet".

![image](https://github.com/Datahuntl/VComputacional/assets/103469153/44436fd3-a917-4b88-b3c4-00a47eeb3c0b)

![image](https://github.com/Datahuntl/VComputacional/assets/103469153/083e437d-cf20-4da7-af2d-c19bc690bfad)


Escolhendo o Formato de YOLOV8, vamos fazer o download do nosso arquivo em zip. Ao ter o dataset instalado podemos extrair a pasta em qualquer local de preferencia.

Após extrair a pasta vamos precisar do seguinte:

![IoMA Ideia (2)](https://github.com/Datahuntl/VComputacional/assets/103469153/2026bb51-78c4-4219-ad6e-cf1beace3ddf)

![image](https://github.com/Datahuntl/VComputacional/assets/103469153/c7bbc184-fbb5-4f91-9f1f-37e2f6e00087)

O arquivo data.yaml vai ficar junto com o notebook, enquanto as pastas de "train", "test" e "valid" vão ficar dentro da Pasta que criamos chamada "Data", não se preocupe com a pasta chamada "Runs" pois o YOLO cria ela para fazer o treinamento.

Quando tiver feito os arranjos necessários, abra o arquivo chamado "data.yaml" com o seu bloco de notas, aparecendo o seguinte:

![image](https://github.com/Datahuntl/VComputacional/assets/103469153/d591044b-3ba7-4d1f-975b-2034a1e525d4)

No arquivo do data.yaml você vai precisar alterar os locais de origem do "train", "test" e "valid" para os locais dele **no seu drive** como no exemplo a seguir:

![image](https://github.com/Datahuntl/VComputacional/assets/103469153/8cbc0b85-2553-4a56-be6a-abaef3834570)

Com o dataset instalado no seu drive e o data.yaml corrigido podemos começar a treinar o nosso modelo.

(Com esse notebook do Colab](https://colab.research.google.com/drive/10n7kMuX8Ik0Ttx7XkULgRWHqY9MjYviP?usp=sharing) você podera ver como ficara o nosso treinamento por meio de dados locais.

No Tópico de "Treinamento por Dados Locais" simplesmente rode os blocos de código e faça alterações nas epócas ou tamanho da imagem caso necessário e você terá um modelo treinado.
