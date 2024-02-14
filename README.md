# Real-World-Dataset-Exploration---Small-Project-in-ML

This ML Project on Real-World Dataset Exploration was aimed to apply different data manipulation techniques and perform Exploratory Data Analysis to uncover pattern, trends and anomalies in our data. It also aimed to employ statistical tests and data visualization techniques to make data-driven inferences and show these inferences in a clear manner.

For the dataset, I have used an open source Disease Dataset available for download from Kaggle (https://www.kaggle.com/datasets/kaushil268/disease-prediction-using-machine-learning) which contained two separate csv files for training and testing. The data set was aimed to help the physicians task easy by combining the field of medical science with machine learning. It contained over 133 columns and 4290 observations(4290X133). Out of 133 columns, 132 columns represent different kind of symptoms and contain binary value ( 0 or 1 Either symptom present/absent) and the final column is the 'prognosis' that classifies the disease.

For the preprocessing steps, I first checked for missing values and outliers. There was one column called 'Unnamed: 133' that had missing values NaN. and this was removed. The next thing we ensured was that all the datatypes were in the correct format and apply necessary data transformation techniques whereever applicable. Luckily all the datatypes of 133 feature columns were correct and didnt require any transformation.

After the preprocessing, we applied Exploratory data techniques to find userful infromation and develop two hypothesis from the analysis:

Some symptoms such as 'runny_nose', 'congestions', 'chills' and 'high_fever' are closely related. as shown in the coefficient matrix
Vomiting, Fatigue and high fever shows high variability in box plot. This could indicate that these symptoms are likely to be seen in many of the diseases.
This was effectively proven to be true using different statistical test from the scikit library. For the first hypothesis, we developed a contigency table and correlation matrix to show that the feature columns exhibit positive correlation. We also used chi-squared test to show there is a high association of between each features.

For the second hypotheis, we used the groupby() function to find useful statistical information about the columns. In the table, the variability of Vomiting, Fatigue and High Fever is non zero for many diseases, which confirms that these symptoms are present in many diseases and are likelihood of occurence is very high. Thus confirmed the second hypothesis.

Finally we plotted graphs and matrix using different visualization techniques from MatplotLib and Seaborne.

