# Remarks

## Make it work, make it right, make it fast
1. *Make it Work* stage: code to achieve the desired behavior or effect
2. *Make it Right* stage: refactoring
3. *Make it Fast* stage: profiling and optimizing

## `print` statement versus `print` function
Avoid using `print` as a statement. `print` should never have been implemented like a statement. 
```python
# Does only work in Python 2.x.x
print 'Hello, World!'
```

But use a function call instead:
```python
# Does work in both Python 2.x.x and Python 3.x.x
print('Hello, World!')
```

## Global statements
Avoid using global `print` function calls in a `Python` module:
```python

def foo(bar)
	return bar
	
print(foo(1))
```

But use instead:
```python

def foo(bar)
	return bar
	
# Will only be executed if this module is the `__main__` module, 
# not when this module is being imported.
if __name__ == "__main__":
	print(foo(1))
```

The same applies for variables: make variables global if they need to be global (e.g. constants) not because it is convenient for testing.

For testing you can encapsulate your tests in seperate functions and even your tests in separate test suite functions:
```python
if __name__ == "__main__":
	test1()
	test2()
```

## Integer division

```python
print('Python', python_version())
print('3 / 2 =', 3 / 2)
print('3 // 2 =', 3 // 2)
print('3 / 2.0 =', 3 / 2.0)
print('3 // 2.0 =', 3 // 2.0)
```
Possible output:
```python 
Python 2.7.6
3 / 2 = 1
3 // 2 = 1
3 / 2.0 = 1.5
3 // 2.0 = 1.0
```

Possible output:
```python 
Python 3.4.1
3 / 2 = 1.5
3 // 2 = 1
3 / 2.0 = 1.5
3 // 2.0 = 1.0
```

* Use `//` for integer division in both Python 2.x.x and Python 3.x.x to obtain integers.
* Convert one of the arguments explicitly to a `float` in both Python 2.x.x and Python 3.x.x to obtain floating point values.

## Packages
* Avoid to use the scalar arithmetic operations provided in `math` on `Python` lists, use the `numpy` module instead.
* Avoid to use the basic random number generator operations provided in `random`, use the `numpy.random` submodule instead.

```python
import numpy as np

def foo():
	a = np.zeros((3))
	b = np.ones((3))
	c = np.arange(3)
	d = np.array([0.0, 7.0, 9.0])
	e = np.random.random((3))
	return a, b, c, d, e

if __name__ == "__main__":
	for bar in foo():
		print(bar)
```

Use `matplotlib` for plotting:
```python
import matplotlib.pyplot as plt

def foo():
	xs = np.arange(3)
	ys = np.random.random((3))
	plt.plot(xs, ys)
	plt.show()

if __name__ == "__main__":
	foo()
```

## Imports
Import full module and use its full name:
```python
import numpy

if __name__ == "__main__":
	a = numpy.array([0.0, 7.0, 9.0])
	print(a)
```

Import full module and redefine its name for use:
```python
import numpy as np

if __name__ == "__main__":
	a = np.array([0.0, 7.0, 9.0])
	print(a)
```

Import specific functionality of a module, without the need of using the module name:
```python
from numpy import array

if __name__ == "__main__":
	a = array([0.0, 7.0, 9.0])
	print(a)
```

```python
from numpy import array as rowvector

if __name__ == "__main__":
	a = rowvector([0.0, 7.0, 9.0])
	print(a)
```

Import all functionality of a module, without the need of using the module name (bad practice):
```python
from numpy import *

if __name__ == "__main__":
	a = array([0.0, 7.0, 9.0])
	print(a)
```

## Command line
* By executing `python hello.py` in a command terminal, your default `Python` distribution will execute `hello.py`.
* By executing `python` in a command terminal, you can interactively start writing `Python` code.

The variable `_` contains the last answer. So:
```python
>> 1 + 1
2
>> _ + 1
3
>> _
3
```
