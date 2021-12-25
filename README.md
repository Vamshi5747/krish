# Mathematical classification
Classification is the arrangement or sorting of objects into groups based on a shared property. If you have a collection of items(questions), you can categorise the algebra in one category, the geometry in another, and so on.
With the help of classification, we can teach children about a variety of topics. The three most important factors are as follows:

It aids in the identification and verification.
It aids in understanding and studying the characteristics, similarities, and differences between various items.
It describes how the questions are grouped and classified into various categories.

# Natural Language Processing
Natural Language Processing, also known as NLP, is a branch of Artificial Intelligence that focuses on enabling systems to understand and process human languages. In this article, I will use NLP to analyse and classify the questions. 

# Dataset
The dataset was originally made up of 11090 questions (rows) and 5 columns.
There are 23 different types of questions in total, which are as follows: 
 
- understanding of quadratic equations
- word problem  
- simple system of equations with two variables  
- linear equation in one variable
- knowledge of quadratic equations
- permutations and combinations
- probability
- least common multiple
- knowledge of percentage 
- knowledge of fractions and ratios
- permutations and combinations problem with digits
- knowledge of upstream and downstream speeds
- sequences and progressions
- scaled models and application of scaling
- distance and time
- knowledge of fractions and ratios
- exponential growth and decay
- relative speed
forward discount percentage
mixed fractions
set theory venn diagram
knowledge of decimal numbers
slope of line  parallel line  perpendicular line  given points

# Preparation for Embedding 

The most common methods in Natural Language Processing (NLP) for converting sentences to machine readable code are TF-IDF, Word Embedding, Word2vec and Glove.

A word is converted to an n-dimensional vector using Glove, Word2vec, and Word Embedding. Similar n-dimensional vectors map to related words, while dissimilar words map to dissimilar vectors. 
A model may then utilise this information to learn the link between words

We're utilising Term Frequency — Inverse Document Frequency (TF-IDF) in this note book to convert a collection of text documents to a matrix representation. After each document is translated to a row of the TF-IDF matrix, each word is stored in a column vector.

Why i choose this TF -IDF vectorizor 
Tf-idf is a word scoring technique that determines how essential a word is to a question.
for example
Question 1: percentage  of what number is 34 
Question 2: the sum of two numbers is 8 . 5 and their product is 18 . what are the numbers ?
number, what, and numbers are all frequent terms with low TF-iDf ratios, while sum and product words have a high TF-iDf ratio.
We can easily classify the questions this way. Giving unusual terms a high priority will make it easier to classify the queries.

# Preprocesing
- Performed data cleaning(unwanted text removal, lower(), and stop words remove)
- Tokenization: 
- Stemming: 
- Lemmatization:


# Model 
###### Linear SVM Classification
Use a straight line to divide (linearly separable)
Support Vector Machine, also known as Support Vector Classification, is a supervised and linear Machine Learning algorithm that is commonly used to solve classification problems.

![image](https://user-images.githubusercontent.com/95626757/147388120-9bbfaa62-211a-43f9-994b-b29d98ce75b2.png) 

Tfidf vectors 

![Screen Shot 2021-12-25 at 9 57 27 PM](https://user-images.githubusercontent.com/95626757/147389367-50502726-8adf-41d3-ba43-00b9ea67f012.png)


X-axis: TF-iDf ratios
Y-axis: encoded labels 

![Screen Shot 2021-12-25 at 8 47 45 PM](https://user-images.githubusercontent.com/95626757/147388175-a6acb0cf-2fb1-41da-a12d-af7716a78055.png)

Fitting the training data to the Support Vector Machine after it has been initialised  
![Screen Shot 2021-12-25 at 9 58 53 PM](https://user-images.githubusercontent.com/95626757/147389384-6ba1e3f3-33a7-471e-9117-85bf9f9a2327.png)

Why i choose this svm model. 

It is capable of solving both linear and nonlinear problems and is useful for a wide range of practical applications. The basic idea behind SVM is straightforward: the algorithm draws a line or a hyperplane that divides the data into classes.

![Screen Shot 2021-12-25 at 10 07 54 PM](https://user-images.githubusercontent.com/95626757/147389522-5bf3b7b9-836e-4ad5-af1b-eb845ec6c9db.png)


Identifying and categorising predictors and targets


