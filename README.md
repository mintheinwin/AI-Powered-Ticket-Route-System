# RoBERTa-Based IT Ticket Classification

## Introduction

This project implements a **RoBERTa-based text classification model** for automatically classifying software defect and support tickets. The model uses ticket **Summary, Description, and Comments** to predict the appropriate **Assigned Team** and **Team Email**.

The project uses a labeled dataset to train and evaluate the model, with mock data used to protect sensitive information.

## Problem Statement

In large-scale software development and IT support environments, defect and support tickets are continuously generated to track issues, bugs, and user requests. These tickets typically contain textual information such as summaries, descriptions, and comments written by developers, testers, and support engineers.

Manually assigning tickets to the appropriate team can be time-consuming and may result in inconsistent classification. Automating this process can help reduce ticket resolution time, improve workflow efficiency, and ensure that issues are routed to the appropriate support team.

## Objective

The main objective of this project is to develop a **RoBERTa-based ticket classification model** that can:

* Classify tickets based on their textual content.
* Predict the appropriate **Assigned Team**.
* Retrieve the corresponding **Team Email**.
* Reduce manual ticket-routing efforts.
* Improve the efficiency and consistency of defect management.

## Model Development

The project focuses on developing a transformer-based classification pipeline using **RoBERTa**.

The main development steps include:

1. **Data Preparation** – Preparing labeled ticket data containing Summary, Description, Comments, Assigned Team, and Team Email.
2. **Text Preprocessing** – Cleaning and preparing textual features for model training.
3. **Feature Engineering** – Combining Summary, Description, and Comments as input features.
4. **Model Pre-Training** - Loading a pre-trained RoBERTa model and tokenizer and Preparing and tokenizing the ticket text.
5. **Model Training** – Fine-tuning RoBERTa for ticket classification.
6. **Optimization** – Using gradient-based optimization and learning-rate scheduling to improve training performance.
7. **classification Report** - Generate a classification report using Assigned Team names.
8. **Evaluation** – Evaluating the model's ability to correctly classify tickets into the appropriate teams.

## Application Development

1. **Model Testing** – Test the trained model using the `.pth` model format to verify its prediction performance.
2. **Model Export** – Export and serialize the trained model using the Pickle (`.pkl`) format for application integration and deployment.
3. **Model Deployment** – Integrate and deploy the trained model in **Streamlit** and **Radio** applications for user interaction and real-time   ticket classification.


## Dataset

Due to data sensitivity and confidentiality considerations, this project uses a **mock dataset(Defect_ticket_v2.csv)** that represents real-world IT defect and support tickets.

The dataset contains fields such as:

* `Summary`
* `Description`
* `Comment`
* `Assigned Team`
* `Team Email`

## Future Improvements

Potential improvements for future development include:

* Hyperparameter tuning.
* Data augmentation.
* Increasing the size and diversity of the training dataset.
* Comparing RoBERTa with other transformer-based models.
* Improving classification performance for underrepresented teams.
* Developing a real-time ticket classification and team-routing system.

## Conclusion

This project demonstrates how **RoBERTa and natural language processing (NLP)** can be applied to automate IT ticket classification and routing. By predicting the appropriate support team from ticket content, the proposed approach has the potential to improve operational efficiency and reduce the time required for manual ticket assignment.

## Test Model from HuggingFace Streamlit Application:

* Link: 
https://huggingface.co/spaces/mintheinwin/Ticket-AI-Powered-Routing-streamlitApp

### Get Testing Input from Dataset
For model testing, the application reads test data from the `Defect_ticket_v2.csv` dataset. The input text is obtained from the following columns:
* `Description`
* `Comment`
* `Summary`

These three fields are combined and provided as input to the trained RoBERTa model for prediction. The model then predicts the **Assigned Team**, which can be used to retrieve the corresponding **Team Email**.

