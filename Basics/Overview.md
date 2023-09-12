# Table Of Contents
- [Data types](/DataTypes.md)
- [Lists](/Lists.md)
- [Loops](/Loops.md)
- [Strings](/Strings.md)

## Variables and Data Types
In Python, every value has an associated type with it. For instance:

```python
a_string = "hello" # the value is a string (or str)
an_integer = 5 # the value is an integer (or int)
a_float = 1.7 # the value is a float
a_boolean = True # the value is a bool, meaning True or False
```

These values can be stored in what's called a `variable`. In the example above these are `a_string`, `an_integer`, `a_float`, and `a_boolean`. When you reference these words, that you get to name, the Python interpreter will give you back its' value.

```shell
>>> hello = 40
>>> hello
40
```

When I reference the variable `hello`, it will always return to me the value I assigned to it `40`.

## Naming Variables
In Python, there are certain rules and styles you should adhere to for naming your variable. In general we use what is called "snake case" which is just an underscore character between the words.

```python
sample_variable = 10
another_longer_variable = "foo"
```

In addition to this, there are *invalid* variable names as well: 

```python
sample-variable = 10
sample variable = 10
1sample_variable = 10
''sample_variable = 10 
sample_&variable = 10
1234 = 10
```

hyphens, spaces, starting with a number, being a number, special characters are not allowed so keep that in mind when coming up with variable names

## Comments
These will come in handy when you step away from your code from a while and come back to it wondering "what was I trying to do here"

```python
# a note to future self
foo = 10
bar = 10.5
```

A comment needs to start with the `#` character on each line you want the comment. You can use comments to temporarily "delete" lines too that you may want to bring back at some later point but don't want to deal with the hassle of copy/pasting it to another document and then bringing it back