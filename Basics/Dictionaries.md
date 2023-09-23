# Dictionaries
In my opinion, dictionaries are the most versatile data structure in Python (and in many languages). The concept is straightforward, it is literally a dictionary which is a bunch of keys and and their associated values. Think about a regular word dictionary where the keys are the words themselves and the values are the meanings. Same deal

Here's an example of a dictionary

```Python
house = {"bedrooms": "3", "bathrooms": "1"}
```

Do you notice the curly braces and each key ("bedrooms", "bathrooms") having a value (3, 1)? This is how we declare a dictionary with some values.

> NOTE: a dictionary is _unordered_ so you cannot assume the order of the keys within a dictionary like you can with a list

## Interacting with a dictionary
### Accessing
In order to access a specific key in a dictionary, you can use syntax that is quite similar to lists. For instance you could do

```
>>> house["bedrooms"]
"3"
```

Additionally if you wanted to check to see if a key exists in a dictionary you could do 

```
>>> "bedrooms" in house
True
```

### Methods
There are a bunch of methods you can call on dictionaries but we will focus on 3 here"::

```Python
>>> house.keys()
dict_keys(['bedrooms', 'bathrooms'])
>>> house.values()
dict_values(['3', '1'])
>>> house.items()
dict_items([('bedrooms', '3'), ('bathrooms', '1')])
```

Their naming makes it pretty straightforward to tell what they're doing. `keys()` will give you a list of the keys, `values()` will do it for values, and `items()` will give you this fancy thing that is 2 items in one, the key and the value.

### Looping
Dictionaries are similar to loop through when comparing to lists however there are some differences. See the example beloww

```Python
>>> house = {"bedrooms": "3", "bathrooms": "1"}
>>> for key, value in house.items():
>>>     print("Key: " + key + " Value: " + value)
Key: bedrooms Value: 3
Key: bathrooms Value: 1
```

If you notice, right after the `for` we have _two_ items instead of one. This is because `house.items()` gives us a 2-items-in-one value that we can unpack and put in each of these two variables. If you wanted a for loop that just iterated over the keys, you can do that as well:

```Python
>>> house = {"bedrooms": "3", "bathrooms": "1"}
>>> for key in house.keys():
>>>     print("Key: " + key)
Key: bedrooms
Key: bathrooms
```