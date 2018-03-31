Machine learning mostly deals with scalar values either in form of vector or matrix. Now, what if you have a feature or field in your dataset which has finite labelled values. Such **categorical values** are usually finite so it needs to be encoded into binary format. Take case of Natural Language Processing which deals only with text; you we want to apply Machine learning techniques then words need to be encoded. 

This post talks about different binary encoding techniques. 

### What is Categorical data?
Categorical data is data that takes only a limited number of values.

Some examples enclude:
- Like which is your favourite actor among: Tom Hanks, Al Pacino, Robert De Niro and Angelina Jolie.
- Classify images into either CAT, DOG, or TIGER
- Color variables with values as RED, GREE, BLUE, BLACK, ORANGE etc.
- Dictionary of top 5000 words found on wikipedia

Many machine learning (specially Deep Learning) algorithms cannot operate on label data directly. They require all input variables and output variables to be numeric. This means that categorical data must be converted to a numerical form. If the categorical variable is an output variable, you may also want to convert predictions by the model back into a categorical form in order to present them or use them in some application.

### Binary Representation (Encoding) of Categorical Data
Let explore how can we encode categorical values into binary format. 

#### Option 1: Integer Encoding
If there are 4 possible values of a category then it can be represented by 2 bits (coz 2^2 = 4). So each option is assigned an integer value and the binary representation of integer value is the encoded value. 

```
00 - Tom Hanks
01 - Al Pacino
10 - Robert De Niro
11 - Angelina Jolie
```

#### Option 2: ONE-HOT Encoding
One-hot representation is a representation method in which only one element is 1 and the other elements are 0 in the vector. By setting 1 or 0 for each dimension, it represents “that word or not”.

Use one bit position to represent one option
```
1000 - Tom Hanks
0100 - Al Pacino
0010 - Robert De Niro
0001 - Angelina Jolie
```
The binary variables are often called **dummy variables** in other fields, such as statistics.


### References
https://www.kaggle.com/dansbecker/using-categorical-data-with-one-hot-encoding
https://machinelearningmastery.com/why-one-hot-encode-data-in-machine-learning/
