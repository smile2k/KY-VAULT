Besides assigning an initial value to a variable or assigning another variable to it, we can also perform the usual mathematical operations on variables. Basic operators in C# include +, -, *, / and % which represent addition, subtraction, multiplication, division and modulus respectively.

Example 
Suppose x = 7, y = 2 
Addition: x + y = 9 
Subtraction: x - y = 5 
Multiplication: x*y = 14 
Division: x/y = 3 (rounds down the answer to the nearest integer) 
Modulus: x%y = 1 (gives the remainder when 7 is divided by 2) 

In C#, division gives an integer answer if both x and y are integers. However, if either x or y is a non integer, we will get a non integer answer. 
For instance,
7 / 2 = 3 
7.0 / 2 = 3.5 
7 / 2.0 = 3.5 
7.0 / 2.0 = 3.5
