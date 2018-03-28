One hot encoding is a process by which categorical variables are converted into a form that could be provided to ML algorithms to do a better job in prediction. Categorical variables represent numberical values typically from 0 to N-1.

### What is Categorical data?
Categorical data is data that takes only a limited number of values.

Assume that you have a field which can take 4 possible values. It could be as trivial as selecting one option from 4 listed options on a online platform. Like which is your favourite actor among: Tom Hanks, Al Pacino, Robert De Niro and Angelina Jolie.

We need to encode 4 options to some binary representation if you want to apply some ML/DL algorithm. 

### Option 1
4 options can be represented by 2 bits (coz 2^2 = 4)
00 - Tom Hanks
01 - Al Pacino
10 - Robert De Niro
11 - Angelina Jolie

### Option 2
Use one bit position to represent one option
1000 - Tom Hanks
0100 - Al Pacino
0010 - Robert De Niro
0001 - Angelina Jolie

### Option 2 is known as ONE-HOT ENCODING. 
