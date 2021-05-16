### Understanding Programs better
* Today i will introduce one website to improve your understand of code [Refer Here](http://pythontutor.com/index.html)

### break and continue statements in loops
* __break__ will exit the loop
* __continue__ will skip the step in current loop and go to the next iteration
* To understand break and continue execute this program in pythontutor.com
```python
index = 2
is_even = False
while index <= 10000:
    if index%2 == 0:
        print(index)
        index = index+9
        continue
    elif index%3 == 0: 
        print(index)
    elif index%11 == 0:
        break
    index = index+1

print("i'm out of the loop")
```

### Now lets solve our Number guessing program
* Lets understand this program
```
we will tell python3 to remember a random number between some range (1,100)
then we will ask the user to enter his guess
if he has guessed the same number which python remembers he wins
if he guesses lower than random we will hint the user to guess high
else we will hint to guess low
we will do you accept defeat?, if user say yes we will stop & show the number
else user continues guessing
```
* Lets speak with Jarvis
```
Hi Jarvis
Remember a random number between 1 and 100 as lucky_number
continue till user accepts defeat or wins
   take input from user and remember it as guess
   if guess < lucky_number hint user to guess high or accept defeat
   if guess > lucky_number hint user to guess low or accept defeat
   if guess == lucky_number display congrats and stop execution.
```
* Hint for generating a lucky number
```
import random
lucky_number = random.randint(1,100)
```
* My Program looks as shown below
```python
import random
lucky_number = random.randint(1,100)
while True:
    user_guess = int(input('Enter your guess : '))
    if user_guess < lucky_number:
        print("Guess higher")
    elif user_guess > lucky_number:
        print("Guess lower")
    else:
        print("congrats you were great at guessing")
        break

    accept_defeat = int(input("Enter 0 to accept defeat any other number to continue: "))
    if accept_defeat == 0:
        print(lucky_number)
        break
```

### Bank interest rates
* This program should ask certain questions and show the fixed deposit interest rates to customer
```
Ask age of the customer
if age > 60 

    show interest rate will be 12%
Ask number of years that the customer is having account with this bank
    if numberofyears > 10
        show interest as 8 %
    3< numberofyears< 10
       show interest as 6%
show interest rate as 4.5%
```