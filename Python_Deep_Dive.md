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
* * *
# Section 3 Variables and Memory
* Immutable: The value of a var can never be changed. New result of a var is to change to pointer to a new space with new value  
* Mutable: can be changed
  * Lists, sets, dic, users-defined classes
  * List.append won’t change the address, but using '+' will change the address  
  e.g. ```new_list = [1,2,3] + [4]``` will change the address  
  ``` new_list.append(4)``` won't change the address  
  * mutable collection objects are not safe from side effect
  ![Screenshot]()
* Immutable:
  * An object whose internal state cannot be changed
  * numbers(int, float, boolean), strings, tuples, frozen set, user-defined classes
  * Mutable in immutable object is mutable  
  e.g. ```t=([1,2]) -> t=([1,2,3])``` and the address of t won’t be changed
* Memory Optimization  
  * Immutable var: Python manager will locate same memory for immutable var if they have the same value no matter how to initiate the var.  
  ```python
  a = 10,
  b = int(10)
  c = int('10')
  d = int('1010', 2)
  print(id(a), id(b), id(c), id(d))
  --> 194xd, 194xd, 194xd, 194xd
  c = [1,2]
  d = c
  // c and d will have the same memory address
  d.append(3)
  print(c)
  --> [1,2,3]
  // c and d will still have the same memory address
  ```
  * Mutable var, the python manager will locate different locations even though they have the same value (only within integer between [-5, 256]
[]

