
- Object is a small unit (entity) in the program that represents a real-world person or thing.
- objects are created based on class.
- objects are created on heap. heap is memory area for object for every run.
- heap memory is common for all methods for that application.
- All reference variables local variable of methods are stored in stack, for each method is called , new stack will be created.
- object stores actual data (fields) and can access methods of class
- reference variable stores address of any (only one) object


### Inheritance

- Allows the classes to be arranged in a hierarchy that represents "is a type of " relationships
- The parent class acts as base type of child classes.
- The child are called derived class.
- Child will have inherited functionality defined in parent via inheritance

#### Types of Inheritance
- Single Inheritance
- Multi-Level Inheritance
- Hierarchical Inheritance :  One base class &Many derived class
- Multiple Inheritance : Multiple base class (in c# this can be implemented by interface)
- Hybrid Inheritance : 

```
class ParentClassName()
{
	public methodname1 (param1)
	{
	}
}

class ChildClassName : ParentClassName()
{
	public ChildClassName(...): ParentClassName(arg1, arg2)
	{
	}
}

// the construtor of child will call construtor of parent class and continue to 

```

#### base keyword
- base keyword represents parents class's members in the child class.
- it is optional to use. but in case of name ambiguity (example: there is method in child or from other multi inherited base ) it is mandatory to use base keyword.
- if Parent class have parameterized constructor than it is mandatory to call it, but if there is parameter-less than it is optional.
-

#### Method Hiding;
if child class want to overwrite the definition of method inherited from base class, method hiding should be used with `new` keyword in defining method with same name and same parameters in derived or child class.

#### Method Overriding
- It extend the parents class method.
- When method is called both parent and child method will be used
- Syntax : in parent class `virtual` keyword is used while in base class `override` keyword is used.. additionally in child method, first line will call method from base class using `base` keyword
```
class ChildClass: ParentClass
{
	public override void extendMethod()
	{
		base.ExtendMethod();
	}
}
```

#### Sealed Class
-  sealed class can inherited from other classes and interface.
- sealed class block and further inheritance. means sealed class cannot be used as base or parentclass for inheriting.
- It cannot contain virtual method.

```
sealed class SealedClass() : base class
{

}
```

#### Sealed Method
This sealed keyword along with `override` will prevent child of this class to override the method which was virtual from based class.


#### Abstract Class

- Is base class which cannot be create object.  no object can be initiated from abstract class
- Abstract class can be used as base class.
- example : Animal is abstract class, which can be used to base class for animal like wild, pet. which on further can be inherited as lion, dog, etc.
- Abstract is intended for common set of fileds and methods to all child classes.
- Abstract can contain all types of members like fields, properties, methods, constructors, etc. Members of abstract class can be used via child class.

#### Abstract Method
- method in abstract can have abstract methods which need to be implemented in child classes. Child class will use keyword `override` to implement the abstract method of base abstract class.
- This abstract method is only structure with no implementation.

#### Interface 
- interface is set of abstract method, that must be implemented by the child classes.
- Child class should implement all methods of the interface. 
- like abstract we cannot create object of interface
- But we can create reference of interface , which can store the address of objects of any one of the corresponding child.
- interface cannot inherited from class, but classes can be inherited from class and interface
- 
```
interface Interface1
{
	ReturnDataType methodName(param1);
}

interface Interface2
{
	ReturnDataType methodName(param1);
}

class DerivedClass : Interface1, Interface2
{
	public ReturnDataType methodName(param1)
	{
	}
}
```
- Explicit Interface Implementation: When same name method is available in multiple base interface , then child class have option to implement only single method, or using explicit interface implementation using interface name with method 
```
	void  interface1.Method1(param1, param2)
	{
	}
	void interface2.Method2(param1,param2)
```



#### Namespaces
Namespace is collection of classes, interfaces, structures, delegates types, enumerations.

- Nested namespaces are allowed.
```
namespace Employee
{
	namespace Manager
	{
		public interface Iinterface1
		{
		}
	}
	
	namespace HR
	{
		public interface Interface2
		{
		}
	}
}
```
-  to access we need to specify full path `parentNamespace.ChildNameSpace.Interface.`
- 'Using' is directive to be used at top of class file. it will import all element of that space.
- situational we can use directive `using parentNamespace.Childnamespace` for convenience to write full path in every line while calling element of that namespace.
- `using mynamespace = parentNamespace.Childnamespace` allows to create alias name for the namespace 
- `using static Namespace.StaticClassName` is feature from #CS_6_0 which allow us to directly access any of its methods anywhere in the current file. 
```
using static System.Console;

//somewhere in main
WriteLine("we can directly use writeline without inline full path)
```

- Partial Class:
	- Class that span into multiple files. Compiler will compile it as single class only.
	- `public partial class product { }` can be created in various files
- Partial Methods
	- `partial void MethodNAme(param1) { }`
	- Partial methods are declared in one partial class, just like abstract method, and implement in another partial class, that have same name.
	- Partial methods are private in nature so should be called using 
- Static class
	- is class that can contain only "static members".
	- it is useful to prevent accidental creation of object for the class, by making it as "static class"