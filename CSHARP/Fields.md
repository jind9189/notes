

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

