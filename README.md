# Comparative Sentiment Analysis and Information Extraction of Drug Reviews

## Overview

This project aims to analyze and compare patient reviews of medications for chronic conditions such as **Eczema** and **Diabetes**. With the rising prevalence of these conditions and the growing usage of medications, patients frequently share their experiences and opinions online. These reviews provide crucial insights into drug efficacy, side effects, and public perception. However, the vast amounts of unstructured data make it difficult for consumers and healthcare professionals to make informed decisions.

This research applies advanced **Sentiment Analysis** and **Information Extraction** techniques to identify side effects and public sentiments related to these medications. By doing so, it hopes to contribute valuable insights to healthcare professionals, pharmaceutical researchers, and consumers for better-informed decisions.

## Objectives

- **Sentiment Analysis**: To classify the sentiments (positive, negative, or neutral) within the reviews of drugs used for Eczema and Diabetes treatment.
- **Side Effect Extraction**: To extract specific side effects mentioned in the reviews and compare medications for similar medical conditions.
- **Comparative Analysis**: To examine the perceived effectiveness and side effects of various drugs used for treating Eczema and Diabetes.

## Data Collection

The dataset for this project was collected from reputable sources such as **WebMD** and **Drugs.com**. The data includes over **1800 reviews** for **10 drugs** used for both Eczema and Diabetes. These reviews provide firsthand accounts of patients' experiences and their sentiments regarding the medications.

The reviews were scraped using **Python’s requests** and **BeautifulSoup** libraries, and then cleaned and structured for further analysis.

## Data Preprocessing

Before analyzing the reviews, the data underwent essential preprocessing steps:

- **Text Cleaning**: Removal of irrelevant characters and noise.
- **Tokenization**: Breaking the reviews into smaller units for further analysis.
- **Normalization**: Standardizing word forms to ensure consistency.
- **Custom Stop Words List**: A customized list was created, excluding the word "not" to preserve negations in sentiment analysis.
  
A manual annotation of side effects was carried out for validation since automatic sentiment analysis was found to be less effective for drug reviews due to their nuanced nature.

## Exploratory Data Analysis (EDA)

We performed comprehensive EDA to understand the distribution of side effects and sentiments in the reviews:

- **Skin and abdomen-related side effects** were prevalent in both diabetes and eczema medications.
- Diabetes drugs like **Trulicity** and **Januvia** showed specific patterns in side effects, such as **gastrointestinal** or **musculoskeletal discomfort**.
- Eczema drugs like **Dupixent** showed significant **psychological** side effects.

### Sentiment Distribution

- **Diabetes drug reviews**: 74% of reviews expressed **negative sentiment**, indicating concerns or dissatisfaction.
- **Eczema drug reviews**: Reviews exhibited a mixed sentiment distribution, though **26%** were negative.

These findings suggest the need for better medication management strategies to address both physical and psychological aspects of these diseases.

## Modeling and Results

### Multilabel Classification

For side-effect classification, we used a **Linear Support Vector Classifier (SVC)** with the **One-vs-Rest (OvR)** strategy. This approach improved the accuracy from **52%** to **56%** by balancing class weights, especially for rare side effects like **Upper Respiratory-Related** and **Metabolic-Related**.

### Retrieval Augmented Generation (RAG)

To further enhance the model’s capability, we explored the use of **Retrieval Augmented Generation (RAG)**. This model combines **retrieval** of relevant documents, **augmentation** of the data, and **generation** of output. By integrating vector databases like **Qdrant** and **FastEmbed**, we improved our ability to provide more accurate and contextually relevant results, especially for complex side-effect and sentiment-related queries.

## Key Technologies Used

- **Natural Language Processing (NLP)**: Sentiment analysis using **Vader**, **TextBlob**, and **SVC**.
- **Information Extraction**: Extraction of side effects from unstructured reviews.
- **Machine Learning**: **Multilabel Classification** using **Linear SVC** with class balancing.
- **Vector Databases**: **Qdrant** and **FastEmbed** for enhancing the Retrieval Augmented Generation model.

## Insights

This project demonstrates that analyzing patient reviews using NLP and machine learning techniques can uncover valuable insights into the side effects and public perception of medications. The findings emphasize the importance of addressing both **physical** and **psychological** side effects in the treatment of chronic conditions like **Diabetes** and **Eczema**.

## Conclusion

By leveraging sentiment analysis and information extraction, this research aims to contribute to a better understanding of the real-world effectiveness and safety of drugs. The project’s methodology can be applied to other medical domains, providing insights for healthcare professionals and patients alike.

## Future Work

- **Model Improvement**: Further enhancements in the sentiment analysis models could be explored using more advanced techniques such as **BERT** or **GPT**.
- **Larger Datasets**: Expanding the dataset to include more diverse drug reviews from additional sources.
- **Real-time Data Integration**: Incorporating real-time data streams for continuous monitoring of drug side effects.

