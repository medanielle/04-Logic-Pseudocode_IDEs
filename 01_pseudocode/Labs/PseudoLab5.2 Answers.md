
# Bug Collector

A bug collector collects bugs every day for seven days. Design a program that keeps a running total of the number of bugs collected during the seven days. The loop should ask for the number of bugs collected for each day, and when the loop is finished, the program should display the total number of bugs collected.

         // Declare a variable to hold each number entered by the user.
   Declare Integer dailyBugs

         // Declare an accumulator variable, initialized with 0.
   Declare Integer weeklyBugs = 0

         // Declare a counter variable for the loop.
   Declare Integer counter

         // Explain what we are doing.
   Display "This program calculates the total of 7 days worth of bug collecting."

         // Get five numbers and accumulate them.
   For counter = 1 To 7
      Display "Enter a number of Bugs collected."
      Input dailyBugs
      Set weeklyBugs = weeklyBugs + dailyBugs
   End For
         // Display the total of the numbers.
   Display "The total bugs collect this week is ", weeklyBugs

# Calories Burned

Running on a particular treadmill you burn 3.9 calories per minute. Design a program that uses a loop to display the number of calories burned after 10, 15, 20, 25, and 30 minutes.


module main()            
            // Declare a variable to maintain count and minutes.
   Declare Integer minutes

            // Declare an accumulator variable, initialized with 0.
   Declare Integer calories

    for minutes = 10 to 30 step 5
        set calories = minutes * 3.9
        Output minutes, calories
    end for
End module


# Budget Analysis

Design a program that asks the user to enter the amount that he or she has budgeted for a month. A loop should then prompt the user to enter each of his or her expenses for the month, and keep a running total. When the loop finishes, the program should display the amount that the user is over or under budget.
main()
            //Declare your sentinel
    declare string doAgain

            //Declare variables for 
    declare real monthlyBudget
    declare real eachExpense
    declare real total

            //Get budget from user
    Display "What's your Budget? "
    input monthlyBudget

            //get all expenses from customer
    do 
        Display "Enter an expense: "
        input eachExpense
        total -= eachExpense
        Display "Do you have more expenses? (Enter 'y' for yes)
        input doAgain
    while doAgain == 'y'

            //give final output, both positive and negative
    if total >= 0 then
        Display "You are $", total, " underbudget."
    Else 
        Display "You are $", total, " overbudget."
return

# Sum of Numbers

Design a program with a loop that asks the user to enter a series of positive numbers. The user should enter a negative number to signal the end of the series. After all the positive numbers have been entered, the program should display their sum.

module main()
            //Declare variables for numbers entered and total sum
    decalre real num = 0
    declare real sum = 0

            //loop to get numbers and add them up
    while num >= 0
        Display "please enter a positive numer to add to sum: "
        input num
        set sum += num
    end while

    Display "Your total sum was ", sum

end module


# Tuition Increase

At one college, the tuition for a full-time student is $6,000 per semester. It has been announced that the tuition will increase by 2 percent each year for the next five years. Design a program with a loop that displays the projected semester tuition amount for the next five years.

module main()

            //Declare variables
    declare integer year = 1
    declare real inflation = 0.02
    declare integer tuition = 12000

    for year = 1 to 5 step 1
        set tuition = (tuition * inflation) + tuition
        inflation += 0.02
        Display "Year ", year, " tuition will be ", tuition
    end for

end module
        


# Average Rainfall

Design a program that uses nested loops to collect data and calculate the average rainfall over a period of years. The program should first ask for the number of years. The outer loop will iterate once for each year. The inner loop will iterate twelve times, once for each month. Each iteration of the inner loop will ask the user for the inches of rainfall for that month. After all iterations, the program should display the number of months, the total inches of rainfall, and the average rainfall per month for the entire period.

module main()

            //Declaration
    declare integer years 
    declare integer months
    declare real monthlyRain
    declare real totalRain
    declare real avgRainPerMon

    Display "Please enter years: "
    input years

    for 1 to years step 1
        for 1 to 12 step 1
            Display "please enter monthly rain: "
            input monthlyRain
            set totalRain += monthlyRain
            months += 1
    
    set avgRainPerMon = totalRain / months
    Output months, totalRain, avgRainPerMon

end Module

# Celsius to Fahrenheit Table

Design a program that displays a table of the Celsius temperatures 0 through 20 and their Fahrenheit equivalents. The formula for converting a temperature from Celsius to Fahrenheit is

![image](https://user-images.githubusercontent.com/47218880/67429019-e7911f00-f5a4-11e9-849e-c07e34b8044c.png)

F =9/5 * C + 32

where F is the Fahrenheit temperature and C is the Celsius temperature. Your program must use a loop to display the table.

module main()

                //Declaration
    declare real celsius, fahrenheit

                //build table
    Display "Celsius /t Fahrenheit"
    for celcius = 0 to 20 step 1
        set fahrenheit = (9 / 5 * celcius) + 32
        Display celsius /t fahrenheit /n

end module


# Pennies for Pay

Design a program that calculates the amount of money a person would earn over a period of time if his or her salary is one penny the first day, two pennies the second day, and continues to double each day. The program should ask the user for the number of days. Display a table showing what the salary was for each day, and then show the total pay at the end of the period. The output should be displayed in a dollar amount, not the number of pennies.

module main()
            //Declaration
    decalre integer days
    declare real salary
    declare real total

            //Get number of days
    Display "How many days? "
    input days

            //build table
    Display "Day /t Salary"
    for 1 to days step 1
        salary += 0.01'
        total += salary
        Display days /t salary /n
    
    Display "total salary is " total

# Largest and Smallest

Design a program with a loop that lets the user enter a series of numbers. The user should enter 
−
99
 to signal the end of the series. After all the numbers have been entered, the program should display the largest and smallest numbers entered.


module main()
    declare integer number = 0, largest, smallest 

    while numer != 99
        Display "Enter a number: "
        input number
        if number > largest
            set largest = number
        if number < smallest
            set smallest = number
    end while
    
    Display largest, smallest


# First and Last

Design a program that asks the user for a series of names (in no particular order). After the final person’s name has been entered, the program should display the name that is first alphabetically and the name that is last alphabetically. For example, if the user enters the names Kristin, Joel, Adam, Beth, Zeb, and Chris, the program would display Adam and Zeb.


module main()
    declare string word = 'test'
    decalre string last, first 

    while word != 'done'
        Display "Enter a Name: "
        input word
        if word > last
            set last = word
        if word < first
            set first = word
    end while
    
    Display first, last

    TEACHER:
/ Variables
Declare String name, lowest, highest
Declare Integer count
// Get the first name.
Display "Enter the first name."
Input name
First and last
// Since this is the only name entered so far,
// it is both the lowest and highest (alphabetically).
// Assign the name to lowest and highest.
Set lowest = name
Set highest = name
// Get the rest of the names and keep the lowest and highest.
For count = 2 To MAX_NAMES
   // Get the next name.
   Display "Enter the next name."
   Input name
   // Determine whether this is the lowest
   // or greatest name.
   If name < lowest Then
       Set lowest = name

# Calculating the Factorial of a Number

In mathematics, the notation n! represents the factorial of the nonnegative integer n. The factorial of n is the product of all the nonnegative integers from 1 up through n. For example:
![image](https://user-images.githubusercontent.com/47218880/67429154-2cb55100-f5a5-11e9-959b-79c4f1a34757.png)

7! = 1x2x3x4x5x6x7x = 5040

and

![image](https://user-images.githubusercontent.com/47218880/67429177-3c349a00-f5a5-11e9-94c6-82826c1b03cf.png)

4! = 1x2x3x4x = 24

Design a program that asks the user to enter a nonnegative integer and then displays the factorial of that number.

// Variables
Declare Integer number, count, factorial
// Set factorial to 1.
Set factorial = 1
// Get the number.
Display "Enter a number and I will calculate its factorial."
Input number
// Get the rest of the names and keep the lowest and highest.
For count = 1 To number
   factorial = factorial * count
End For
// Display the factorial.
Display "The factorial is ", factorial

# Multiplication Table

Design a program that uses nested loops to display a multiplication table for the numbers 1 through 12. The program’s output should look like this:
```
1 * 0 = 0

1 * 1 = 1

1 * 2 = 2

1 * 3 = 3
```
and so forth..
```
12 * 9 = 108

12 * 10 = 120

12 * 11 = 132

12 * 12 = 144
```
