### Project euler problem 2
* [Refer Here](https://projecteuler.net/problem=2) for problem.
* Lets speak with jarvis
```
Hi Jarvis
remember 2 as result
remember 1 as value_1
remember 2 as value_2
remember sum as 0
continue till value_1 + value_2 <= 4000000
  sum = value_1 + value_2
  check if sum is even if yes add to result
  value_1 = value_2
  value_2 = sum
```
* The Python program is
```python
value_1 = 1
value_2 = 2
result = 2
sum = 0
while value_1 + value_2 <= 4000000:
    sum = value_1 + value_2
    if sum%2 == 0:
        result = result + sum
    value_1 = value_2
    value_2 = sum
print(result)
```


### Project euler problem 3
* [Refer Here](https://projecteuler.net/problem=3) for problem.
* Lets speak with jarvis
```
Hi jarvis
remember 13195  as number
calculate number//2 and remember as factor
continue till factor > 1
    check if number is divisible by factor (number%factor == 0)
    if yes
       find if it is prime or not
       remeber is_primefactor with value true
       start from 2 till factor//2 and check if the number is divisble by any number. 
       if yes is_primefactor will be false
    if is_primefactor is true
      print number & exit program
```
* Python program is
```python
number = 13195
factor = number//2
while factor > 1:
    if number%factor == 0:
        # This means it is a factor
        # now check if this factor is prime
        is_prime_factor = True
        index = 2
        while index <= factor//2:
            if factor%index == 0:
                is_prime_factor = False
                break
            index = index + 1
        if is_prime_factor == True:
            print(factor)
            exit(0)
    factor = factor -1
```