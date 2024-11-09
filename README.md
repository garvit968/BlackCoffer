# Data Extraction and NLP

This project demonstrates how to web scrap various articles of various weblinks mentioned in `Scrapping/data/Input.xlsx`. Performing NLP on text of these articles and then storing it in output Output_Data_updated.xlsx

## Table of Content

- Project Structure
- Prerequisites
- Installation 
- Data Description 
- Evaluating the Model 
- Results 

## Project Structure

```bash
COFFER/
│
├── Scrapping/
│   ├── data                    # Input Xlsx sheet
│   ├── scrapper.ipynb          # Scapping Code
│   └── articles                # Scraped Article store
│
├── Transformation/
│   ├── MasterDictionary        # Sentiment Analysis Documents
│   ├── StopWords               # Stopwords Document
│   └── datatransform.py        # Script to evaluate the model
│
├── Output_Data_updated.xlsx    # Output Required Xlsx sheet
├── requirements.txt            # Python dependencies
└── README.md                   # Project documentation


```

## Prerequisites

- pandas 
- openpyxl 
- requests 
- beautifulsoup4
- nltk
- syllapy
- openpyxl
- urllib

## Installation

1. Install Dependencies 
```bash
pip install -r requirements.txt
```

2. Download the dataset (if not already included) and place it in the `data/` directory.

3. Download the MasterDictionary (if not already included) and place it in the `Transformation/` directory.

4. Download the StopWords (if not already included) and place it in the `Transformation/` directory.

5. Download the Output_Data.xlsx (if not already included) and place it in the `COFFER/` directory.



## Data Description

The dataset consists of the following columns:

- URL_ID: URL id of the given article, also used as placeholder to save.
- URL - URL respective to given URL id.


## EvaluAting the Model
The Tranformation script calculates the sentiment of text using tokenizers and various NLP based libraries. The model's performance can be assessed using metrics like:

- POSITIVE SCORE
- NEGATIVE SCORE
- POLARITY SCORE
- SUBJECTIVE SCORE
- AVG SENTENCE LENGTH
- PERCENTAGE COMPLEX WORDS
- FOG INDEX
- AVG WORDS PER SENTENCE
- COMPLEX WORD COUNT
- FILTERED WORD COUNT
- SYLLABLE PER WORD
- PERSONAL PRONOUNS
- AVG WORD LENGTH

Example script to evaluate the model:

```bash
python Transformation/datatransofrm.py
```

but before that you need to run following to extract text from articles:

```bash
python Scrapping/scrapper.ipynb
```

## Results
After training and evaluating the model, you should observe that the file Output_Data_Updated.xlsx should be created and you should see all the metrics calculated in that inbound.

