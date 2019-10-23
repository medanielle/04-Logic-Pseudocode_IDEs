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

         // Declare a variable to hold each number entered by the user.
   Declare Integer number

         // Declare an accumulator variable, initialized with 0.
   Declare Integer total = 0

         // Declare a counter variable for the loop.
   Declare Integer counter

         // Explain what we are doing.
   Display "This program calculates the total of ten numbers."

         // Get five numbers and accumulate them.
   For counter = 1 To 10
      Display "Enter a number."
      Input number
      Set total = total + number
   End For
         // Display the total of the numbers.
   Display "The total is ", total

* Design a For loop that calculates the total of the following series of numbers:
![image](https://user-images.githubusercontent.com/47218880/67423054-31740800-f599-11e9-9565-031c1f729e1c.png)

1/30 + 2/29 + 3/28 + ... + 30/1 


         // Declare a variable to hold each number in fractions 
   Declare Integer numerator
   Declare integer denominator = 30

           // Declare an accumulator variable, initialized with 0.
   Declare float total = 0

            // Get factional numbers and accumulate them.
   for numerator = 1 to 30
      total += (numerator/denominator)
      numerator += 1
      denominator -= 1
   end for
            //Display the total
   Display "Total is ", total
   


* Design a nested loop that displays 10 rows of # characters. There should be 15 # characters in each row.

for 1 to 10
   for 1 to 15
      Display "#"
   end for
   Display newline
end for

* Convert the While loop in the following code to a Do-While loop:
```
Declare Integer x = 1
While x > 0
   Display "Enter a number."
   Input x
End While
```
Declare Integer x
Do
   Display "Enter a number."
   Input x
while x > 0


* Convert the Do-While loop in the following code to a While loop:
```
Declare String sure
Do
  Display "Are you sure you want to quit?"
  Input sure
While sure != "Y" AND sure != "y"
```
Declare String sure = "n"
while sure != "y"
  Display "Are you sure you want to quit?"
  Input sure
end while


* Convert the following While loop to a For loop:
```
Declare Integer count = 0
While count < 50
   Display "The count is ", count
   Set count = count + 1
End While
```

Declare Integer count
for count = 0 to 50
   Display "The count is ", count
   set count = count + 1
End for

* Convert the following For loop to a While loop:
```
Declare Integer count 
For count = 1 To 50
   Display count
End For
```

Declare Integer count = 0
while count < 50
   Display count
   count += 1
end while