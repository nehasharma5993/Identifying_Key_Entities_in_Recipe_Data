# Project Name : Identifying Key Entities in Recipe Data using Syntactic Processing

## Table of Contents
* [General Info](#general-information)
* [Steps Involved](#steps-involved)
* [Technologies Used](#technologies-used)
* [Conclusions](#conclusions)
* [Acknowledgements](#acknowledgements)
  

## General Information
- This data set comprises culinary recipes with a focus on ingredient extraction and analysis.
- Each recipe features a structured ingredient list with labelled components, identifying ingredients, quantities and units.
- The business objective is to leverage the increasing popularity of online cooking platforms and meal-planning apps by enhancing the user experience.
- This can be achieved by implementing a custom-named entity recognition (NER) model to automatically tag ingredients, quantities and recipe names.
- This automation will streamline the process of organising recipes, improve searchability and enable users to easily find recipes based on available ingredients, portion sizes or specific dietary requirements.


## Steps Involved
- Import Necessary Libraries
- Data Ingestion and Preparation
- Train-Validation Split (70 train:30 validation)
- Exploratory Data Analysis on the Training Data Set
- Feature Extraction for the CRF Model
- Model Building and Training
- Prediction and Model Evaluation
- Error Analysis on the Validation Data


## Conclusions
#### Training Performance
- Overall Accuracy: 96%
- The model performs very well on training data, with high precision, recall, and F1-scores across all classes.
- Ingredient is the dominant class with highest accuracy (98% recall).
- Quantity and Unit are less frequent and show slightly lower recall (91% and 88% respectively), but still strong.

#### Validation Performance
- Overall Accuracy: 93% (slightly lower than training, as expected).
- Ingredient still performs best with 97% recall, indicating strong generalization.
- Quantity and Unit show a drop in recall (88% and 80%), suggesting some confusion, especially with similar tokens.


## Recommendations
- Handle Class Imbalance: The model performs best on the ingredient class because it dominates the dataset. Use class weighting or upsample underrepresented classes (quantity, unit) to help the model pay more attention to them.
- Use Contextual Models: Incorporate previous and next tokens explicitly into features if you're using CRF or traditional ML.
- Analyze Errors: Misclassifications often occur between semantically similar labels (quantity vs ingredient). Introduce domain-specific rules or features (e.g., regex for numbers/units) to assist classification.
- Data Augmentation: Augment training data by creating synthetic examples or leveraging semi-supervised techniques.


## Technologies Used
- numpy
- pandas
- matplotlib
- sklearn
- re (for regular expressions)
- joblib


## Acknowledgements
- I would like to express gratitude to the UpGrad IITB Programme for providing me with the opportunity to implement Syntactic Processing as part of our coursework. 
- This case study has enriched our understanding and practical application of data analysis and machine learning techniques, contributing significantly to our learning experience.


## Contact
Created by [@nehasharma5993]


## License
This project is open source and available without restrictions.
