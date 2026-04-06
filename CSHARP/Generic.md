
Understanding generic class, 


### Generic Class
Generic class is a class, which contains one or more "type parameters"
```
	class ClassName<T>
	{
		public T FieldName
	}
	
	// somewhere in main
	ClassName<int> referenceVariable = new ClassName <int> ();
```
-  Depending on type passed the class will be generic. In above case if int is passed to `Classname & FieldName` will be int.

#### Generic Constraints
Generic constraint is mechanism to provide constraint to what are possible type to be passed to the generic class
```
class ClassName <T1, T2> where T1: StudentClass where T2: EmployeeClass
{
	public T FieldName;
}
```
- when any other type is provided compiler will give compile error. it will make it typesafe.

#### Generic Methods
- Where you are not sure , what type of parameter need to be passed, you can use generic methods.
```
class sample{

	public void GenericPrintMethod<T>(T obj) where T: class
	{
		if(obj.GetType() == typeof(Student))
		{
			Student temp = obj as Student;
			System.Console.WriteLine(temp.Marks);
		}
		else if (obj.GetType() == typeof(Employee))
		{
			Empoyee temp = obj as Employee;
			System.Console.WriteLine(temp.Salary);
		}
		
	}
}	

//somewhere in main
	
	Sample sample = new Sample();
	Employee emp = new Employee()(Salary =1000);
	Student stu = new Student() {Marks = 80};
	
	sample.GenericPrintMethod<Employee>(emp);
	sample.GenericPrintMethod<Student(stu);
	

// Output
// 1000
// 80	

```
