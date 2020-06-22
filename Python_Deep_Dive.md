# Section 1 Basic Review
* Conditions
  ```python 
  b = true if a>1 else false 
  ```
* Function
  * else will execute if while is not exited from break statement 
    ```python
    while...else...
    ```
  * function is just an object. You can assign a function to a variable
    ```python
    my_func=func_4
    func_4()
    --> 'running func_4'
    my_func()
    --> 'running func_4'
    ```
 * lambda function
    ```python
    fn1 = lumnda x: x**2
    fn1(2)
    --> 4
    ```  
* Enumerate returns a tuple (index, element)
  ```python
  s = 'hello`
  for i, c in enumerate(s):
      print(i,c)
  --> 0 h
  --> 1 e
  --> 2 l
  --> 3 l
  --> 4 o
  ```
* \__str__: it is used when you call str()
  ```python
  class Rectangle(10,20):
	def __str__(self):
        return 'Rectangle: width={0}, height=  {1}'.format(self.width, self.height)
  r1 = Rectangle(10, 20)
  str(r1)
  --> 'Rectangle: width-10, height=20'
  ```
* \__eq__
use to define how to compare ==  
* isinstance(): doesn't work for subclass. Has to be exact the same type of class  
* 3 ways to set and get attribute value
```python
class Rectangle:
    def __init__(self, width, height):
        self._width = width
        self._height = height
    
    @property
    def width(self):
        return self._width
    
    @width.setter
    def width(self, width):
        self._width = width
```
* useful functions:
  * `isprintable()` : check whether a var is printable
  * `isalpha()` : check whether a string only contains char
  * `id()` : check the memory address of a var
  * `gc.collect()` :collect the gabbage
  * timer:  
  ```python
  start = time.perf_counter()
  end = time.perf_counter()
  time = end - start
  ```
