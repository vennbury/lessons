---
title: Lists, Tuples, and Sets
priority: 9
---

# Lists, Tuples, and Sets

## Learning outcomes

- Create lists and access their elements
- Common list operations
- Create tuples and access their elements
- Understand the commonality between lists and strings
- Learn about sets, their purpose, and methods of working with them

<br>

## About this Lesson

In this lesson, we will learn about the list, tuple, and set data types that allow us to store multiple items in a single variable. These data types are built into Python, and there is one more data type called a dictionary that we will learn in the next lesson.

<br>

## Lists

### Initializing Lists

Lists store a collection of items that can be changed, of different data types, have duplicated, and are ordered.

```py
fruits = ["apple", "bannana", "peach"]
classes = ["Math", "History", "Math"]
numbers = [1, 2, "Three"]
print(fruits)
print(classes)
print(numbers)
```

<b>Output:</b>

```bash
['apple', 'bannana', 'peach']
['Math', 'History', 'Math']
[1, 2, 'Three']
```

As seen above, we can create a list using brackets `[]` and place our items inside that are separated by a comma. We can also create an empty list with empty brackets or use the `list()` method.

```py
empty_list_1 = []
empty_list_2 = list()
print(empty_list_1)
print(empty_list_2)
```

<b>Output:</b>

```bash
[]
[]
```

<br>

### Indexing and Slicing Lists

Just like we could with strings, we can index and slice strings to get their values.

```py
nums = [1, 2, 3, 4, 5]
print(nums[0])
print(nums[-1])
```

<b>Output:</b>

```bash
1
5
```

```py
nums = [1, 2, 3, 4, 5]
print(nums[:3])
print(nums[2:5])
```

<b>Output:</b>

```bash
[1, 2, 3]
[3, 4, 5]
```

slicing:
courses[0:2]

We can find the index of an item in our list by using the `list.index(item)`. If the item doesn't exist in the list, we will receive a ValueError.

```py
nums = [1, 2, 3, 4, 5]
print(nums.index(3))
```

<b>Output:</b>

```bash
2
```

<br>

### List Methods

Similar to strings, we can also use `len()` method to find the length of a string.

```py
nums = [1, 2, 3, 4, 5]
print(len(nums))
```

<b>Output:</b>

```bash
5
```

We can add values to our list by using the `list.append(item)` method.

```py
nums = [1, 2, 3, 4, 5]
nums.append(6)
print(nums)
nums.append(10)
print(nums)
```

<b>Output:</b>

```bash
[1, 2, 3, 4, 5, 6]
[1, 2, 3, 4, 5, 6, 10]
```

We can also use the `list.insert(index, value)` method where we can place an item in a specific position of a list.

```py
nums = [1, 2, 3, 4, 5]
nums.insert(3, "Hello")
print(nums)
nums.insert(0, "World")
print(nums)
```

<b>Output:</b>

```bash
[1, 2, 3, 'Hello', 4, 5]
['World', 1, 2, 3, 'Hello', 4, 5]
```

We can also remove items by using the `list.remove(item)` method. To remove the last element on the list, you can call `list.pop()`, which returns the last item and also modifies the list.

```py
nums = [1, 2, 3, 4, 5]
nums.remove(1)
print(nums)
print(nums.pop())
print(nums)
```

<b>Output:</b>

```bash
[2, 3, 4, 5]
5
[2, 3, 4]
```

We can merge two lists by using the `list.extend(list)` method.

```py
nums = [1, 2, 3, 4, 5]
nums_2 = [6, 7 ,8 , 9, 10]
nums.extend(nums_2)
print(nums)
print(nums_2)
```

<b>Output:</b>

```bash
[1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
[6, 7, 8, 9, 10]
```

To check if an item is contained in the list, we can use the `item in list` conditional.

```py
nums = [1, 2, 3, 4, 5]
print(1 in nums)
animals = ['bear', 'ram', 'cat']
print('cat' in animals)
print('rat' in animals)
```

<b>Output:</b>

```bash
True
True
False
```

<br>

#### Sorting and Reversing

To reverse a list, the `list.reverse()` method can be called on it.

```py
nums = [1, 2, 3, 4, 5]
nums.reverse()
print(nums)
```

<b>Output:</b>

```bash
[5, 4, 3, 2, 1]
```

We can sort a list by using the `list.sort()` method. It will numerically sort numbers and sort strings by alphabetical order.

```py
nums = [3, 5, 1, 2, 4]
nums.sort()
print(nums)
animals = ['bear', 'ram', 'cat']
animals.sort()
print(animals)
```

<b>Output:</b>

```bash
[1, 2, 3, 4, 5]
['bear', 'cat', 'ram']
```

We can also specify our `sort` method to sort in reverse order with `list.sort(reverse=True)`.

```py
nums = [3, 5, 1, 2, 4]
nums.sort(reverse=True)
print(nums)
animals = ['bear', 'ram', 'cat']
animals.sort(reverse=True)
print(animals)
```

<b>Output:</b>

```bash
[5, 4, 3, 2, 1]
['ram', 'cat', 'bear']
```

We can also use the `sorted(list)` function, which will copy our list so that we don't modify our original list.

```py
nums = [3, 5, 1, 2, 4]
sorted_nums = sorted(nums)
print(nums)
print(sorted_nums)
```

<b>Output:</b>

```bash
[3, 5, 1, 2, 4]
[1, 2, 3, 4, 5]
```

We can also use the `min(list)` and `max(list)` to find the minimum and maximum of our list.

```py
nums = [1, 2, 3, 4, 5]
print(min(nums))
print(max(nums))
animals = ['bear', 'ram', 'cat']
print(min(animals))
print(max(animals))
```

<b>Output:</b>

```bash
1
5
bear
ram
```

If we have a list of floats or integers, we can use the `sum(list)` method to find the summation of all items in the list.

```py
nums = [1, 2, 3, 4, 5]
nums_and_floats = [1, 2.5, 6.01, -19.025]
print(sum(nums))
print(sum(nums_and_floats))
```

<b>Output:</b>

```bash
15
-9.514999999999999
```

<br>

#### Lists and Strings

We can convert lists to strings and strings to lists using the `separator.join(list)` and `str.split(connector)`, where the separator is a string that will be placed between each item in the list and the connector is the string that will be removed from the string. For an integer or floating-point items in an array, we will need to pass each value as an integer using list comprehensions, which will be taught in the advanced python course.

```py
nums = [1, 2, 3, 4, 5]
print("".join(str(item) for item in nums))
animals = ["cat", "bear", "ram"]
print("".join(animals))
print("MOO".join(animals))
```

<b>Output:</b>

```bash
12345
catbearram
catMOObearMOOram
```

```py
nums_str = "1, 2, 3, 4, 5"
animals_str_1 = "catbearram"
animals_str_2 = "catMOObearMOOram"
print(nums_str.split(" ")) # converts to list items
print(animals_str_1.split(" "))
print(animals_str_2.split(" "))

```

<b>Output:</b>

```bash
['1,', '2,', '3,', '4,', '5']
['catbearram']
['catMOObearMOOram']
```

<br>

## Tuples

As we have seen, we can add and remove elements from a list, sort the list, and extend it with another list. All of these operations change the original list meaning that the list data type is "mutable". The tuple data type is similar to the list, but it is "immutable" as we cannot modify it once it is made. We can create an empty tuple with parenthesis `()` or the `tuple()` method.

```py
empty_tuple_1 = ()
empty_tuple_2 = tuple()
print(empty_tuple_1)
print(empty_tuple_2)
```

<b>Output:</b>

```bash
()
()
```

Tuples are used when you have a collection of items that will not change and you would like to have fast access (covered in the Data Structures and Algorithms Course) to knowing if elements are in your tuple with the `item in tuple` conditional.

```py
animals = ['cat', 'racoon', 'chipmunk']
print('racoon' in animals)
print('ram' in animals)
```

<b>Output:</b>

```bash
True
False
```

<br>

## Sets

Sets are also similar to lists except that they do not care about order and contain no duplicates. They have fast access to items the way tuples do. To initialize a set, we use the `set()` method. If we use empty curly braces `{}`, we will initialize a dictionary (we will learn about in the next lesson).

```py
empty_set = set()
print(empty_set)
```

<b>Output:</b>

```bash
set()
```

Since sets do not contain an order, the ordering when we print the elements of a set will change each time. As previously mentioned, sets have fast access to elements inside them with the `item in set` syntax.

```py
nums = {1, 2, 3, 3}
print(nums) # will vary
print("2" in nums)
print(2 in nums)

```

<b>Output:</b>

```bash
{1, 2, 3}
False
True
```

We can add items to a set using the `set.add(item)` method as opposed to the lists `list.append(item)` method. Otherwise, we can remove and pop elements just like we could with lists.

```py
nums = {1, 2, 3, 3}
nums.add(5)
nums.add(3)
print(nums)
print(nums.pop())
print(nums)
nums.remove(2)
print(nums)
```

<b>Output:</b>

```bash
{1, 2, 3, 5}
1
{2, 3, 5}
{3, 5}
```

Sets provide capability for operations that are used in set theory. We can use the `set.intersection(set)` method to find values in boths sets.

```py
nums_1 = {1, 2, 3, 4}
nums_2 = {3, 4, 5, 6}
print(nums_1.intersection(nums_2))
```

<b>Output:</b>

```bash
{3, 4}
```

We can use the `set.difference(set)` to find elements that are only present in the first set.

```py
nums_1 = {1, 2, 3, 4}
nums_2 = {3, 4, 5, 6}
print(nums_1.difference(nums_2))

```

<b>Output:</b>

```bash
{1, 2}
```

We can use the `set.union(set)` to find all elements that are present in either of the sets.

```py
nums_1 = {1, 2, 3, 4}
nums_2 = {3, 4, 5, 6}
print(nums_1.union(nums_2))
```

<b>Output:</b>

```bash
{1, 2, 3, 4, 5, 6}
```

<br>

## Exercises

### Lists

1. Create a list of 5 fruits.
2. Create another list of 3 elements that is a sublist of the first variable. Use negative indexing.
3. Add the second variable to the end of the first variable and store it as another variable.
4. Now do the same operation but add the second variable after the first element of the first variable.
5. Loop through the list and print each item on a new line.
6. Sort the list alphabetically.

<br>

### Tuples

1. Create a tuple with three values: an integer, a string, and a Boolean.
2. Deconstruct that tuple into three variables.

<br>

### Sets

1. Create a set from the list made in the Lists part of this exercise.
2. Create a set that contains 3 of the same fruits as the set in (1), and 2 different ones (or just 2 random strings).
3. Perform and print the results of three operations: intersection, difference, and union.

<br>

## Knowledge Check

- How to create lists? (Don't forget about string methods)
- What is negative indexing?
- How to add elements to a list?
- How to remove elements from a list?
- What are some of the ways to sort a list?
- How to create empty tuples?
- What's the difference between a list, a tuple, and a set?

<br>

## Additional Resources

- [Comprehensive overview](https://phoenixnap.com/kb/python-data-types#:~:text=Set%20Data%20Type%20%20%20Data%20Type%20%20complex%20%28%3Cvalue%3E%29%20%205%20more%20rows%20) of standard data types.
- Corey Schafer's video on [Lists, tuples, and sets](https://www.youtube.com/watch?v=W8KRzm-HUcc&list=PL-osiE80TeTt2d9bfVyTiXJA-UTHn6WwU).
- Corey Schafer's video on [Slicing strings and lists](https://www.youtube.com/watch?v=ajrtAuDg3yw&list=PL-osiE80TeTt2d9bfVyTiXJA-UTHn6WwU).
