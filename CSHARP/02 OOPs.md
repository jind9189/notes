


### CLASS
- Class represents the non-primitive type. it represent the structure of fields and methods.
- Class is model of objects, sometime called blueprint.
- class declares list of fields and list of methods

#### Class [accessModifier]


|     | Assess Modifier | Description                                                                   |
| --- | --------------- | ----------------------------------------------------------------------------- |
| 1   | Interal         | Class is accessible within the same assembly                                  |
| 2   | public          | class is accessible in the same assembly and other assemblies                 |
| 3   | static          | class contains only static members only                                       |
| 4   | abstract        | class can additionally contains abstract methods                              |
| 5   | sealed          | sealed class can't be inherited                                               |
| 6   | partial         | multiple partial classes that have same name, are combined into single class. |
|     |                 |                                                                               |
|     |                 |                                                                               |





```
[accessModifier] class car
{
	//Fileds : variable to store values about object
	// Methods : manipulate the variable
	// Constructors :  initialize the field
	// Properties : used to set  or get values in fields
	// Events : to raise notification to other classes
	// Destructors : clear unmanage resources.


	string fname;
	strng lname;
	int age;
	
	string print_fullname(string fname, string lname, )
}
```

### OBJECTS

- Object is a small unit (entity) in the program that represents a real-world person or thing.
- objects are created based on class.
- objects are created on heap. heap is memory area for object for every run.
- heap memory is common for all methods for that application.
- All reference variables local variable of methods are stored in stack, for each method is called , new stack will be created.
- object stores actual data (fields) and can access methods of class
- reference variable stores address of any (only one) object



### Fields
#### Fields [AccessModifier]

|     | Access Modifier    | in same class | in child of same assembly | in other class of same assembly | in child of other assembly | In Other class at other assembly |
| --- | ------------------ | ------------- | ------------------------- | ------------------------------- | -------------------------- | -------------------------------- |
| 1   | Private            | Yes           | No                        | No                              | No                         | No                               |
| 2   | Protected          | Yes           | Yes                       | No                              | Yes                        | No                               |
| 3   | private protected  | Yes           | Yes                       | No                              | No                         | No                               |
| 4   | internal           | Yes           | Yes                       | Yes                             | No                         | No                               |
| 5   | protected internal | Yes           | Yes                       | Yes                             | Yes                        | No                               |
| 6   | public             | Yes           | Yes                       | Yes                             | Yes                        | No                               |


#### Field [modifier]

|     |          |                                                                                                                              |
| --- | -------- | ---------------------------------------------------------------------------------------------------------------------------- |
| 1   | static   | files are common to all objects                                                                                              |
| 2   | const    | fields value can't be modified. by nature it is static in nature. compiler replaces all constant names with respective value |
| 3   | readonly | fields value can't be modified. Compile-time restriction only.                                                               |
|     |          |                                                                                                                              |
Field syntax
```
 // accessModifier modifier type FieldName;
 
 public string fname;
 public string lname;
 

```


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
