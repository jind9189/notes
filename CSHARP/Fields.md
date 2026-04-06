

### Variables

- Variable is a named memory location in RAM, to store a particular type of value, during the program execution
- The variable can hold value of type primitive or non-primitive
- The variable value can be changed any no of times.- 
- The variable data type should be specified while declaring the variable. It can’t change later.
- The variable must be declared before its usage.
- The variable must be initiated before reading its value.
- Variable will be stored in stack, For every method call, a new stack will be created.
- The stack (along with its variable) will be deleted automatically, at the end of method execution
- The variable in object of class is called fields.- 
- Variable when passed to methods is refereed as argument and parameter.
    
Syntax : 

```
DataType VariableName:
DataType Variable = Defaultname;
Variable = newValue
```

#### Type Conversion
Depending on requirement or need variable value might be required to convert from one type to another. this an be done by type conversion or type casting.

#numericConversion
- Implicit Casting:
	- The lower-numerical type can be automatically (implicitly) converted into 'higher-numerical type'
- Explicit Casting
	- manual convert value from one type to another data type. specially where higher type variable is to be converted into lower 
	```
		int a =100;
		float b ;
		b =float(a); // this is example of explicit casting
	```
#stringConversion
- Parse
	- The string value can be converted into any numerical data type by using parsing .
	- strong string to numeric value
	- parse will fail with error exception if string contains any character other than numeric.
	```
		string age = "40";
		int intAge = int.parse(age);
	```
#stringConversion with error handling
- TryParse
	- Same as parse,  but check input string value before real conversion,  if input value is invalid, it don't convert and returns false without raising any error exception.
#system_methods based conversion
- Conversion Methods
	- Predefined methods to convert any primitive type , string, to any other primitive or string .
	- `System.Convert` is class, which contains a set of predefined method.
	- for each data type we have conversion method.



### Fields of object


- Fields are variables that are declared in the class, but stored in objects
- modifier of fields can be [ static , const, read-only]
- When method is called the variable passed as argument will be passed as reference variable.
- When no value is passed than default value will be passed.
- Named argument : supply value to the parameter , based on parameter name
```
	public void Somemethod(double Param1=45, double param2=20)
	{
	}
	
	Somethod(40,50);
	Somemethod(,);  /default value
	somemethod(param1:24, param2:45) // calling method using name
	
```



refer #fieldAccessModifier  in [[Access Modifier]]

#### Field Modifier

| #   | field-modifier | Description                                                                                                                  |
| --- | -------------- | ---------------------------------------------------------------------------------------------------------------------------- |
| 1   | static         | files are common to all objects                                                                                              |
| 2   | const          | fields value can't be modified. by nature it is static in nature. compiler replaces all constant names with respective value |
| 3   | readonly       | fields value can't be modified. Compile-time restriction only.                                                               |
|     |                |                                                                                                                              |
Field syntax
```
public student
{
	public string fname;
	public string lname;
	public int age;
}

static void Main()
{
	student1 = new student();
	student2 = new student();	
} 
```


### Parameters to methods
- Parameter Modifiers
	- default
	- ref
	- out
	- in
	- params
```
Accessmodifier modifier ReturnDataType Methodname(ref DataType parameter1)
{
	
}	
// Calling method should also use 'ref' keyword . now you can change original variable whose value was passed to called method.
	
	
Accessmodifier modifier ReturnDataType Methodname2(out DataType Parameter1, in DataType Parameter2, param DataType Parameter3)
{
	Parameter1 = Somevalue1;
	
}
	
Var returnValue = Methodname2(out Argument1, out Argument, param DataType[] Parameter3)
// in this example methoname2 returns 3 value 1 via retrun , 2 with out parameters.
//Parameter2 value become read-only and cannot be modified inside the method.
// Parameter3 will take parameters from position 3rd as array of arguments.
```

#### Ref returns :  #needpractise
```
AccessModifier modifier ReturnDataType MethodName()
{
	return ref variable;
}


ref variable = Method()
```
- The references of return variable will be assigned to receiving variable. (C# 7.3)
- Any changes be made available calling variable



#### Enumerations
- Enumeration is collection of constants.
- it is used to specify the list of options allowed to be stored in a field / variable.
- It is used to control the input of other value than the list of values specified in enumeration.
```
	enum enumAgeGroup : int
	{
		Child, Teenager, Adult, Senior
	}
```
- By default , int is datatype of enum is int, you are allowed with some specific type to be changed. 

### Type of Values
- Value Types:  Stores simple values.  instances are stored in stack. 
	- Structure : instance is called structure instance
	- Enumeration: instance is called enumeration instances
- Reference Types; : instances are stored in heap. heap in only one for entire application. Mainly meant for storing complex large amount of values.
	- String, 
	- Classes 
	- Interfaces
	- Delegates

#### Class Vs Structure

| Structure                                                                            | Classes                                                                               |
| ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------- |
| it is value types                                                                    | It is reference type                                                                  |
| Instances are stored in stack. structure doesn't required heap                       | instance object are stored in Heap. but class reference variable are stored in stack. |
| Suitable to store small data                                                         | Suitable to store large data                                                          |
| Memory allocation and de-allocation if faster                                        | Memory allocation / deallocation is a bit-slower                                      |
| structure doesn't support parameter-less constructor                                 | Class support parameter-less constructor                                              |
| structures doesn't support inheritences                                              | class support inheritance                                                             |
| the "new" keyword just initializes all field of the structure instances.             | the new keyword creates a new object                                                  |
| does not support abstract and virtual methods                                        | class have abstract and virtual methods                                               |
| there is no destructors                                                              | class support destructors                                                             |
| derived from System.ValueType (note: System.ValueType is derived from System.object) | derived from System.Object                                                            |
| Does not support to initialzie "non-static fields" in declaration                    | Classes support to initialize "non-static fields" in declaration.                     |
| structures doesn't support protected and protected internal" access modifier         | Classes support "Protected" and 'Protected internal' access modifier                  |
| structure instance does not support to assign "null"                                 | Class references variable support to assign null.                                     |

#### Constructor in Structures
- By default for every structure c# provide parameter-less constructor. 
- We can create user-define parameterized constructor in structure. every fields should be initialized in parameterized constructor.
- The 'new' keyword do not create object but just initialize the memory in heap. in reality it is calling constructor of structure.
```
public strruct Category
{
	private int _catID;
	private int _catName;
	
	public Category (int catID, string catName)
	{
		_catID = catID;
		_catName = catName
	}
}

//somewhere in main
Category category = new Category(1,"Electronics")
```

#### Read-only structure #CS_8_0
- Useful in case requirement is structure which need to be used to retrieve the variable . All property ave only get accessors. 
- There will be a parameterized constructor that initializes all the fields.
-  it have faster performance .

> Except strings all primitive types are structures. 



#### System.Object 
-  it is based of all datatype
- there area virtual method in system.object like Equals, GetHashCode, ToString which can be overridden in case of requirement
```

public class person
{
	public string PersonName {get; set;}
	public string Email{get; set;}
	
	public override bool ToString()
	{
		return "Person name is "
	}
		
}


// somewhere in main
System.object obj = new Person() {PersonName = "Scott", Email="scott@gmail.com"};
```

#### Boxing to Unboxing
- Boxing : 
	- Value-type to reference type (example : int to System.Object )- it is automatically. no explicit syntax required. 
	- When variable is created with primitive data type , it has value in stack when boxing happen object is created in HEAP and address of object is assigned in stack.  (so now value is moved from stack to heap)
```
	int x = 10;
	object obj = x;
	
	System.Console.WriteLine(obj); // 10
		
```
- Unboxing
	-  Converting from reference type to value-type object
	- it will happen only for compatible data type
	- syntax has to be used `(Data-Type)SourceValue`
	-  So value is copied from heap to stack
```
	Object obj = 10;
	int x = int(obj);
	System.Console.WriteLine(obj); // output is 10
	System.Console.WriteLine(x); // output is 10
```
