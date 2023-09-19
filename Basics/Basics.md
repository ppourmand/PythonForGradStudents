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

## Flow Control
The concept of flow control is what makes programming so powerful. Yes we could try to code things in one big series of instructions but that will get unwieldy quickly. With flow control we can do actions based on conditions, think of a flow chart:

```mermaid
graph TD;
    Start-->a[Am I hungry?];
    a[Am I hungry?]-->Yes;
    a[Am I hungry?]-->No;
    No-->b[Go outside];
    Yes-->c[Go get some food]
```

The condition here would be the question `Am I hungry?`. We can represent the above chart in Python code as well:

```Python
if am_i_hungry:
    eat()
else:
    go_outside()
```

The first line checks a variable called `am_i_hungry`, which can evaluate to `True` or `False`. If the value is `True` it goes inside the `if` and calls the function `eat()`. If the `am_i_hungry` variable is `False`, however, the control flow falls to the `else` and drops into it, resulting in the `go_outside()` function to be called instead