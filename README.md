# Amazon Personalized Recommendation System

## Introduction
This project involves building a live product recommender system based on customer preferences using a 128 GB Amazon product dataset. The system leverages big data processing techniques to provide real-time product recommendations, using powerful tools like Apache Spark, MongoDB, and Apache Kafka.

## Objective
The primary objective of this project is to create a robust recommendation system that can handle large-scale data and provide personalized product recommendations to users based on their reviews. The system aims to analyze customer reviews, train a recommendation model, and deliver real-time recommendations through a web application.

## Methodologies
1. **Load Dataset**:
   - Load the Amazon dataset using Apache Spark with `StructType` for type safety, ensuring correct data processing and reducing runtime errors.
   - Schema definition and initial data inspection.

2. **Clean Dataset**:
   - Handle missing numeric values by filling with 0 and string values with empty strings.
   - Remove punctuations and URLs, convert text to lowercase.

3. **Load Data into MongoDB**:
   - Efficiently load the cleaned dataset into MongoDB for further analysis.

4. **Exploratory Data Analysis (EDA)**:
   - **Sentiments of Reviews**: Analyze the sentiment of reviews using the ratings.
     - Result: Most products are positively reviewed with an average rating of 5.
   - **Scatter Plot of Reviews vs. Review Length**:
     - Result: Visual representation of review length distribution.
   - **Top 10 Most Reviewed Products**: Analyze the sentiment and profitability of the top 10 most reviewed products.
     - Result: Most reviewed products are generally well-rated.
   - **Top 10 Least Reviewed Products**: Examine the sentiment of the least reviewed products.
     - Result: Some products with fewer reviews are not well-rated.

5. **Model Training**:
   - Initial attempts to train the model on the entire dataset were unsuccessful due to memory constraints.
   - The model was trained on a smaller subset of the data using collaborative filtering techniques (ALS algorithm).

6. **Kafka Connection and MongoDB Integration**:
   - Develop a Flask-based web application to interact with users.
   - Use Apache Kafka for streaming real-time recommendations based on user input.
   - Store recommended products in MongoDB and display them to users through Kafka consumers.

## Technologies Used
- **Apache Spark**: For efficient data processing and loading into MongoDB.
- **MongoDB**: To store and manage the cleaned dataset and user preferences.
- **Pandas and Matplotlib**: For exploratory data analysis and data visualization.
- **Flask**: To create a web application for user interaction.
- **Apache Kafka**: For real-time streaming of product recommendations.
- **Machine Learning**: Using the ALS algorithm for collaborative filtering to build the recommendation model.

## Conclusion
This project successfully demonstrates the integration of big data processing, machine learning, and real-time streaming to build a personalized product recommender system. Despite the challenges with handling a large dataset, the system efficiently processes and analyzes data to provide valuable insights and recommendations. The use of Apache Spark, MongoDB, and Apache Kafka highlights the capability to manage and process large-scale data, offering a scalable solution for real-time product recommendation.

