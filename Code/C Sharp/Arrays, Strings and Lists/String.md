# initialize a string variable
```CSharp
string message = "Hello World";
string anotherMessage = ""; // empty string
```

we can join two or more strings using the concatenate sign (+) and assign them to a variable.
```CSharp
string myName = "Hello World, " + "my name is Jamie";
```

# String Properties and Methods
## Length()

```CSharp
"Hello World".Length
```

## Substring()

```CSharp
string message = "Hello World";
string newMessage = message.Substring(2, 5);
// extracts a substring of 5 characters from message, starting from index 2
```

```
Result 
"llo W"
```

## Equals()
We can use the Equals() method to compare if two strings are identical.
```CSharp
string firstString = "This is Jamie"; 
string secondString = "Hello"; 
firstString.Equals("This is Jamie"); // returns true
firstString.Equals(secondString); //returns false
```

## Split()
The Split() method splits a string into substrings based on an array of user-defined separators. After splitting the string, the Split() method returns an array that contains the resulting substrings.
Chia chuỗi 
```CSharp
string [] separator = {“, ”, “; ”}; 
string names = “Peter, John; Andy, , David”; 3 
string [] substrings = names.Split(separator, StringSplitOptions.None);
string [] substrings = names.Split(separator, StringSplitOptions.RemoveEmptyEntries);

```

```CSharp
{“Peter”, “John”, “Andy”, “” , “David”}
{“Peter”, “John”, “Andy”, “David”}
```