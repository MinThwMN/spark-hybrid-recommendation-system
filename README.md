# Spark Hybrid Recommendation System

## Overview

This project develops a scalable hybrid recommendation system for e-commerce platforms using Apache Spark. The system combines Collaborative Filtering (ALS) and Content-Based Filtering to generate personalized product recommendations while addressing the cold-start problem.

The project also incorporates Big Data optimization techniques such as Parquet storage and Spark caching to improve processing efficiency and scalability.

## Objectives

* Build a product recommendation system using Apache Spark.
* Generate personalized Top-K product recommendations.
* Mitigate the cold-start problem through content-based filtering.
* Improve data processing efficiency using Parquet and Spark Cache.
* Evaluate recommendation quality using RMSE.

## Dataset
The dataset is too large to be stored in this repository.

Source:
https://nijianmo.github.io/amazon/index.html

Dataset used:
Arts, Crafts and Sewing Reviews

Dataset characteristics:

* ~494,000 reviews
* ~22,900 products
* ~56,000 users

The project utilizes:

* Review data for Collaborative Filtering
* Product metadata for Content-Based Filtering

## Technologies

* Python
* PySpark
* Apache Spark
* Spark SQL
* Spark MLlib
* Parquet
* Google Colab

## Methodology

### Data Processing

* Load and preprocess Amazon review data
* Convert JSON datasets into Parquet format
* Join review data with product metadata
* Encode users and products using StringIndexer

### Collaborative Filtering

Implemented using Alternating Least Squares (ALS) in Spark MLlib.

Key features:

* Matrix Factorization
* Latent Factor Learning
* Top-K Recommendation Generation

### Content-Based Filtering

Utilizes product metadata including:

* Brand
* Category

A content score is generated based on user preferences for similar products.

### Hybrid Recommendation System

A weighted hybrid strategy combines:

Hybrid Score = α × ALS Score + (1 − α) × Content Score

The optimal alpha value is selected through validation experiments.

## Optimization Techniques

### Parquet Storage

* Reduced storage requirements
* Faster data loading
* Improved Spark SQL performance

### Spark Cache

* Eliminated redundant computations
* Reduced training time
* Improved iterative processing efficiency

## Evaluation

The recommendation system is evaluated using:

* RMSE (Root Mean Squared Error)
* Execution Time
* Resource Utilization

## Key Contributions

* Implemented ALS-based collaborative filtering on Spark.
* Designed a hybrid recommendation architecture combining collaborative and content-based approaches.
* Addressed cold-start limitations.
* Applied Big Data optimization techniques for scalable processing.

## Author

Le Nguyen Minh Thu
