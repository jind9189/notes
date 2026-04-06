#### If Condition
```
if (condition1)
	{
		//what to do when condition1 passed
	}
else if (condition2)
	{
		//what to do when condition1 failed but condition2 passed
	}
else 
	{
		// what to do if not condition passed.
	}
	
	

```

alternative if syntx
```
 condition ? what_if_true : else
 
 condition ?? true
```

#### Switch case
```
	switch (variable)
	{
		case value1: 
			code block; 
			break;
		casse value2: 
			code block; 
			break;
		default: 
			code block;
			break;
	}
```

#### While Loop
will check condition and than only will execute the code block
```
	variable initialization
	while (condition)
	{
		//code block here;
		variable increament / decreament
	}
	
	
```

##### Do While
execute code block at-least once and than check the condition
```
	variable init
	do
	{
		//code blocke here
	} while (condition)
```

#### For Loop
provide the syntax to write code with initialization, condition and increment in single line
```
	for (init; condition; incrementation)
	{
		//code blocke here		
		if(conditionToBreak)
		{
			break;
		}
		lablename:
		if(conditionToContinue)
		{
			continue;
		}
		if (conditionToGoSomePlace)
		{
			goto labelname;
		}
	}
```

> Break statement will be used inside the loop, it terminate the program. to break a loop conditionally only it should be used within `if block`
> Continue statement will be used to skip the iteration of execution of loop for that condition, go and perform next iteration
> goto Labelname; can be used from line of code inside a method. goto cannot be used cross method.





