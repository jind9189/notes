
Methods are also called function.
Methods perform manipulation of the field of object.

#MethodAccessModifier

### About Methods
- Access modifier
	- #MethodAccessModifier
- Modifier 
	- Methods have 7 types of modifier like static, virtual, abstract, override, new, partial , sealed.
	- Modifier are optional and have no default modifier.
- ReturnType:
	- Data type of return value result that  method will return. Void indicate that method do not return any value to caller
- Static methods:
	- static methods can manipulate static fields only
	- it can be accessed with object only.

#### Local Function 
C# 7.0
- Function is small function inside the function. so this will become reusable code inside the parent function.
- it do not have Access Modifier. so it is defined with return Datatype and method Name
- local function can use the variable

#### Static Local function
- they are not like static modifier of methods .
- it has restriction in accessing local variable of parent function. 

#### Recursion 
- When methods calls itself
- Useful in mathematics computations, such as finding factorial of a number



### Constructors
Constructors are special methods of class
- [[Constructors]]
### Destructors
Destruction are special methods of class.
- [[Destructors]]

### Properties
- Receive the incoming value, validate the value, assign value into field.
- Property is collection of two accessor (get and set accessor) #ValidationProcess
```
class Student{
	private string _fname;
	
	public string FirstName
	{
		set
		{
			// validation/ Manipulation logic before assigning value
			// example : make fname with right case like 
			// also check if contains only Alphabet characters only, etc
			this._fname = value //here he value mean the value passed as FirstName
			
		}
		
		get
		{
			return _fname;
		}
	}
}

// somewhere in main 
Student student1 = new Student();
student1.FirstName = "mukesh";
```
- Auto-implemented Properties:
	- feature of #CS_3_0
	- do not have definition of properties 
	- Automatically create `_PropertyName` while compilation time 
	- if set accessor is used , property is write-only , but if only get accessor is used, it become read-only property
```

	public string FirstName
	{
		accessModifier set;
		accessModifier get;
	
	}
```
-  Auto-Implemented Property Initializer
	- feature of #CS_6_0
	- Used to create property easily .
	- Creates a private field with as `propertyName` automatically , during compilation-time
	```
		//in class definition
		public string City{ get ; set;} = "Ahmedabad";
		
		//somewhere in main
		student1.city = "Jaipur";
		System.Console.Writeline(student1.City) // print : Jaipur
		System.Console.Writeline(student2.City) // print : Ahmedabad
	```
- 