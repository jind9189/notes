
Receive a number/ string , search for the particular item among a group of items, set or get value into the group of items.

```

public class Car
{
	private string[ ] _brand = new[] {"BMW", "SKODA", "HONDA"};
	
	
	//public indexers
	public string this[int inde]
	{
		set 
		{
			this._brands[index] = index 
		}
		
		get
		{
			return _brands[index];
		}
	}
}

//somewhere in main
Car c = new Car();
c[0] = "Maruti";
System.Console.WriteLine(c[0]);



```


### Index Overloading
