---
title: Dictionaries
priority: 10
---

# Dictionaries

## Learning outcomes

- How to create dictionaries
- How to add and remove dictionary items
- How to access dictionary elements
- How to loop through dictionary elements

## Dictionaries

also called hashmaps or associative arrays.

allow us to use in a key-value pair.

As we mentioned in the previous lesson, to instantiate a dictionary we use curly braces. We can also use the `dict()` function.

```py
info = {}
info = dict()
```

Dictionaries store values in a key-value pair format. The key is a unique identifier for the value. The value can be any data type, including another dictionary. The keys can be thought of as a set, where the order does not matter and each key is unique.

```py
phone_book = {
  'John': '555-555-5555',
  'Jane': '555-555-5556',
  'Bob': '555-555-5557',
}
print(phone_book)
```

<b>Output:</b>

```py
{'John': '555-555-5555', 'Jane': '555-555-5556', 'Bob': '555-555-5557'}
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

- [Dictionaries](https://www.youtube.com/watch?v=daefaLgNkw0&list=PL-osiE80TeTt2d9bfVyTiXJA-UTHn6WwU&index=5)
