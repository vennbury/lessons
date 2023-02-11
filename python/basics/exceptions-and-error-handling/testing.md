---
title: Testing
priority: 36
---

## Learning Outcomes

- What is unit testing
- How to unit test with the `unittest` and `pytest` modules
- How to use fixtures to set up and tear down tests
- How to assert statements in tests

<br>

## About this Lesson

Being able to test our programs is an important skill to have to ensure that your code is working as expected. We will first go over the built-in `unittest` module and then proceed with the similar but more powerful `pytest` module.

<br>

### Writing Tests with unittest

Tests in the `unittest` module are written as functions within a class that inherits from the `unittest.TestCase` class. We can use the `assertEqual`` method to check if two values are equal. If the condition is false, the test fails, and if it's true, the test passes.

```py
import unittest

class TestAddition(unittest.TestCase):
  def test_add_integers(self):
    self.assertEqual(1 + 1, 2)
  def test_add_strings(self):
    self.assertEqual('foo' + 'bar', 'foobar')
```

We can also use the following common assert methods:

- `assertNotEqual`, which is the opposite of `assertEqual`
- `assertTrue` and `assertFalse`
- `assertIsNone` and `assertIsNotNone`
- `assertIn` and `assertNotIn`
- `assertRaises`

<br>

#### Running Tests with unittest

To run our tests, we can use the following command:

```bash
python -m unittest test_addition.py
```

where `test_addition.py` is the name of the file containing our tests. If any of the tests fail, the output will show the line number and name of the failed test along with the error message.

<br>

### Test Fixtures

We can use test fixtures to set up and remove an environment for our tests. The `setUp` method is used to run instructions before each test, and the `tearDown` method is run after each test. Let's say we want to test with the contents of a file, we would want to have an isolated environment where we create the file with our contents before each test and remove it after each test.

```py
import unittest
import os

class Test_Files(unittest.TestCase):
    def setUp(self):
        self.file = open("data.txt", "w")
        self.file.write("Entry 1\nEntry 2")
        self.file.close()
    def tearDown(self):
        os.remove("data.txt")
    def test_file_contents(self):
        self.file = open("data.txt", "r")
        contents = self.file.read()
        self.assertEqual(contents, "Entry 1\nEntry 2")
        self.file.close()
```

<br>

## Testing with pytest

Pytest is a simpler yet more powerful testing framework as opposed to the built-in `unittest` module. To get started, we will need to install `pytest` with the following command:

```bash
pip install pytest
```

Writing tests is similar to the `unittest` module, but we can create functions in our code that start with `test_` and `pytest` will automatically run them. Instead of using `assert` functions, we use the `assert` keyword and write our expression after it.

```py
def test_addition():
    assert 2 + 2 == 4
```

And to run our tests, we can use the following command:

```bash
pytest test_addition.py
```

where `test_addition.py` is the name of the file containing our tests. We can still group our tests into a class, but we will need to also prefix the class name with `Test`.

```py
class Test_Addition:
    def test_add_integers(self):
        assert 1 + 1 == 2
    def test_add_strings(self):
        assert 'foo' + 'bar' == 'foobar'
```

Fixtures in `pytest` are similar to the `unittest` module, but we use the `@pytest.fixture` decorator instead of the `setUp` and `tearDown` methods. We use the `yield` keyword to yield our setup (in this case the path to our file path). If no tear down procedure is needed, use the `return` keyword for your setup instead of the `yield` keyword.

```py
import pytest

@pytest.fixture
def data_file(tmp_path):
    file_path = tmp_path / "data.txt"
    with open(file_path, "w") as f:
        f.write("Entry 1\nEntry 2")
    yield file_path
    file_path.unlink()

def test_file_contents(data_file):
    with open(data_file, "r") as f:
        contents = f.read()
    assert contents == "Entry 1\nEntry 2"
```

`pytest` has a lot more features such as support for mocking and plugins for testing web applications and databases. You can read more about it [here](https://docs.pytest.org/en/7.1.x/getting-started.html).

## Knowledge Check

- What is unit testing?
- How do the `unittest` and `pytest` modules differ?
- How do we assert statements in `unittest`? How about in `pytest`?
- What is a test fixture?
- Why are the `setUp` and `tearDown` methods useful?

<br>

## Additional Resources

- [The Importance of Test Driven Development](https://web.archive.org/web/20211123190134/http://godswillokwara.com/index.php/2016/09/09/the-importance-of-test-driven-development/)
- [Unit Testing in Python](https://machinelearningmastery.com/a-gentle-introduction-to-unit-testing-in-python/)
- [unittest Module Documentation](https://docs.python.org/3/library/unittest.html)
- [pytest Framework](https://docs.pytest.org/en/7.1.x/getting-started.html)
