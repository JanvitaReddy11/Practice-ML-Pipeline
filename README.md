# Spam Classification using DVC

## Overview

This project implements an end-to-end machine learning pipeline for text classification, specifically for detecting spam messages. The pipeline is managed using DVC (Data Version Control) to enable reproducibility and experiment tracking.

## Project Structure

src/: Contains all the Python scripts for different stages of the pipeline.

data/: Stores raw, interim, and processed data (ignored in Git).

models/: Stores trained model files (ignored in Git).

reports/: Contains evaluation metrics (ignored in Git).

dvc.yaml: Defines the pipeline stages.

params.yaml: Stores hyperparameters and configurations.

## Pipeline Stages

Data Ingestion: Loads and preprocesses the dataset.

Data Preprocessing: Removes stopwords, applies stemming, and tokenizes text.

Feature Engineering: Extracts features using TF-IDF vectorization technique.

Model Training: Trains a Random Forest classifier using the processed data.

Model Evaluation: Computes accuracy, precision, and recall metrics.

## DVC Integration

Initialized DVC (dvc init).

Created dvc.yaml to automate pipeline execution.

Configured params.yaml to store hyperparameters.

Used dvc repro to execute and track pipeline runs.

Integrated dvclive for tracking experiments (dvc exp run).

## Running the Pipeline

# Clone the repository
$ git clone <repo-url>
$ cd <repo-directory>

# Install dependencies
$ pip install -r requirements.txt

# Run the pipeline
$ dvc repro

# Track experiments
$ dvc exp run
$ dvc exp show

## Conclusion

This project demonstrates a robust and reproducible approach to text classification using DVC. It ensures efficient model tracking and experiment management, making it easy to iterate and improve the classifier.