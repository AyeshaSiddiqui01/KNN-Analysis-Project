# Exploring K-Nearest Neighbors (KNN): Regression & Classification
# About This Project
This project is part of my ongoing journey to understand machine learning fundamentals specifically, how the K-Nearest Neighbors (KNN) algorithm works for both regression and classification tasks.

Using real-world health data, I experimented with KNN to predict cognitive scores (MMSE) and classify dementia stages (CDR_binary). It’s been a great hands-on experience to understand how KNN makes predictions based on data “neighbors.”
# What I Did

**Preprocessed the dataset:** handled numeric and categorical variables, scaled the features using StandardScaler, and split the data into training and testing sets.

**Trained KNN models for:**

Classification: predicted CDR_binary (0 or 1)

Regression: predicted MMSE scores

**Fine-tuned** the number of neighbors (k) by finding the Optimal K  to balance model accuracy and overfitting. I tested different values of K (from 1 to 20) to identify which number of neighbors gave the best performance. <img width="544" height="350" alt="knn_finetuning_plot" src="https://github.com/user-attachments/assets/3da74897-171b-4fb8-b36a-f5507d3fd936" />


**Visualized** how performance changed as k varied. 

# Key Insights

Before fine-tuning, my regression model had an R² score of 0.46. After several tuning attempts, the score even dropped eventually turned negative. This helped me realize how sensitive KNN can be to scaling and parameter choices.

The predicted MMSE values tended to cluster near the middle, confirming KNN’s tendency to “average out” extremes. Most actual MMSE scores were between 26–30, showing many participants with higher cognitive scores.

# What I Learned

This project taught me more than just model building, it showed me:

How feature scaling can dramatically affect distance-based algorithms.

Why it’s important to experiment with hyperparameters like k.

That even “lower” model scores are part of the learning process — each result reveals something valuable about the data and model behavior.

A scatter plot comparing actual vs. predicted MMSE scores showed:

Most predictions followed the general trend but deviated slightly from the ideal line.

The model tended to underestimate higher scores and overestimate lower ones, a common KNN regression pattern. <img width="403" height="400" alt="knn_mmse_plot" src="https://github.com/user-attachments/assets/6c8afb3b-c062-47d7-94aa-c9ad140d11a4" />

