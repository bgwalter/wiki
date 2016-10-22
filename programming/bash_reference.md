Bash programming
================

Variables
---------

```sh
# Initialize a new variable and write it to the screen
example="Hello, world!"
echo $example
```


Conditional statements
----------------------

### Equality

An if statement takes the following form:

```sh
if [ <test of equality> ]; then
	# do something
fi

```

Alternatively, if you want to check if the statment is false, you can use the `!` operator:

```sh
if [ !<test of equality> ]; then
	# do something
fi

```

#### Equal

```sh
# test if two variables are the same
if [ a -eq b ]; then
	echo "$a == $b"
fi

# test if two variables are not the same
if [ a -nq b ]; then
	echo "$a != $b"
fi
```

#### Less than

```sh
# test if a variable is less than another
if [ a -lt b ]; then
	echo "$a < $b"
fi

# test if a variable is less than or equal to another
if [ a -le b ]; then
	echo "$a <= $b"
fi
```

#### Greater than

```sh
# test if a variable is greater than another
if [ a -gt b ]; then
	echo "$a > $b"
fi

# test if a variable is greater than or equal to another
if [ a -ge b ]; then
	echo "$a >= $b"
fi
```

Loops
-----

### For loop

```sh
# print the numbers 0 through 10
for i in 1 2 3 4 5; do
	echo $i
done
```

### While loop

```sh
while [ <condition> ]; do
	# do something
done
```

Running programs
----------------

Often times it's necessary to run an outside program. You do this by using the syntax, `$(<command>)`. For exmaple, say you want to use `ls` to print every file in a directory:

```sh
for i in $(ls); do
	echo $i
done
```


Functions
---------

```sh
# define function
function a {
	echo "hello"
}

# call function
a
```

### Parameters

```sh
# function definition
function a {
	echo $1
}

# call function
a "hello"
```


Command line arguments
----------------------

```sh
# print the first argument to the screen
echo $1

# print the number of arguments passed to the screen
echo $#

# print every argument to the screen
for i in $@; do
	echo $i
done
```

If you saved the above code as a program, `test.sh` and ran it as `sh test.sh hello world` it would print:

```
hello
2
hello world
```

Case
----
