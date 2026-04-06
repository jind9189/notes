#CS_3_0 
#advanceCoding #needpractise 
Extension method is a method which inject (can add structure or interface), without modify  the source code of that class .
Useful when we do not have source code, but we want to extend the existing class.

```
// existing class


```

Syntax for extension method
```
class ClassName
{
	//
	// class body
}


static class ClassName
{
	public static ReturnType MethodName (this ClassName ParameterName, ...)
	{
		//
		// method body here
		//
	}
}
```

Example

```

// Project1: External or other project
public class Product
{
	public double productCost {get; set;}
	public double DiscountPercentage {get; set;}	
}

// project2 implementing extension to class of project

using project1; // this will be part of project1

namespace ExtensionMethodsExample
{
	public static class ProductExtensions
	{
		public static double GetDiscount (this Product product)
		{
			return product.Product * product.DiscountPercentage / 100; 
		}
	}
	
}

// somewhere in main program

using project1;
using extensionNamespace;

//main
	Product p = new Product() {Product =1000, DiscountPercentage = 10};
	Console.WriteLine(p.GetDiscount());

```