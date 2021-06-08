.. Cancer Project documentation master file, created by
   sphinx-quickstart on Fri May  7 10:07:23 2021.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.

Welcome to Cancer Project's documentation!
==========================================

Authors
-------

* Gisele Fernandes
* Lucas Buk Cardoso
* Maria Paula Curado
* Stela Verzinhasse Peres 
* Tatiana Natasha Toporcov
* Vanderlei Cunha Parro

Introduction
------------

Here is presented the project documentation with cancer data provided by FOSP (Fundação Oncocentro de São Paulo).

The project was developed using the python language, with the objective of making predictions for deaths and recovery time of patients with the disease.

Complete files and notebooks are available on `Github <https://github.com/Lucas-Buk/cancer_project>`_.

Summary
-------

The project will be divided into stages to provide a better understanding and organization. The steps being:

* Libraries and Functions;
* Data analysis, creation of new columns and first preprocessing;
* Classifiers: with preprocessing, creation and validation of machine learning models. Using six labels:

   * ob;

   * RECNENHUM;

   * RECDIST;

   * vivo_ano1;

   * vivo_ano3;

   * vivo_ano5.

Data Dictionary
---------------

The data has 93 columns, below we have a description of each one.

* **SEXO**: Gender of the patient (int = 1).

   1 - MALE;
   
   2 - FEMALE.

* **IDADE**: Patient's age (int = 3).

* **ESCOLARI**: Code for patient education (int = 1).

   1 - ILLITERATE;
   
   2 - ELEMENTARY SCHOOL INCOMPLETE;
   
   3 - ELEMENTARY SCHOOL COMPLETE;
   
   4 - HIGH SCHOOL;
   
   5 - UNIVERSITY EDUCATION;
   
   9 - IGNORED.

* **UFNASC**: UF of birth (char = 2). Other options: SI - No information; OP - Another country.
* **UFRESID**: UF of residence (char = 2). Other options: OP - Another country.
* **IBGE**: Code of the patient's city of residence according to IBGE with check digit (char = 7).
* **CIDADE**: City of residence of the patient (char = 200).
* **CATEATEND**: Category of diagnosis assistance (int = 1).

   1 - HEALTH INSURANCE;
   
   2 - SUS;
   
   3 - PRIVATE;
   
   9 - NO INFORMATION.
* **DTCONSULT**: Date of the first consultation (date = 10). Format: DD/MM/YYYY
* **CLINICA**: Clinic code (int = 2).

   1 - ALLERGY / IMMUNOLOGY;

   2 - HEART SURGERY;
   
   3 - HEAD AND NECK SURGERY;
   
   4 - GENERAL SURGERY;
   
   5 - PEDIATRIC SURGERY;
   
   6 - PLASTIC SURGERY;
   
   7 - THORAXIC SURGERY;
   
   8 - VASCULAR SURGERY;
   
   9 - CLINICA MEDICA;
   
   10 - DERMATOLOGY;
   
   11 - ENDOCRINOLOGY;
   
   12 - GASTRO SURGERY;
   
   13 - GASTROENTEROLOGY;
   
   14 - MANAGEMENT;
   
   15 - GYNECOLOGY;
   
   16 - GYNECOLOGY / OBSTETRIC;
   
   17 - HEMATOLOGY;
   
   18 - INFECTOLOGY;
   
   19 - NEPHROLOGY;
   
   20 - NEUROSURGERY;
   
   21 - NEUROLOGY;
   
   22 - OPHTHALMOLOGY;
   
   23 - SURGICAL ONCOLOGY;
   
   24 - CLINICAL ONCOLOGY;
   
   25 - PEDIATRIC ONCOLOGY;
   
   26 - ORTHOPEDICS;
   
   27 - OTORHINOLARYNGOLOGY;
   
   28 - PEDIATRICS;
   
   29 - PNEUMOLOGY;
   
   30 - PROCTOLOGY;
   
   31 - RADIOTHERAPY;
   
   32 - UROLOGY;
   
   33 - MASTOLOGY;
   
   34 - CUTANEA ONCOLOGY;
   
   35 - PELVIC SURGERY;
   
   36 - ABDOMINAL SURGERY;
   
   37 - DENTISTRY;
   
   38 - HEPATIC TRANSPLANTATION;
   
   99 - IGNORED.
* **DIAGPREV**: Diagnosis and previous treatment (int = 1).

   1 - WITHOUT DIAGNOSIS / WITHOUT TREATMENT;

   2 - WITH DIAGNOSIS / WITHOUT TREATMENT;

   3 - WITH DIAGNOSIS / WITH TREATMENT;

   4 - OTHERS.
* **DTDIAG**: Date of diagnosis (date = 10). Format: DD/MM/YYYY
* **BASEDIAG**: Code of the diagnosis base (int = 1).

   1 - CLINICAL EXAMINATION;

   2 - NON-MICROSCOPIC AUXILIARY RESOURCES;

   3 - MICROSCOPIC CONFIRMATION;

   4 - NO INFORMATION.
* **TOPO**: Topography code (char = 4). Format: C999
* **TOPOGRUP**: Topography group (char = 3). Format: C99
* **DESCTOPO**: Topography description (char = 80).
* **MORFO**: Morphology code (char = 5). Format: 99999
* **DESCMORFO**: Description of the morphology (char = 80).
* **EC**: Clinical stage (char = 5).
* **ECGRUP**: Clinical staging group (char = 3).

   0 - Primary tumors, classified as in situ;

   I - Localized tumors;

   II - Tumors with regional involvement by direct extension;

   III - Tumors with regional involvement of lymph nodes;

   IV - Tumors with distant metastasis;

   X - For tumors not evaluated by the responsible professional or without information on staging noted in the medical record;

   Y - For tumors in which the TNM classification is not applied. These are non-solid tumors (for example, leukemias).
* **T**: TNM - T classification (char = 5).
* **N**: TNM - N classification (char = 5).
* **M**: TNM - M classification (char = 3).
* **PT**: Post-surgical staging (char = 5).
* **PN**: Post-surgical staging (char = 5).
* **PM**: Post-surgical staging (char = 3).
* **S**: TNM - S classification (int = 1). Domain: 0; 1; 2; 3; 8 - DOES NOT APPLY; 9 - X
* **G**: TNM Classification - G (Degree) (char = 5).
   Domain (except C40, C41, C381, C382, C383, C47, C48 and C49): 0; 1; two; 3; 4; 8 - DOES NOT APPLY; 9 - X.

   Domain (C40, C41, C381, C382, C383, C47, C48 and C49 only): HIGH; LOW; 8 - DOES NOT APPLY; 9 - X.
* **LOCALTNM**: TNM Classification - Location (int = 1).

   1 - SUPERIOR;

   2 - MEDIUM;

   3 - LOWER;

   8 - NOT APPLICABLE;

   9 - X.
* **IDMITOTIC**: TNM Classification - Mitotic Index (int = 1).

   1 - HIGH;
      
   2 - LOW;
      
   8 - NOT APPLICABLE;
      
   9 - X.
* **PSA**: TNM - PSA classification (int = 1).

   1 - LESS THAN 10;
      
   2 - GREATER OR EQUAL TO 10 AND LESS THAN 20;
      
   3 - GREATER OR EQUAL TO 20;
      
   8 - NOT APPLICABLE;
      
   9 - X.
* **GLEASON**: TNM - Gleason classification (int = 1).

   1 - SMALLER OR EQUAL TO 6;
      
   2 - EQUAL TO 7;
      
   3 - GREATER OR EQUAL TO 8;
      
   8 - NOT APPLICABLE;
      
   9 - X.
* **OUTRACLA**: Another classification of staging (char = 20).
* **META01**: Metastasis (char = 3). Format: C99
* **META02**: Metastasis (char = 3). Format: C99
* **META03**: Metastasis (char = 3). Format: C99
* **META04**: Metastasis (char = 3). Format: C99
* **DTTRAT**: Treatment start date (date = 10). Format: DD/MM/YYYY
* **NAOTRAT**: Reason code for not carrying out the treatment (int = 1).

   1 - REFUSAL OF TREATMENT;
      
   2 - ADVANCED DISEASE, LACK OF CLINICAL CONDITIONS;
      
   3 - OTHER ASSOCIATED DISEASES;
      
   4 - TREATMENT ABANDONMENT;
      
   5 - CANCER DEATH;
      
   6 - DEATH FOR OTHER CAUSES;
      
   7 - OTHER;
      
   8 - NOT APPLICABLE (IF HAVE TREATMENT);
      
   9 - NO INFORMATION.
* **TRATAMENTO**: Combination code of the treatments (char = 1).

   A - Surgery;
      
   B - Radiotherapy;
      
   C - Chemotherapy;
      
   D - Surgery + Radiotherapy;
      
   E - Surgery + Chemotherapy;
      
   F - Radiotherapy + Chemotherapy;
      
   G - Surgery + Radio + Chemo;
      
   H - Surgery + Radio + Chemo + Hormone;
      
   I - Other treatment combinations;
      
   J - No treatment.
* **TRATHOSP**: Combination code of treatments at the hospital (char = 1).

   A - Surgery;
      
   B - Radiotherapy;
      
   C - Chemotherapy;
      
   D - Surgery + Radiotherapy;
      
   E - Surgery + Chemotherapy;
      
   F - Radiotherapy + Chemotherapy;
      
   G - Surgery + Radio + Chemo;
      
   H - Surgery + Radio + Chemo + Hormone;
      
   I - Other treatment combinations;
      
   J - No treatment.
* **TRATFANTES**: Combination code of treatments performed before / during admission outside the hospital (char = 1).

   A - Surgery;
      
   B - Radiotherapy;
      
   C - Chemotherapy;
      
   D - Surgery + Radiotherapy;
      
   E - Surgery + Chemotherapy;
      
   F - Radiotherapy + Chemotherapy;
      
   G - Surgery + Radio + Chemo;
      
   H - Surgery + Radio + Chemo + Hormone;
      
   I - Other treatment combinations;
      
   J - No treatment;

   K - No information.
* **TRATFAPOS**: Combination code of treatments performed after admission outside the hospital (char = 1).

   A - Surgery;
      
   B - Radiotherapy;
      
   C - Chemotherapy;
      
   D - Surgery + Radiotherapy;
      
   E - Surgery + Chemotherapy;
      
   F - Radiotherapy + Chemotherapy;
      
   G - Surgery + Radio + Chemo;
      
   H - Surgery + Radio + Chemo + Hormone;
      
   I - Other treatment combinations;
      
   J - No treatment;

   K - No information.
* **NENHUM**: Treatment received at the hospital = none (int = 1). 0 - NO; 1 - YES
* **CIRURGIA**: Treatment received at the hospital = surgery (int = 1). 0 - NO; 1 - YES
* **RADIO**: Treatment received at the hospital = radiotherapy (int = 1). 0 - NO; 1 - YES
* **QUIMIO**: Treatment received at the hospital = chemotherapy (int = 1). 0 - NO; 1 - YES
* **HORMONIO**: Treatment received at the hospital = hormone therapy (int = 1). 0 - NO; 1 - YES
* **TMO**: Treatment received at the hospital = tmo (int = 1). 0 - NO; 1 - YES
* **IMUNO**: Treatment received at the hospital = immunotherapy (int = 1). 0 - NO; 1 - YES
* **OUTROS**: Treatment received at the hospital = others (int = 1). 0 - NO; 1 - YES
* **NENHUMANT**: Treatment received outside the hospital and before admission = none (int = 1). 0 - NO; 1 - YES
* **CIRURANT**: Treatment received outside the hospital and before admission = surgery (int = 1). 0 - NO; 1 - YES
* **RADIOANT**: Treatment received outside the hospital and before admission = radiotherapy (int = 1). 0 - NO; 1 - YES
* **QUIMIOANT**: Treatment received outside the hospital and before admission = chemotherapy (int = 1). 0 - NO; 1 - YES
* **HORMOANT**: Treatment received outside the hospital and before admission = hormone therapy (int = 1). 0 - NO; 1 - YES
* **TMOANT**: Treatment received outside the hospital and before admission = tmo (int = 1). 0 - NO; 1 - YES
* **IMUNOANT**: Treatment received outside the hospital and before admission = immunotherapy (int = 1). 0 - NO; 1 - YES
* **OUTROANT**: Treatment received outside the hospital and before admission = others (int = 1). 0 - NO; 1 - YES
* **NENHUMAPOS**: Treatment received outside the hospital and during / after admission = none (int = 1). 0 - NO; 1 - YES
* **CIRURAPOS**: Treatment received outside the hospital and during / after admission = surgery (int = 1). 0 - NO; 1 - YES
* **RADIOAPOS**: Treatment received outside the hospital and during / after admission = radiotherapy (int = 1). 0 - NO; 1 - YES
* **QUIMIOAPOS**: Treatment received outside the hospital and during / after admission = chemotherapy (int = 1). 0 - NO; 1 - YES
* **HORMOAPOS**: Treatment received outside the hospital and during / after admission = hormone therapy (int = 1). 0 - NO; 1 - YES
* **TMOAPOS**: Treatment received outside the hospital and during / after admission = tmo (int = 1). 0 - NO; 1 - YES
* **IMUNOAPOS**: Treatment received outside the hospital and during / after admission = immunotherapy (int = 1). 0 - NO; 1 - YES
* **OUTROAPOS**: Treatment received outside the hospital and during / after admission = other (int = 1). 0 - NO; 1 - YES
* **DTULTINFO**: Date of the patient's last information (date = 10). Format: DD/MM/YYYY
* **ULTINFO**: Last information about the patient (int = 1).

   1 - LIVE, WITH CANCER;
      
   2 - LIVE, WITHOUT OTHER SPECIFICATIONS;
      
   3 - CANCER DEATH;
      
   4 - DEATH FOR OTHER CAUSES, WITHOUT OTHER SPECIFICATIONS.
* **CONSDIAG**: Difference in days between the dates of consultation and diagnosis (num = days).
* **TRATCONS**: Difference in days between the dates of consultation and treatment (num = days).
* **DIAGTRAT**: Difference in days between the dates of treatment and diagnosis (num = days).
* **ANODIAG**: Year of diagnosis (int = 4). Format: 9999
* **CICI**: Childhood tumor (char = 5).
* **CICIGRUP**: Childhood tumor - Group (char = 80).
* **CICISUBGRU**: Childhood tumor - Subgroup (char = 80).
* **FAIXAETAR**: Age range of the patient (char = 5).
* **LATERALI**: Laterality (int = 1).

   1 - RIGHT;
   
   2 - LEFT;
      
   3 - BILATERAL;
      
   8 - NOT APPLICABLE.
* **INSTORIG**: Home institution (char = 200). Mandatory only if DIAGPREV = 03 - WITH DIAGNOSIS / WITH TREATMENT.
* **DRS**: Regional Health Departments (char = 200).
* **RRAS**: Regional Health Care Network (char = 200).
* **DTPREENCH**: Completion date (date = 10). Format: DD/MM/YYYY
* **REGISTRADO**: 
* **DTRECIDIVA**: Date of the last occurrence of recurrence (date = 10). Format: DD/MM/YYYY
* **RECNENHUM**: Without recurrence (int = 1). 0 - No; 1 - Yes
* **RECLOCAL**: Local recurrence (int = 1). 0 - No; 1 - Yes
* **RECREGIO**: Regional recurrence (int = 1). 0 - No; 1 - Yes
* **RECDIST**: Distance / metastasis recurrence (int = 1). 0 - No; 1 - Yes
* **REC01**: Recurrence / metastasis local (char = 3). Format: C99
* **REC02**: Recurrence / metastasis local (char = 3). Format: C99
* **REC03**: Recurrence / metastasis local (char = 3). Format: C99
* **REC04**: Recurrence / metastasis local (char = 3). Format: C99
* **HABILIT2**: Hospital qualification (int = 1). CACON or UNACON

.. toctree::
   :maxdepth: 2
   :caption: Libraries and functions

   Cancer Libraries and functions

.. toctree::
   :maxdepth: 2
   :caption: Data Analysis

   Cancer Models 2.0

.. toctree::
   :maxdepth: 2
   :caption: Classification ob

   Label - ob

.. toctree::
   :maxdepth: 2
   :caption: Classification RECNENHUM
   
   Label - RECNENHUM

.. toctree::
   :maxdepth: 2
   :caption: Classification RECDIST

   Label - RECDIST

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