
- All Variable are either Value Types and Reference Type
- Value types are not `nullable` while Reference types are default `nullable` types
- `ClassObject.NullableProperty.HasValue` can be used to condition check if it has value or it is null


#### Null Coalescing Operator
- `Null Coalescing operator` check whether the value is null or not
```
// syntax with ternary operator 

p2.property.hasValue ? p2.Property.value : 0  ;


// syntax with   null Coalescing operator
// variableName ?? valueIfNull 

p2.property ?? 0  ;

```

#### Null Propagation Operator
- The are syntax to perform `null propagation operator` . it checks the value of left hand operator whether it is null or not.
- it return value when value is not null. but returns null if value is null
- it access the property or method only if the reference variable is "not null"
- To avoid null exception.
```
Person p1 = new Person() {Age =20};


// normal code
Console.WriteLine( p1 == null : Convert.ToString(p1.Age);

// null propogatgion operator print value only if it is not null.
Console.WriteLin( p1?.Age );

```