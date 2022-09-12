.. Cancer Project documentation master file, created by
   sphinx-quickstart on Fri May  7 10:07:23 2021.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.

Welcome to Cancer Project's documentation!
==========================================

Authors
-------

* Gisele Fernandes - Epidemiology and Statistics on Cancer Group, International Research Center, A.C. Camargo Cancer Center
* Lucas Buk Cardoso - Research Engineer at Núcleo de Sistemas Eletrônicos Embarcados, Instituto Mauá de Tecnologia
* Maria Paula Curado - Epidemiology and Statistics on Cancer Group, International Research Center, A.C. Camargo Cancer Center
* Stela Verzinhasse Peres - Director of Information and Epidemiology, Fundação Oncocentro de São Paulo
* Tatiana Natasha Toporcov - Epidemiology Department, Faculdade de Saúde Pública, Universidade de São Paulo
* Vanderlei Cunha Parro - Coordinator of Núcleo de Sistemas Eletrônicos Embarcados, Instituto Mauá de Tecnologia

Introduction
------------

Here is presented the project documentation using **all types of cancer** provided by FOSP (Fundação Oncocentro de São Paulo).

The project aims to use machine learning models to predict and identify the characteristics that most interfere in the death and survival of cancer patients in the state of São Paulo, Brazil. The data were extracted from the Deputy Directorate of Information and Epidemiology of Fundação Oncocentro de São Paulo, coordinator of the Hospital Cancer Registry of São Paulo, and contains patients treated between 2000 and 2021.

The project was developed using the python language, using machine learning models, specifically the models Random Forest and XGBoost. 

Complete notebooks are available on `Github <https://github.com/Lucas-Buk/cancer_project>`_.

Summary
-------

The project will be divided in topics to provide a better understanding and organization. The steps being:

* Libraries and Functions;
* Data analysis, creation of new columns and first preprocessing;
* Classifiers: with preprocessing, training and validation of machine learning models. Using five labels:

   * obito_geral;

   * obito_cancer;

   * vivo_ano1;

   * vivo_ano3;

   * vivo_ano5.

For each label, some scenarios were used to analyze the performance of the models, such as grouping the years and removing some columns from the data.

.. toctree::
   :maxdepth: 2
   :caption: Libraries and functions

   Cancer Libraries and functions

.. toctree::
   :maxdepth: 2
   :caption: Data Analysis

   Cancer Models

.. toctree::
   :maxdepth: 2
   :caption: Classification obito_geral

   Label - obito_geral

.. toctree::
   :maxdepth: 2
   :caption: Classification obito_cancer

   Label - obito_cancer

.. toctree::
   :maxdepth: 2
   :caption: Classification vivo_ano1

   Label - vivo_ano1

.. toctree::
   :maxdepth: 2
   :caption: Classification vivo_ano3

   Label - vivo_ano3

.. toctree::
   :maxdepth: 2
   :caption: Classification vivo_ano5

   Label - vivo_ano5