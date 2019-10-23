# Exercise Workbench
* Design a While loop that lets the user enter a number. The number should be multiplied by 10, and the result stored in a variable named product. The loop should iterate as long as product contains a value less than 100.

   declare integer number
   do 
      Display "Enter a number: "
      input number
      set product = number * 10
      Output product
   while product < 100



* Design a Do-While loop that asks the user to enter two numbers. The numbers should be added and the sum displayed. The loop should ask the user whether he or she wishes to perform the operation again. If so, the loop should repeat; otherwise it should terminate.

declare string doAnother
declare integer num1,num2,sum
do
   Display "Enter first number: "
   input num1
   Display "Enter second number: "
   input num2
   set sum = num1 + num2
   Display "The Sum is ", sum
   Display "Again? Enter (y for yes): "
   input doAnother
while doAnother == y


* Design a For loop that displays the following set of numbers:

0, 10, 20, 30, 40, 50, . . . , 1000

declare integer number
constant integer MAX_VALUE = 1000
for number <= MAX_VALUE
   output number
   number += 10
end for

* Design a loop that asks the user to enter a number. The loop should iterate 10 times and keep a running total of the numbers entered.

declare integer number

* Design a For loop that calculates the total of the following series of numbers:
![image](https://user-images.githubusercontent.com/47218880/67423054-31740800-f599-11e9-9565-031c1f729e1c.png)

1/30 + 2/29 + 3/28 + ... + 30/1 

* Design a nested loop that displays 10 rows of # characters. There should be 15 # characters in each row.

* Convert the While loop in the following code to a Do-While loop:
```
Declare Integer x = 1
While x > 0
   Display "Enter a number."
   Input x
End While
```
* Convert the Do-While loop in the following code to a While loop:
```
Declare String sure
Do
  Display "Are you sure you want to quit?"
  Input sure
While sure != "Y" AND sure != "y"
```
* Convert the following While loop to a For loop:
```
Declare Integer count = 0
While count < 50
   Display "The count is ", count
   Set count = count + 1
End While
```
* Convert the following For loop to a While loop:
```
Declare Integer count
For count = 1 To 50
   Display count
End For
```
