
## Basic
### Assembly: 
compiled code is either ``exe/dll`` and called assembly.

#### Garbage Collection
- garbage collection is process of deleting objects from memory, to free up memory.
- It may perform garbage collection when program need more memory. 
- Memory manager component of clr does this job.
- Heap is created for program when start and is 1 for entire life time of application.
- Garbage Collection process : GC checks belongs information from MSIL code, collects references of an object. it identifies whether any object is referenced by static field. the object that has at-least on living references variables in any stack or static field are alive objects. other are un-used or dead objects.
- GC automatically get triggered in the following conditions
	- when the "heap" is full or free space is too low
	- when we call `GC.Collect()` is called explicitly
- Generation: heap contains three segments (called generations)
	- Generation 2: long lived generation
	- Generation 1: Survival Generation
	- Generation 0: Short Lived generation
	- 


#### Managed and unmanaged Resources
- the objects that are created by CLR are called Managed resources. This will participate and will be managed by garbage collection.
- File Streams, database connection are example of unmanaged resources.
- Destructors : 
	- clears unmanaged resources just before deleting the object. Generally at the end of application execution.
	- `~Classname() `{  // code ;} 
	- Destructor doesn't de-allocate any memory , it just will be called by CLR automatically just before deleting the object of the class.
	- destructor will be compiled as finalize
- Dispose : 
	- clear unmanaged resources after the specific task (work ) is completed . so no need to wait till end of application execution.
	- IDisposable interface of system namespace. has method Dispose. Which is used to close unmanaged resources that are created during the life-time of the object.
	```
	Class ClassName : System.IDisposable
	{
		public void Dispose()
		{
			// close un-managed resources here.
		}
	}
	
	// somewhere in main program
	using(Sample s = new Sample())
	{
		s.method()
	}
	```
- #CS_8_0 using Classname referenceVariable = new ClassName(); // dispose will be called at end of method the line is used.
#### Destructors
-  the ob



### OOPs Concepts
- Encapsulation is a concept that binds together the data and operations that manipulate the data, and that keeps both data safe from outside to be misused. It is concept of grouping data and manipulations (means field and methods)
- Abstraction: is the concept of providing only limited data or operations to the code exist outside of class.
- Polymorphism :  provides the ability to the developer, to define different implements for the same method in the same class or different classes.
	- Compile-Time Polymorphism: `Method overloading` or `static polymorphism` or `Early binding`
	- Run-Time Polymorphism : `Method Overriding` or `Dynamic polymorphism` or `late binding`

- Local variable and parameter variable local to method- 
- This
	- 'this' keyword refers to current object, which method has be invoked.
	- this is not available with static methods.
- Method Overloading:
	- Writing multiple methods with same name in the same class, with different parameters
```
Example
	SomeMethod(Param1);
	SomeMethod(Param1, Param2)
	// all method must have same but different parameters types, 
```


### Condition Control
	As a programming language csharp provide syntax to provide condition control of program to flow.
refer : [[Condition Control]]

Topics

- 
- [[Class]]
- [[Objects]]
- [[Fields]]
- [[Methods]]
-