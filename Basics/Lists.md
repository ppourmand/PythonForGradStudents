# Lists
This will probably be the data structure that you interact with the most. Lists are just as they sound, a list of things!

```Python
my_first_list = [1, 2, 3]
list_of_colors = ["blue", "red", "yellow"]
```

## Getting values from lists
There are many ways to access values from a list. The most basic one that you may have seen before is with indexes:

```Python
my_list = ["blue", "red", "yellow"]
my_list[0]
```

### Indexes
This will give us the value `"blue"`. In Python, the beginning of the list is considered to be index 0 and increases for every position after (1, 2, 3, etc). Additionally, indexes can _only_ be integer values, they can't be something like `1.5`. 

You would think the values have to be positive only but that is not the case. A negative index simply means starting from the end of the list. For instance `-1` would refer to the last item in a list and `-2` the second-to-last item.

### Slices
If you want to access parts of the list and not just one item from the list, we use something similaar to indexes called slices. When we use a slice, the value we get is another list with the items that we specified so for example:

```Python
first_list = ["hotdog", "burger", "pizza", "pasta"]
second_list = first_list[1:3]
```

With this, the value of `second_list` is `["burger", "pizza"]`. The first number is which index to start at, and include. The second number is which index to end at, and not include

As a shortcut you can leave out either the first or second number and Python will just assume you mean until the end or beginning: 

```Python
second_list = first_list[1:] # start at the first index, go until the end
second_list = first_list[:3] # start at the beginning, go until the third index
```

### Deleting, changing, adding, containing
There are tons of methods that you can call on lists to do differnt things, and they are all listed (lol!) [here](https://docs.python.org/3/tutorial/datastructures.html)

Some of the basics that you will probably use the most are:

```Python
my_list = ["hotdog", "burger", "pizza", "pasta"]

my_list.append("smoothie") # adds this item to end of the list
my_list.pop() # remove the last item from the list and return it
my_list.sort() # sorts the list
my_list[1] = "cake" # changes the item at index one to 'cake'. Burger would now be cake
"hotdog" in my_list # this checks to see if the item hotdog is contained within our list, if it is this statement is True, otherwise it is False
```