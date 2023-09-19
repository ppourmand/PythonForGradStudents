# Loops
In Python, and coding in general, we like to be lazy. That is it say, if we can do less work with the same outcome, we will choose that 10 times out of 10.

The most basic idea behind achieving this is with loops. If we want to do an action multiple times, a loop is the best way to express that idea.

## For Loop
### Example
Lets say your data looks like the following:

```Python
my_data = ["car", "house", "plane"]
```

From our [lists](Lists.md) overview, we know that this is a list of 3 strings. Maybe we want to add the word "my" to every single item in this list like `my car` and `my house`. Logically we would want to go through each word and do it ourselves, right? Python makes this easier for us with what's called a `for loop`

Here's what a for loop that would achieve what we want looks like

```Python
my_data = ["car", "house", "plane"]
my_new_data = []

for item in my_data:
    my_new_data.append("my " + item)

print(my_new_data)
```

when we run this code, the output is

```Python
['my car', 'my house', 'my plane']
```

Yay! We've successfully edited every String in this List!


## While Loop
In Python, there are several types of loops. The first one we learned is called a `for loop`. Now we will learn about a `while loop`

While loops are good for checking to see if some sort of condition you want is valid

### Example
```Python
countdown = 5

while countdown > 0:
    print("Still counting down! value: ", countdown)
    countdown = countdown - 1
```

In this example, we have a variable called `countdown` that we've set to the value of `5`. On the line with the `while` we check a condition to see if the value of `countdown` is greater than 0. If it is, we jump into the "body" of the loop and start executing those lines in order

So since the `while` condition is true on the first run, we jump in and print out "Still counting down! value:" with the value of the countdown . Next we decrease the value of `countdown` by 1, so it's now equal to 4. We repeat this until the `while` condition is no longer met

Therefore, our output would be printing out "Still counting down!" 5 times! Here's the output:

```Python
Still counting down! value:  5
Still counting down! value:  4
Still counting down! value:  3
Still counting down! value:  2
Still counting down! value:  1
```