## What is an OBJECT

Object is the istantiation of a class. The class can be anything. It can be, 

- User Defined Class
- System Class

System Classes are, 
> int, float, string, double, char, etc...

So writing anyline of below code is creating an object
```csharp
	1.  int i = new int();
	2.  string s = new string();
	3.  float f = new float();
	4.  double d = new double();
	5.  car c = new car();

	// these 5 lines represents 5 objects	
```

## Scope of an OBJECT
There can be 5 scopes for creating and using an object

- Local Scope
- Block Scope
- Instance Scope
- Class Scope / `static`
- Method return / `caller scope`

### Local Scope of OBJECT
> Calling an `object` inside a method

```csharp
	class program
	{
		public void object(){
			myObject o = new myObject();
			o.id = 31;
		}
	}
```

Here the lifetime of the `object o` depends on the lifetime of the method. If the mehod is destroyed then the object is also destroyed with the method. 

### Block Scope of OBJECT
> Calling an Object inside a block of code

```csharp
	if(value == 1){
		myObject o2 = new myObject();
		foreach(s.id == o2.id){
			Console.WriteLine($"{s.name}");
		}
	}
```

This `object o2` will be destroyed when the if block of code will be over. So this is the Block Scope of an object. 

### Instance Scope of  OBJECT

> if an object referance is called in a class and will be initiated in an other object then it is called Instance Scop of OBJECT

```csharp
	class person{
		int id;
		public address a;
	}

	class program
	{
		public static void main()
		{
			person p = new person();
			p.address = new address(32,"Dhanmondi","Dhaka");
		}
	}
```
Here the object `p.address` is alive untill the person `p` is alive. If person `p` is somehow deleted / destroyed then the object `p.address`  will also be vanished. 


### Class Scope of OBJECT
> If an object reffered as a `static object` in a `static class` then this object is called class scope of an OBJECT. 

```csharp
	public static class admin
	{
		static address a = new address(32,"Dhanmondi","Dhaka");
	}

	public class program
	{
		public static void main()
		{
			Console.WriteLine(admin.a.city);
		}
	}
```

Now with this approach untill the program ends and static class gets destroyed the object remains in it's place. 

### Method Return / Caller Scope
> If a method on a class is set to return a new object then it is called `caller scope` of an object

```csharp
	class person
	{
		int age;
		public address a;
		public Account account;
		Account assign_account(int id, string name)
		{
			account = new Account(id, name);
			return account;
		}
	}	

	class program
	{
		public static void main()
		{
			Person p = new person();
			Account a = p.assign_account(5,"Rayshad");
		}
	}
```
Here the assign account not only creates account object but also returns that object by value. This makes the object `caller scope`.
