Special method of class, which contains initializing logic of fields.
- Static constructor : can initialize static fields . execute only one time when first object is created. Access modifier will be private by default/
- Instance constructors by default will be private by default, but any other access modifier can be used as per requirement.
```
class Student
{
	string fname;
	string lname;
	string age;
	
	//constructors
	public Student (string firstnameParam, string lastnameParam, string agePara)
	{
		this.fname = firstnameParam;
		this.lname = lastnameParam;
		this.ageParam = age;
	}
}


//somewhere in main()
Student student1 = new Student("mukesh", "Bedval", 30);
Student student2 = new Student("Manish", "Bedval", 28);


```

- Parameter-less constructors do not take any parameter so it will initialize by fix values.
- Implicit Constructor : Compiler will create implicit constructor when there is not constructor parameter-lessor parameterized .
- Constructor Overloading : 
- when there are multiple constructors with same name in the class, with different set of parameter (similar to method overloading)
- Object Initialize :
	- special syntax to initialize fields / properties of class , along with creating the object.
	- It will be executes after the constructor. 
	- Its purpose is to initialize fields, after creating object, so it cannot have any initialization logic.
	```
		Student studen1 = new Student(){firstname ="Seema" , lastname="Sharma"};
	```
- 

