## 1. Directive
They tell the compiler that our program uses a certain namespace.

For instance, the first line 
``` CSharp
using System;
``` 
tells the compiler that our program uses the System namespace.

## 2.Namespace
A namespace is simply a grouping of related code elements. These elements include classes, interfaces, enums and structs etc (we’ll cover each of these elements in subsequent chapters).

For instance, the code below defines two namespaces, both of which contain a class named MyClass. This is allowed in C# as the two classes belong to different namespaces (First and Second).
```CSharp
namespace First 
{ 
	class MyClass { } 
} 
namespace Second 
{ 
	class MyClass { } 
}
```

## 3. The Main() Method
The Main() method is the entry point of all C# console applications. Whenever a console application is started, the Main() method is the first method to be called.

## 4. Comments
