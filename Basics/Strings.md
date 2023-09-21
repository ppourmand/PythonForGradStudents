# Strings
I'm sure you've see these before in other languages but string literals in Python can be done in three ways: 
- Single quotes
- Double quotes
- Triple quotes

```Python
single_quotes = 'hello world'
double_quotes = "hello world"
triple_quotes = '''this
    is a
    multiline
    string
'''
```

> Note: the triple quotes are just three single quotes

Single quotes _will_ work but if your sentence has a single quote in it then that will cause issues so I've seen more people use double quotes than anything else.

### Escape Characters
These are special characters that can be put into strings in order to "escape" it. For instance:

```
\'
\"
\t # a tab character
\n # a newline character
\\
```

If you want to insert a single quote into a string but can't because your string is surrounded by single quotes, you can add a `\` in front of it which tells Python to use the _literal_ quote character and not confuse it for ending the string. See below

```
my_string = 'A single quote string. let\'s use a single quote within it'
```

If we didn't have `\` then Python would 1. give us an error 2. think that the string ends after `let` rather than `it`

### Indexing and Slicing
Strings, thankfully, work very similarly to lists! [Everything you can do to a list](Lists.md#indexes) you can do to a string.

```Python
>>> my_string = "hello world"
>>> my_string[0]
h
>>> my_string[4]
0
>>> my_string[-1]
d
>>> my_string[:5]
hello
>>> my_string[6:]
world
```

### Methods on Strings
[Here](https://docs.python.org/3/library/string.html) is the Python documentation for some common string operations. 

You will probably only really use stuff like `.lower()`, `.upper()`, and maybe `.join()`/`.split()`

Join and split are interesting since they do the opposite of each other: split splits a string based on some character you want and join well.. joins them with a character you want. Here is an example:

```Python
>>> a_sentence = "hello everyone this is a sentence"
>>> a_sentence.split(" ")
["hello", "everyone", "this", "is", "a", "sentence"]
>>> a_sentence.join("-")
"hello-everyone-this-is-a-sentence"
```

The `split(" ")` splits the string by a space character and returns a list of each split item. The `.join("-")` takes that list and joins all the items together, with the character `-` and returns a string 