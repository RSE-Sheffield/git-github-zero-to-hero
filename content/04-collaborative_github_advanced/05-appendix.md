+++
title = "Appendix"
date =  2021-05-19T12:11:18+03:00
weight = 5
+++

## Correct Pull Requests

***

### subtract

There should be **changes to 3 files**, 2 of which should be new files in the correct location.

#### `pythoncalculator/subtract.py`

There should be a **new `pythoncalculator/subtract.py`** containing:

```python
def subtract(x, y):
    return x - y
```
####  `pythoncalculator/__init__.py`

The `pythoncalculator/__init__.py` file should contain the following line:

```python
from .subtract import subtract
```

#### `tests/test_subtract.py`

There should be a **new `tests/test_subtract.py`** containing:

```python
from pythoncalculator import subtract


def test_subtract():
    assert subtract(1, 3) == -2
```

***

### divide

There should be **changes to 3 files**, 2 of which should be new files in the correct location.

#### `pythoncalculator/divide.py`

There should be a **new `pythoncalculator/divide.py`** containing:

```python
def divide(x, y):
    return x / y
```
####  `pythoncalculator/__init__.py`

The `pythoncalculator/__init__.py` file should contain the following line:

```python
from .divide import divide
```

#### `tests/test_divide.py`

There should be a **new `tests/test_divide.py`** containing:

```python
from pythoncalculator import divide


def test_divide():
    assert divide(10, 2) == 5
```

***

### multiply

There should be **changes to 3 files**, 2 of which should be new files in the correct location.

#### `pythoncalculator/multiply.py`

There should be a **new `pythoncalculator/multiply.py`** containing:

```python
def multiply(x, y):
    return x * y
```
####  `pythoncalculator/__init__.py`

The `pythoncalculator/__init__.py` file should contain the following line:

```python
from .multiply import multiply
```

#### `tests/test_multiply.py`

There should be a **new `tests/test_multiply.py`** containing:

```python
from pythoncalculator import multiply


def test_multiply():
    assert multiply(10, 3) == 30
```