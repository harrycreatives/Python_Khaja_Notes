### Python 3 intelligence about Numbers
* What our Python3 knows/understands about numbers

![preview](./Images/python19.png)

* Python 3 has the following knowledge
  * Expression Operators: +,-,*,/,%,>>,** etc..
  * Built in functions: pow, abs, round, int, hex, bin etc..

* We will explore this as we go along
* For python 3 are variables names not places
* When we use numbers we build expressions using variables and operators
```
x = 5
y = 6
z = x + y
```
![preview](./Images/python20.png)

* What will python do if the operators are mixed

![preview](./Images/python21.png)

* What if you want to do addition first and then multiplication, then use parantesis ()

![preview](./Images/python22.png)

* So lets try to speak with python to solve our simple intrest
  * Lets try in a shell

![preview](./Images/python23.png)

  * Create a file called as simpleintrest.py and in this file add some instructions with expressions.
```python
principal = 10000
rate_of_intrest = 10
time_in_years = 2
simple_intrest = principal * rate_of_intrest * time_in_years /100
print(simple_intrest)
```
* To execute this program. Open powershell/cmd/terminal.
```
python <path to your program>
```
![preview](./Images/python24.png)
![preview](./Images/python25.png)

### Mixed Types are converted up
* When python sees mixed types the result will be always the complex type.

![preview](./Images/python26.png)

* But what will you do if you want the result to be simple type, then you need to tell python do conversions using built-in functions like int(), float() etc

![preview](./Images/python27.png)