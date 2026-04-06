It allows to declare a variable, while checking the data-type (class) of a reference variable, and automatically type-casts the reference variable into the specified data type (class)

```
/// CLASSIC WAY TO CHECK DATA TYPE


if (referenceVariable is Class1)
{
	Class1 c1 = (Class1) referenceVariable;
	c1.Property
}

/// THE PATTERN MATCHING WAY TO CHECK DATA TYPE

if (referenceVariable is Class1 c1)
{
	c2.Property... 
}

```

#### Example
```
namespace ClassLibrary1
{

//  parent class definition
	public  class ParentClass
	{
		public int x {get; set;}
	}
	
// child class
	public class ChildClass : ParentClass
	{
		public int y {get; set;}
	}
}

//somewhere in main program

ParentClass pc;
pc = new child() {x =10, y=20;};

Console.WriteLine(pc.x);
// output : 10 , <blank> 

//solution code with pattern matching syntax. where it convert parentclass reference variable into child class reference variable
if (pc is ChildClass cc)
{
	Console.WriteLine(cc.x);
	Console.WriteLine(cc.y);
}



``` 


#### Implicitly Typed Variable
#CS_3_0 
-  The variables that are declared with 'var' keyword are called as 'implicitly typed variables' (aka type-inference)
- this are declared without specifying the 'type' explicitly
- once value is assigned at the time of declaration.
- Generally `linq` query is used in entity framework.
- Cannot be used for method parameters return type of fields.
- it will be always with initialization while declaration.
- cannot have null value.
```
var p = namespacep.namespacec.method(parameter);
```


#### Dynamically Typed Variables
- Dynamically Typed variables are the variable that are declared with 'dynamic ' keyword.
-  Declared without specifying the type explicitly.
- C# compiler skill type-checking at compilation time. instead it resolves the data types of its values, at run time. in case of issue runtime error will occur
- ```
  dynamic dynVariable1 = value;
  ```
- Recommended to be used  for local variables, method parameters, fields , properties return types.



#### Inner Classes

-  inter related classes of a class, 'inner classes'.
- `OuterClassName.InnerClassName`  
- By default access modifier of innerclass will be private. to be used outside it should be declared public.
- 