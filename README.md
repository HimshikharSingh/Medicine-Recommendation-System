# Medicine Recommendation System

## Overview
This project develops a Medicine Recommendation System using Natural Language Processing (NLP) techniques to recommend medications based on their descriptions and similarities to other medications.

## Data Processing
- **Data Loading and Display**: Medication data is loaded into a pandas DataFrame from a CSV file, and initial explorations such as viewing the head of the DataFrame and checking its shape and missing values are conducted.

## Text Preprocessing and Visualization
- **Normalization and Text Processing**: Text in the `Description` and `Reason` fields undergoes normalization, including conversion to lowercase, removal of special characters, and tokenization. These fields are then combined into a `tags` column.
- **Visualization**: The frequency of reasons for medications is visualized using a count plot, and a word cloud is generated to visualize the most common words in the `Description`.

## Data Cleaning
- **Handling Missing Values**: Missing values are identified and rows containing them are removed. Duplicate entries are also checked.

## Feature Engineering
- **Vectorization**: The `tags` field is vectorized using a CountVectorizer, transforming the text into numerical data that facilitates the calculation of cosine similarity.
- **Stemming**: The PorterStemming technique is applied to words in the `tags` column to reduce them to their root forms.

## Similarity Calculation
- **Cosine Similarity**: The cosine similarity between the vectorized text data is calculated, and the distribution of these similarity scores is visualized using a histogram to understand the range and concentration of values.

## Recommendation
- **Top Similar Medications**: A function is defined to recommend the top N similar medications based on cosine similarity scores. This function identifies and lists the most similar medications for a given input, and their similarities are visualized using a horizontal bar chart.

## Conclusion
The system provides a practical approach to finding similar medications based on textual descriptions. It leverages advanced NLP techniques to analyze and recommend medications, aiding healthcare professionals in making informed decisions.

## How to Use
- Input the name of a medication to the recommendation function.
- Receive a list of top similar medications along with their similarity scores.

