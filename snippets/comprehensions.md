---
title: List comprehensions
tags: list
expertise: beginner
cover: blog_images/keyboard-tea.jpg
firstSeen: 2022-07-29T16:55:39+05:30
---

Comprehensions are special code statements that allow you to create new collections (specifically objects that represent groups of items like lists, sets, and dictionaries) based on pre-existing collections of the same type. They work similar to for-loops, using the `for` and `in` keywords to iterate over each element in the collection.

- The general format for set, list, and dictionary comprehesions, respectively, is:
```py
    {<expression> for <variable> in <collection>}
    [<expression> for <variable> in <collection>]
    {<key_expression>:<value_expression for <variable> in <collection>}
```

- Convert every temperature in `temperatures` from Fahrenheit to Celsius using a comprehension.

```py
def compFahrenheitToCelsius(temperatures):
  return [((temp-32)*5)/9 for temp in temperatures]
```

```py
compCelsiusToFahrenheit([32, 77]) # [0, 25]
```

- For comparison, this for-loop would return the same values. Notice that the for loop requires more code to do the same task.

```py
def loopFahrenheitToCelsius(temperatures):
  newList = []
  for temp in temperatures:
    newList.append(((temp-32)*5)/9)
  return newList
```
In general, it is better to use comprehensions for simpler tasks that do not require modifying lists, and for-loops for more complex tasks to preserve your code's readability.
