# Initializing
- An [[Array]] can only hold a fixed number of values. If you need greater flexibility in your program, you can use a list. To declare a list of integers, we write
```CSharp
List userAgeList = new List();
// or 
List userAgeList = new List {11, 21, 31, 41};
```

# List Properties and Methods
## Add()
```CSharp
userAgeList.Add(51); 
userAgeList.Add(61);
```

```
userAgeList now has 6 members: {11, 21, 31, 41, 51, 61}.
```
## Count()
- To find out the number of elements in the list, use the Count property.
## Insert()
To add members at a specific position, use the Insert() method. 
To insert a member at the 3rd position, you write 
```CSharp
userAgeList.Insert(2, 51); 
```
where 2 is the index and 51 is the value you want to insert. 
userAgeList now becomes {11, 21, 51, 31, 41, 51, 61}.

## Remove()
The Remove() method takes in one argument and removes the first occurrence of that argument.
```CSharp
// Before: {11, 21, 51, 31, 41, 51, 61}.
userAgeList.Remove(51);
// After: {11, 21, 31, 41, 51, 61}.
```
## RemoveAt()
```CSharp
userAgeList.RemoveAt(3);// remove at index = 3.
```
## Contains()
To check if a list contains a certain member
```CSharp
userAgeList.Contains(51);
// Have 51 --> True
// No have 51 --> False
```
## Clear()
```CSharp
userAgeList.Clear(); // we will have no elements left in the list.

```
