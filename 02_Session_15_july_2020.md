### Our character to speak with
* This is our character: Jarvis

![preview](./Images/jarvis.jpg)

* Snake/Jarvis has following capabilities

![preview](./Images/python04.png)

### Let’s get started with our first assignment
* I would like to instruct Jarvis to help me calculate simple intrest
* Lets speak with Jarvis
```
Hi Jarvis, How are you doing.

Remember 1000 as principal (principal = 1000)
Rememeber 12 as rateofintrest (rateofintrest = 12)
Remember 5 as timeperiod (timeperiod=5)
Now calculate principal*rateofintrest*timeperiod/100 and remember as simpleintrest 
Now show me simpleintrest
```
### Lets do one more problem solving with Jarvis
* Our Jarvis now has few additional capabilities
![preview](./Images/python04.png)
* I would like jarvis to help us in solving Project euler problem 1 [over here](https://projecteuler.net/problem=1)

```
Hi jarvis, How are you doing
Remember start as 1 (start=1)
Rememeber end as 10 (end = 10)
Remember result as 0
Now start caclulation from start till you reach end
   check start%3 == 0
    if yes add start to result
    
  check start%5 == 0
    if yes add start to result
    
  start = start+1
show me result 
```
* Lets convert the conversation into Java
```java
public class Test {
   public static void main() {

	int start=1;
        int end = 10;
	int result =0;
	while (start<end) {
           if(start%3==0 || start%5 == 0) {
		result = result+start;
	   }
           start = start+1;
		
        }
	System.out.println(result)
   }
}
```
* Lets convert this conversation into C#
```c#
public class Test {
   public static void main() {

	int start=1;
        int end = 10;
	int result =0;
	while (start<end) {
           if(start%3==0 || start%5 == 0) {
		result = result+start;
	   }
           start = start+1;
		
        }
	Console.WriteLine(result)
   }
}
```
* Lets convert this conversation into python
```python
start = 1
end = 10
result = 0
while start<end:
  if start%3 == 0 or start%5 == 0:
     result = result+start
  start = start+1

print(result)
```
### Lets do one more problem solving with Jarvis
* Lets take help of jarvis to solve this problem [Refer Here](https://projecteuler.net/problem=2)
* But first lets take help of jarvis to print fibonacci series till 100
```
Hi Jarvis
remember 1 as number1 and print it
remember 2 as number2 and print it
rememer 0 as result 
Now start calculation till result <= 100
    result = number1 + number2 (Add number1 and number2 and store in result)
    print result
    number1 = number2 (Assign value of number2 to number1)
    number2 = result (Assign value of result to number2)
```