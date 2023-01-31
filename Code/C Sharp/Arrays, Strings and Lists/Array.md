
## Initializing
```CSharp
int[] userAge = {21, 22, 23, 24, 25};
```

```CSharp
int[] userAge = new int[5]; 
userAge = new [] {21, 22, 23, 24, 25};
```

## Array Properties and Methods 
To use a property, we type the property name after the dot. To use a method, we type the method name after the dot operator, followed by a pair of parenthesis ().

### **Length()**
### **Copy()**
The first argument is the array that provides the values to be copied. 
The second is the array where the values will be copied into. 
The last argument specifies the number of items to copy.
```CSharp
int [] source = {12, 1, 5, -2, 16, 14};
int [] dest = {1, 2, 3, 4};
Array.Copy(source, dest, 3);
```

```
Result
{12, 1, 5, 4}
```
### **Sort()**
The array will be sorted in ascending order
```CSharp
int [] numbers = {12, 1, 5, -2, 16, 14};
Array.Sort(numbers);
```

```
Result
{-2, 1, 5, 12, 14, 16}
```

### IndexOf()
```CSharp
int [] numbers = {10, 30, 44, 21, 51, 21, 61, 24, 14};
Console.WriteLine(Array.IndexOf(numbers, 21));
Console.WriteLine(Array.IndexOf(numbers, 21));
```

```
Result
3 
-1 // If it does not exist, the method returns -1.
```

