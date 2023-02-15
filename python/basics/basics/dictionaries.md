---
title: Dictionaries
priority: 10
---

## Learning outcomes

- How to create dictionaries
- How to add and remove dictionary items
- How to access dictionary elements
- How to loop through dictionary elements

## Dictionaries

Dictionaries in Python are a type of data structure that stores data in key-value pairs. They are also known as hashmaps or associative arrays in other programming languages. Dictionaries allow quick access to values (similar to lists), but unlike lists, quick access is through a key instead of an index. The keys are also used to get a value associated as a pair with the key instead of just the key value.

<br>

### Creating a dictionary

As we mentioned in the previous lesson, to instantiate a dictionary we use curly braces. We can also use the `dict()` function.

```py
phone_book = {}
phone_book = dict()
```

The key is a unique identifier for the value and the value can be any data type, including another dictionary. The keys can be thought of as a set, where the order does not matter and each key is unique. To create a dictionary with keys and values, we separate the keys and values using a colon `:` and separate each key-value pair with a comma `,`.

```py
phone_book = {
  'John': '555-555-5555',
  'Jane': '555-555-5556',
  'Bob': '555-555-5557',
}
print(phone_book)
```

<b>Output:</b>

```sh
{'John': '555-555-5555', 'Jane': '555-555-5556', 'Bob': '555-555-5557'}
```

<br>

### Accessing items

To access a value in a dictionary, use square brackets `[]` and place the key inside the brackets. If the key does not exist, a KeyError will be thrown.

```py
print(phone_book['John'])
print(phone_book['Bob'])
```

<b>Output:</b>

```sh
555-555-5555
555-555-5557
```

<br>

We can also use the `.get()` method to access a value. If the key does not exist, it will return `None` instead of throwing an error.

```py
print(phone_book.get('John'))
print(phone_book.get('Not a key'))
```

<b>Output:</b>

```sh
555-555-5555
None
```

<br>

### Adding, Updating, and Deleting items

To set a value, we can use the square bracket notation and assign a value to a key. If the key does not exist, it will be created. If the key exists, the value will be updated.

```py
print(phone_book)
phone_book['John'] = '555-555-5558'
phone_book['Sally'] = '555-555-5559'
print(phone_book)
```

<b>Output:</b>

```sh
{'John': '555-555-5555', 'Jane': '555-555-5556', 'Bob': '555-555-5557'}
{'John': '555-555-5558', 'Jane': '555-555-5556', 'Bob': '555-555-5557', 'Sally': '555-555-5559'}
```

Notice how the value for John was updated to `555-555-5558` and a new key-value pair was added for Sally.

<br>

We can also use the `.update()` method to add or update multiple key-value pairs at once depending on if the key exists or not.

```py
print(phone_book)
phone_book.update({'John': '555-555-5558', 'Sally': '555-555-5559', 'Joe': '555-555-5560'})
print(phone_book)
```

<b>Output:</b>

```sh
{'John': '555-555-5555', 'Jane': '555-555-5556', 'Bob': '555-555-5557'}
{'John': '555-555-5558', 'Jane': '555-555-5556', 'Bob': '555-555-5557', 'Sally': '555-555-5559', 'Joe': '555-555-5560'}
```

<br>

### Deleting Items

To delete a key-value pair, we can use the `del` keyword or the `.pop()` method. The `del` keyword will delete the key-value pair from the dictionary and the `.pop()` method will delete the key-value pair and return the value.

```py
print(phone_book)
del phone_book['John']
print(phone_book.pop('Jane'))
print(phone_book)
```

<b>Output:</b>

```sh
{'John': '555-555-5555', 'Jane': '555-555-5556', 'Bob': '555-555-5557'}
555-555-5556
{'Bob': '555-555-5557'}
```

<br>

### Looping through dictionaries

Before we can introduce you to how to loop through a dictionary you will need to understand the different sets of values we can loop through. There are a few different ways that we can access a set of values from a dictionary such as:

- The keys of the dictionary using the `.keys()` method or just the default behavior of looping through the dictionary.
- The values of the dictionary using the `.values()` method.
- The key-value pairs of the dictionary using the `.items()` method.

<br>

```py
phone_book = {
  'John': '555-555-5555',
  'Jane': '555-555-5556',
  'Bob': '555-555-5557',
}

print(phone_book.keys())
print(phone_book.values())
print(phone_book.items())
```

<b>Output:</b>

```sh
dict_keys(['John', 'Jane', 'Bob'])
dict_values(['555-555-5555', '555-555-5556', '555-555-5557'])
dict_items([('John', '555-555-5555'), ('Jane', '555-555-5556'), ('Bob', '555-555-5557')])
```

<br>

To loop through a dictionary, we can use the `for` loop and the `.keys()` method or just using the default dictionary.

```py
for key in phone_book.keys():
  print(key)
```

or

```py
for key in phone_book:
  print(key)
```

<b>Output:</b>

```sh
John
Jane
Bob
```

<br>

Similarly, to loop through the values of a dictionary, we can use the `for` loop and the `.values()` method.

```py
for value in phone_book.values():
  print(value)
```

<b>Output:</b>

```sh
555-555-5555
555-555-5556
555-555-5557
```

<br>

To loop through the key-value pairs of a dictionary, we can use the `for` loop and the `.items()` method.

```py
for key, value in phone_book.items():
  print(key, value)
```

<b>Output:</b>

```sh
John 555-555-5555
Jane 555-555-5556
Bob 555-555-5557
```

## Exercises

Here's a dictionary:

```python
  info = {
    'name': 'Fyodor Dostoevsky',
    'dob': '11/11/1821',
    'dead': True,
    'died': '28/01/1881',
    'popular_books': ['Notes from Underground', 'Crime and Punishment', 'The Idiot', 'Demons', 'The Brothers Karamazov'],
    'children': [
      {
        'name': 'Alexey Dostoevsky',
        'dob': 1875,
        'died': 1878,
      },
      {
        'name': 'Lyubov Dostoevskaya',
        'dob': 1869,
        'died': 1926,
      },
      {
        'name': 'Sonya Dostoevskaya',
        'dob': 1868,
        'died': 1868,
      },
      {
        'name': 'Fyodor Dostoevsky',
        'dob': 1871,
        'died': 1922,
      },
    ],
  }
```

<br>

1. Print out the `name` field using the square bracket notation.
2. Print the `died` field using the `.get()` method.
3. Remove the `dead` field.
4. Loop through the dictionary and print out 3 things separately: a list of the dictionary's keys, values, and items.

## Knowledge Check

- What does dictionary declaration look like in Python?
- What does dictionary `.get()` do? What are its parameters?
- What do `del` and `.pop()` do in the context of dictionaries? What are the differences?
- How to get dictionary keys, values, and pairs of keys and values?
- What is the syntax for a loop that goes through each item in a dictionary?

## Additional Resources

- [Corey Schafer's video on Python Dictionaries](https://www.youtube.com/watch?v=daefaLgNkw0&list=PL-osiE80TeTt2d9bfVyTiXJA-UTHn6WwU&index=5)
- [W3 Schools on Python Dictionaries](https://www.w3schools.com/python/python_dictionaries.asp)
- [Python Documentation on Python Dictionaries](https://docs.python.org/3/tutorial/datastructures.html#dictionaries)
