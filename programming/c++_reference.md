## Operators

### ? : (Ternary operator)

The ternary operator takes the form of `<condition> ? <true> : <false>`

```C++
int a, b;

// code happens

return (a == b) ? "a and b are equal" : "a and b are not equal";
```

The above code is the same as

```C++
if (a == b) 
	return "a and b are equal";
else 
	return "a and b are not equal"t;
```


## String manipulation

### Comparing strings

There are two ways to compare strings. The first is `std::string::compare()`, which returns:

```
std::string::compare()
	 0 : strings are equal
	>0 : self is shorter than comparison 
	<0 : self is longer than comparison
```
<!-- /> -->

When used, it looks like the following:

```C++
std::string a, b;

// code happens

if (a.compare(b) == 0)
	return "Strings are equal";
```

Many people on [stackoverflow](http://stackoverflow.com/questions/9158894/differences-between-c-string-and-compare) say that this method is ugly and difficult to follow. Thus, they recomend the following:

```C++
if (a == b) {
	return "Strings are equal";
}
```

There isn't much difference between these two methods, in fact, `operator==` calls `std::string::compare()` anyways.

### Concatenate string

```C++
std::string name;

// code happens

std::string greeting = "Hello, " + name + "!";
```

### Convert to string

```C++
int n = 42;
std::string fourtytwo = std::to_string(n);
```