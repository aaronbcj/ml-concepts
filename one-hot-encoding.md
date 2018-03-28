In Machine Learning and Deep Learning you might come across a feature or field having finite labeled values. One hot encoding is a process by which categorical values get encoded into binary values. 

### What is Categorical data?
Categorical data is data that takes only a limited number of values.

Some examples enclude:
- Like which is your favourite actor among: Tom Hanks, Al Pacino, Robert De Niro and Angelina Jolie.
- Classify images into either CAT, DOG, or TIGER
- Color variables with values as RED, GREE, BLUE, BLACK, ORANGE etc. 

We need to encode 4 options to some binary representation if you want to apply some ML/DL algorithm. 

Many machine learning (specially Deep Learning) algorithms cannot operate on label data directly. They require all input variables and output variables to be numeric. This means that categorical data must be converted to a numerical form. If the categorical variable is an output variable, you may also want to convert predictions by the model back into a categorical form in order to present them or use them in some application.

### Binary Representation (Encoding) of Categorical Data
Let explore how can we encode categorical values into binary format. 

#### Option 1: Integer Encoding
4 options can be represented by 2 bits (coz 2^2 = 4). So each option is assigned an integer value and the binary representation of integer value is the encoded value. 

```
00 - Tom Hanks
01 - Al Pacino
10 - Robert De Niro
11 - Angelina Jolie
```

#### Option 2: ONE-HOT Encoding
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
