# Cancer Project - English version
<p align="center">
  <img src="https://scontent-gru1-1.cdninstagram.com/v/t51.2885-19/190687941_204986924790877_2081934706775828299_n.jpg?stp=dst-jpg_s320x320&_nc_ht=scontent-gru1-1.cdninstagram.com&_nc_cat=101&_nc_ohc=zSUkc4bE1CIAX-i90W_&edm=AOQ1c0wBAAAA&ccb=7-5&oh=00_AfDTMBW5lsDotItvppf4zGU2PyeRDzfXGrDXz7GwNoo9zA&oe=65F109CA&_nc_sid=8b3546",width=400, height=240/>
</p>

___

## **Introduction**

The project aims to use machine learning models to predict and identify the characteristics that most interfere in the death and survival of cancer patients in the state of São Paulo, Brazil. The data were extracted from the Deputy Directorate of Information and Epidemiology of Fundação Oncocentro de São Paulo (FOSP), coordinator of the Registro Hospitalar de Câncer de São Paulo (RHC-SP), and contains patients treated between 2000 and 2021.

## **How to run**

To start running the notebooks in this repository, follow these steps:

1. Clone this repository to your local enviroment using the following command:

    ```git clone https://github.com/DCD-NSEE/cancer_project```


2. Open the notebooks in your Python development environment, preferably [Google Colaboratory](https://research.google.com/colaboratory/), but you can also use [Jupyter Notebook](https://jupyter.org/) or [VSCode](https://code.visualstudio.com/) locally.

3. Install the required python libraries
   
## **Setting up the project locally**

### Creating the virtual enviroment (venv)

#### Windows

```console
python -m venv venv
```

#### Linux

```
virtualenv -p python3.10 venv
```

### Activating the venv

#### Windows

```console
venv\Scripts\activate
```

#### Linux

```console
source venv/bin/activate
```

### installing the packages

```console
pip install -e .

pip install -r requirements.txt
```

## **Contributions**

We encourage contributions from other students, teachers, researchers, or data science enthusiasts. If you wish to contribute with your own content, corrections, or improvements to the notebooks, follow these steps:

1. Fork this repository.

2. Make your changes in your fork.

3. Submit a pull request describing your changes and reasons.

## **Contact**

If you have any questions or need assistance, feel free to contact the author:

Send an email to [Pedro Mesquita](mailto:pedro.gjmesquita@gmail.com), to [Lucas Buk](maailto:lucasbukcardoso@gmail.com) or directly to [NSEE](mailto:nsee@maua.br).

---

# Cancer Project - Versão em português


## **Introdução**

O projeto visa avaliar a possibilidade de modelos de aprendizado de máquina treinados com um tipo específico de câncer preverem a sobrevida de 3 anos após o diagnóstico da doença para pacientes com outros tipos. Foram conduzidas duas análises, uma utilizando os seis tipos de câncer mais incidentes (pele, mama, próstata, pulmão, colorretal e cervical) e outra com tipos relacionados ao sistema digestivo (boca, orofaringe, esôfago, estômago, intestino delgado, colorretal e ânus). Métricas foram obtidas para cada tipo individualmente e comparadas com os resultados obtidos ao usar tipos mistos para treinar os modelos.

## Como Utilizar

Para começar a usar os recursos deste repositório, siga estas etapas:

1. Clone este repositório para o seu ambiente local usando o comando:

    ```git clone https://github.com/DCD-NSEE/cancer_project```


2. Abra os notebooks em seu ambiente de desenvolvimento Python, de preferência o [Google Colaboratory](https://research.google.com/colaboratory/), porém pode se usar localmente o [Jupyter Notebook](https://jupyter.org/) ou o [VSCode](https://code.visualstudio.com/).

3. Instale as bibliotecas necessárias no python
   
## **Configurando o projeto para rodar**

### Criando o ambiente virtual (venv)

#### Windows

```console
python -m venv venv
```

#### Linux

```
virtualenv -p python3.10 venv
```

### Ativando a venv

#### Windows

```console
venv\Scripts\activate
```

#### Linux

```console
source venv/bin/activate
```

### Instalando os pacotes

```console
pip install -e .

pip install -r requirements.txt
```

## **Contribuições**

Encorajamos contribuições de outros alunos, professores, pesquisadores ou entusiastas da ciência de dados. Se você deseja contribuir com seu próprio conteúdo, correções ou melhorias nos notebooks, siga estas etapas:

1. Faça um fork deste repositório.

2. Faça suas alterações no seu fork.

3. Envie um pull request descrevendo suas alterações e motivos.

## **Contato**

Se você tiver dúvidas ou precisar de assistência, sinta-se à vontade para entrar em contato com o autor:

Enviar email para [Pedro Mesquita](mailto:pedro.gjmesquita@gmail.com), para [Lucas Buk](maailto:lucasbukcardoso@gmail.com) ou diretamente para o [NSEE](mailto:nsee@maua.br)


## **Authors**

* Lucas Buk Cardoso - Instituto Mauá de Tecnologia
* Vanderlei Cunha Parro - Instituto Mauá de Tecnologia
* Stela Verzinhasse Peres - Fundação Oncocentro de São Paulo
* Maria Paula Curado - A.C. Camargo Cancer Center
* Gisele Fernandes - A.C. Camargo Cancer Center
* Tatiana Natasha Toporcov - Faculdade de Saúde Pública da Universidade de São Paulo

## **Docs**

The project was developed using the python language, using machine learning models, specifically the models Random Forest and XGBoost. Access the documentation [here](https://cancer-project.readthedocs.io/en/latest/).



 

