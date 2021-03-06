### Objects in Python
* We will understand the following
  1. How to create classes and instantiate objects in Python
  2. How to add attributes and operations/methods/behaviors to Python objects

### Creating Python classes
Lets create a new file called as _helloclass.py_ with the following:
```python
class HelloClass:
    pass
```
* This is our first object-oriented program.
* To name your classes Lets try to understand naming conventions from PEP-8. [Refer Here](https://www.python.org/dev/peps/pep-0008/#class-names) Class names should be named using __CapWords__
* __pass__ keyword indicates that no further action needs to be taken
* Now lets create objects
```python
object_1 = HelloClass()
object_2 = HelloClass()
print(object_1)
print(object_2)
```
![preview](./Images/python62.png)

* This code is creating objects (instantiates) two objects from __HelloClass__ named object_1 & object_2
* When printed these two objects tell us what memory address they live in

### Adding Attributes
* Lets create one more file called point.py and add a __Point__ class
```python
class Point:
    pass

p1 = Point()
p2 = Point()

p1.x = 6
p2.x = 5
p1.y = 7
p2.y = 6
print(p1.x, p1.y)
print(p2.x, p2.y)
```
* Lets execute this program 
```
python point.py
```
![preview](./Images/python63.png)
* All we need to do to assign a value to an attribute on an object is ```<object>.<attribute> = <value>```

### Add Operations or behavior
* Now lets create a new implementation of our __Point__ class.
```python
class Point:
    def reset(self):
        self.x = 0
        self.y = 0

p1 = Point()
p2 = Point()

p1.x = 6
p2.x = 5
p1.y = 7
p2.y = 6

print(p1.x, p1.y)
print(p2.x, p2.y)
p1.reset()
p2.reset()
print(p1.x, p1.y)
print(p2.x, p2.y)
```
* Now lets execute this code

![preview](./Images/python64.png)

* Operations or behaviors of class will be defined using def keyword
```
def <operation_name>(<parameters>):
    <code>
```
* Now to understand about self lets look at this code
```python
class Point:
    def reset(self):
        print("resetting")
        self.x = 0
        self.y = 0

    def square(this):
        print("performing square")
        this.x = this.x**2
        this.y = this.y**2

    def print(current):
        print(current.x, current.y)

p1 = Point()
p2 = Point()

p1.x = 6
p2.x = 5
p1.y = 7
p2.y = 6
```
* All operations of the class will have the first parameter with any name, but this argument is conventionally named as __self__. I???ve never seen a python programmer use any other name
* Lets follow the convention and change the code to __self__ in operations.
```python
class Point:
    def reset(self):
        print("resetting")
        self.x = 0
        self.y = 0

    def square(self):
        print("performing square")
        self.x = self.x**2
        self.y = self.y**2

    def print(self):
        print(self.x, self.y)

p1 = Point()
p2 = Point()

p1.x = 6
p2.x = 5
p1.y = 7
p2.y = 6

p1.print()
p2.print()
p1.square()
p2.square()
p1.print()
p2.print()
p1.reset()
p2.reset()
p1.print()
p2.print()
```
* When we call operations we use ```<object>.<operation_name>()```, then python internally passes the object to the self argument or self argument will have current objects reference
* We can call the operations in a different way ```<class>.<operation_name>(<object>)```
```python
p3 = Point()
p3.x = 2
p3.y = 2
Point.print(p3)
```
* What will happen if we don???t use self
```python
class Point:
    def reset():
       pass

p1 = Point()
p1.reset()
```
![preview](./Images/python65.png)

* The error message is simply trying to tell you forgot __self__ argument, whenever you call an operation from object, object itself will be passed as an argument to your method.
* Lets add more arguments to operations.
```
class Point:
    def reset(self):
        print("resetting")
        self.x = 0
        self.y = 0

    def square(self):
        print("performing square")
        self.x = self.x**2
        self.y = self.y**2

    def print(self):
        print(self.x, self.y)

    def move(self, x, y):
        self.x = x
        self.y = y
    
    def add(self, x, y):
        self.x = self.x + x
        self.y = self.y + y

p = Point()
p.x = 4
p.y = 5
p.print()
p.move(2,3)
p.print()
p.add(1,1)
p.print()
```
![preview](./Images/python66.png)
* How to import classes in python interactive shell (REPL)
```
python -i point.py
```
![preview](./Images/python67.png)