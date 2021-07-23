# Breast-Cancer-Detection-Using-Classification-Algorithms

In this readme file you will get to know about what every function is doing, so you can explain it to someone easily.

We have used supervised learning algorithms.

First we are importing the libraries.
Then We are loading the dataset.
The dataset is in dictionary format.
This dataset is Breast cancer wisconsin (diagnostic) dataset. There are 569 patients with breast cancer. we have 30 numeric attributes of the tumour. The target shows that tumours are classified into two types malignant and benign. Malignant means the person is having cancer and benign means it is a normal tumour.
These are the 30 features of the the tumour tissue.

Here we have appended the target column to those 30 features. For data Visualisation.
cancer_df.info shows the no. of values and their types for each feature.
cancer_df.describe shows the numeric distribution of data.
cancer_df.isnull shows if any of the feature is having a null value. but here we don't have any null value.
Data visualisation
pairplot- In paiplot all the features are plotted against each other, i.e. it creates a 30x30 plot and the orange dots are benign tumour and blue dots are depicting malign tumours.
in the next pairplot we have used some specific features to make it more visible.
as we can observe from the scatterplot that we can easily classify the data.

This graph shows that a person not having cancer has a mean radius of about 1. and a person having cancer has a mean radius of more than 1.

This is a heatmap. This heatmap is showing the numerical values of the features. And since all the features except mean area and worst area are close to 0. therefore it is showing data only for mean area and worst area beacuse they are in the multiples of 100s.

next we have correlation matrix which gives the correlation of different features with each other. The higher the correlation the more dependant the features are on each other.

in the next graph we have shown the correlation barplot of all the 30 features with with the target value. -ve correlation means that they are inversly dependant on each other. So the features that are showing less correlation should not be used to get better results.

Now we are making X and Y variables. X variable stores all the features and Y variable stores the target info i.e Malign or benign. After this we are splitting the dataset into test and train. We are using 80% data for training and 20% data for testing.
After this we are using standard scaling to scale our data. By doing this all the big and small values will have the same impact on the model, and no feature will be dominant over the other due to their numerical value.

after this we are feeding these variables into different classification algorithms. First we are predicting using normal data and after that we are using standard scaled data. After evaluating all the results we found out that XGBoost is best suited for our Dataset and it is giving an accuracy of 98.24%

confusion matrix is a table that is used to describe the performance of a classification model on a set of test data for which the true values are known. In this matrix it is showing that out of 114 values only 2 values are predicted incorrectly.

After this we are just saving the model using pickel....................



