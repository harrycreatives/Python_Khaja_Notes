### Repetitive Statements
* When we are assigned home work from our teacher will she say something like write number from 1 to 100 or will she write all the numbers

![preview](./Images/python51.png)
![preview](./Images/python52.png)

* Lets look at our code
```
print(1)
print(2)
print(3)
print(4)
print(5)
print(6)
print(7)
print(8)
print(9)
print(10)
```
* Now if we want to get the same thing done from our python3, we need to understand looping structures. Lets look at __while__
* in the above code only number is changing, so if we make number dynamic rather than static will it help?
```
while <condition>:
    <block>
```
* Lets adopt this to our above program
```python
index = 1
while index <= 10:
    print(index)
    index = index + 1
```

### Write a program to print all the even numbers from 1 to 100
* Lets speak with Jarvis
```
Hi jarvis
start from 1 till 100 and remember this as index
check if index%2 == 0 and if it is yes print index
```
* Now our python program will be something like
```python
index = int(input("Enter the starting number :"))
end = int(input("Enter the ending number :"))
while index <= end:
    if index%2 == 0:
        print(index)
    index = index + 1
```

### Write a program to calculate factors of a number given by user
* Lets speak with Jarvis
```
Hi Jarvis,
Accept input from user and remember as number
start from 2 till number-1 and remember as index
   check if number is divisible by index , if yes print index
```

### Exercise: Write a python programs
* Write a program to find if the input is prime or not?
* [Project Euler Problem 1](https://projecteuler.net/problem=1)
* [Project Euler Problem 2](https://projecteuler.net/problem=2)
* [Project Euler Problem 3](https://projecteuler.net/problem=3)