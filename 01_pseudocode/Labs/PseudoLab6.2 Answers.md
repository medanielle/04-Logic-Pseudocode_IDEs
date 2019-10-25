# Array Programming Projects Choose 4 of the prompts.

## Total Sales

Design a program that asks the user to enter a store’s sales for each day of the week. The amounts should be stored in an array. Use a loop to calculate the total sales for the week and display the result.

module main ()
                //decalration
    declare real total
    constant integer SIZE = 7
    declare real sales[SIZE]
    declare integer index = 0

    for index = 0 to SIZE - 1
        Display "Enter Day ", index + 1, " sales: "
        input sales[index]
        total += sales[index]
    end for 

    Display "Total sales for the week are $", total

end module

## Lottery Number Generator

Design a program that generates a 7-digit lottery number. The program should have an Integer array with 7 elements. Write a loop that steps through the array, randomly generating a number in the range of 0 through 9 for each element. Then write another loop that displays the contents of the array.

module main ()
                //declaration
    constant integer SIZE = 7
    declare real lottery[SIZE]
    declare integer index = 0

    for index = 0 to SIZE - 1
        set lottery[index] = random (0, 9)
    end for 

    Display "Here is the random lottery number:"

    for index = 0 to SIZE - 1
        Display lottery[index]
    end for 
    
end module

## Rainfall Statistics

Design a program that lets the user enter the total rainfall for each of 12 months into an array. The program should calculate and display the total rainfall for the year, the average monthly rainfall, and the months with the highest and lowest amounts.

module main ()
                //declaration
    declare real total, avgRain, 
    declare real highest = 0
    declare real lowest = 100000000
    constant integer SIZE = 12
    declare real rainfall[SIZE]
    declare integer index = 0

                //for loop to gather rain data
    for index = 0 to SIZE - 1
        Display "Enter Month ", index + 1, " rainfall: "
        input rainfall[index]
                //set total and accumulate
        set total += rainfall[index]
                //set highest and check each input
        if rainfall[index] > highest then
            highest = rainfall[index]
        end if
                //set lowest and check each input
        if rainfall[index] < lowest then
            lowest = rainfall[index]
        end if
    end for 

                //calculate average
    set avgRain = total / SIZE
                //Display data
    Display "Total rainfall for the year is", total
    Display "Average rainfall for the year is", avgRain
    Display "Highest rainfall for the year is", highest
    Display "Lowest rainfall for the year is", lowest
end module

## Number Analysis Program

Design a program that asks the user to enter a series of 20 numbers. The program should store the numbers in an array and then display the following data:
```
The lowest number in the array

The highest number in the array

The total of the numbers in the array

The average of the numbers in the array
```

module main ()
                //declaration
    declare real total, avgNum, 
    constant integer SIZE = 20
    declare real numbers[SIZE]
    declare integer index 

                //for loop to gather number data
    for index = 0 to SIZE - 1
        Display "Enter numner ", index + 1, ": "
        input numbers[index]
        total += numbers[index]
    end for 
                //intialize variables before if statements
    set highest = numbers[0]
    set lowest = numbers[0]

                //check each input for highest and set
    for index = 0 to SIZE - 1
        if numbers[index] > highest then
            highest = numbers[index]
        end if
                //check each input and set lowest
        if numbers[index] < lowest then
            lowest = numbers[index]
        end if

                //calculate average
    set avgNum = total / SIZE

                //Display data
    Display "Total numbers in the array: ", total
    Display "Average number in the array: ", avgNum
    Display "Highest number in the array: ", highest
    Display "Lowest number in the array: ", lowest

end module



## Charge Account Validation

Design a program that asks the user to enter a charge account number. The program should determine whether the number is valid by comparing it to the following list of valid charge account numbers:
```
5658845  4520125  7895122  8777541  8451277  1302850
8080152  4562555  5552012  5050552  7825877  1250255
1005231  6545231  3852085  7576651  7881200  4581002
```
These numbers should be stored in an array. Use the sequential search algorithm to locate the number entered by the user. If the number is in the array, the program should display a message indicating the number is valid. If the number is not in the array, the program should display a message indicating the number is invalid.

module main()
                    //Declarations
    constant integer SIZE = 18
    declare integer accounts[SIZE] = 5658845, 4520125, 7895122, 8777541, 8451277, 1302850,
                                     8080152, 4562555, 5552012, 5050552, 7825877, 1250255,
                                     1005231, 6545231, 3852085, 7576651, 7881200, 4581002
    declare boolean found = False
    declare integer index = 0
    declare integer searchValue

                    //Get Search Value from user
    Display "Enter account number: "
    input searchValue

                    //step thru array to look for match
    While found == False AND index <= SIZE -1
        If accounts[index] == searchValue then
            set found = True
        Else 
            set index += 1
        end if
    end while

                    //Display results
    if found == True then
        Display searchValue, "is a valid account number"
    else if found == False then
        Display searchValue, "is NOT a valid account number"
    end if
end module

    

## Days of Each Month

Design a program that displays the number of days in each month. The program’s output should be similar to this:
```
January has 31 days.
February has 28 days.
March has 31 days.
April has 30 days.
May has 31 days.
June has 30 days.
July has 31 days.
August has 31 days.
September has 30 days.
October has 31 days.
November has 30 days.
December has 31 days.
```
The program should have two parallel arrays: a 12-element String array that is initialized with the names of the months, and a 12-element Integer array that is initialized with the number of days in each month. To produce the output specified, use a loop to step through the arrays getting the name of a month and the number of days in that month.

module main()
    constant integer SIZE = 12
    declare integer index
    declare string months[SIZE] = "January", "February", "March", "April", "May", "June", "July", "August", 
                                    "September", "October", "November", "December"
    declare integer days[SIZE] = 31, 28 ,31 ,30 ,31 ,30 ,31 ,31 ,30 ,31 ,30 ,31

    for index = 0 To SIZE -1
        Display months[index], " has ", days[index], " days."
    end for

## Phone Number Lookup

Design a program that has two parallel arrays: a String array named people that is initialized with the names of seven of your friends, and a String array named phoneNumbers that is initialized with your friends’ phone numbers. The program should allow the user to enter a person’s name (or part of a person’s name). It should then search for that person in the people array. If the person is found, it should get that person’s phone number from the phoneNumbers array and display it. If the person is not found in the people array, the program should display a message indicating so.

module main()
    constant integer SIZE = 7
    declare integer index
    declare string names[SIZE] = "January", "February", "March", "April", "May", "June", "July"
    declare integer phoneNum[SIZE] = 8675309, 8675309 ,8675309 ,8675309 ,8675309 ,8675309
                                 8675309 ,8675309 ,8675309 ,8675309 ,8675309 ,8675309
    declare boolean found = False
    declare integer index = 0
    declare integer searchValue

                    //Get Search Value from user
    Display "Enter the name to lookup: "
    input searchValue

                    //step thru array to look for match
    While found == False AND index <= SIZE -1
        If contains(names[index], searchValue) 
            set found = True
        Else 
            set index += 1
        end if
    end while

                    //Display results
    if found == True then
        Display names[index], "'s phone number is: " phoneNum[index]
    else if found == False then
        Display names[index], " was not found in the array."
    end if
end module

##  Payroll

Design a program that uses the following parallel arrays:

empId: An array of seven Integers to hold employee identification numbers. The array should be initialized with the following numbers:
```
56588 45201 78951 87775 84512 13028 75804
```
hours: An array of seven Integers to hold the number of hours worked by each employee.

payRate: An array of seven Reals to hold each employee’s hourly pay rate.

wages: An array of seven Reals to hold each employee’s gross wages.

The program should relate the data in each array through the subscripts. For example, the number in element 0 of the hours array should be the number of hours worked by the employee whose identification number is stored in element 0 of the empId array. That same employee’s pay rate should be stored in element 0 of the payRate array.

The program should display each employee number and ask the user to enter that employee’s hours and pay rate. It should then calculate the gross wages for that employee (hours times pay rate), which should be stored in the wages array. After the data has been entered for all the employees, the program should display each employee’s identification number and gross wages.

module main()
                //Declarations
    constant integer SIZE = 7
    declare integer index
    declare integer empId[SIZE] = 56588, 45201, 78951, 87775, 84512, 13028, 75804
    declare integer hours[SIZE]
    declare integer payRate[SIZE]
    declare integer wages[SIZE]

                //iterate thru array with user input 
    for index = 0 To SIZE -1
        Display empId[index]
        Display "Enter hours: "
        input hours[index]
        Display "Enter pay rate: "
        input payRate[index]
                //Calcuate wages or gross pay
        set wages[index] = hours[index] * payRate[index]
    end for

                //iterate thru array to Display Employee id and wages
    for index = 0 To SIZE -1
        Display empId[index]
        Display "Wages: ", wages[index]
    end for
end module

##  Driver’s License Exam

The local driver’s license office has asked you to design a program that grades the written portion of the driver’s license exam. The exam has 20 multiple choice questions. Here are the correct answers:
```
"B", "D", "A", "A", "C", "A", "B", "A", "C", "D", "B", "C", "D", "A", "D", "C", "C", "B", "D", "A"
```
Your program should store these correct answers in an array. (Store each question’s correct answer in an element of a String array.) The program should ask the user to enter the student’s answers for each of the 20 questions, which should be stored in another array. After the student’s answers have been entered, the program should display a message indicating whether the student passed or failed the exam. (A student must correctly answer 15 of the 20 questions to pass the exam.) It should then display the total number of correctly answered questions, the total number of incorrectly answered questions, and a list showing the question numbers of the incorrectly answered questions.

module main()
    constant integer SIZE = 20
    declare integer index
    declare string correctAnswers[SIZE] = "B", "D", "A", "A", "C", "A", "B", "A", "C", "D", "B", "C", "D", "A", "D",                                        "C", "C", "B", "D", "A"
    declare integer quizer[SIZE]
    declare integer right = 0
    declare integer wrong = 0
    declare integer index
    decalre string wrongList

                    //Get Search Value from user
    for index = 0 To SIZE -1
        Display "Enter your answer to question ", index + 1
        input quizer[index]
        if toUpper(quizer[index]) == correctAnswers[index] then 
            right += 1
        else if
            wrong += 1
            wrongList += "Question", index + 1, ", "
        end if
    end for

                    //Display pass or fail
    if score >=15 then
        Display "You Passed!"
    else 
        Display "You Failed!"
    end if

                    //Display score
    Display "Total number of correctly answered questions: ", right
    Display "Total number of incorrectly answered questions: ", right
#    Display "Question answered wrong: ", wrongList

end module

## Saddle Points

Design a program that has a two-dimensional integer array with 7 rows and 7 columns. The program should store a random number in each element. Then, the program should search the array for saddle points. A saddle point is an element whose value is less than or equal to all the other values in the same row, and greater than or equal to all the other values in the same column. The program should display all of the saddle point values found in the array (if any).

                 // Constants for the array sizes.
    Constant Integer ROWS = 7
  Constant Integer COLS = 7
 
  // An array to hold company sales.
  Declare integer randomArray[ROWS][COLS]
 
  // Counter variables
  Declare Integer row, col
 
  // Accumulator
  Declare integer hits = 0
  declare interger hitsValues[ROWS]

 
  // Display instructions.
 
  // Nested loops to fill the array with random numbers
  For row = 0 To ROWS − 1
     For col = 0 To COLS − 1
        Input randomArray[row][col] = random(0,9)
     End For
  End For
 
  // Nested loops to elements for saddle points.
  For row = 0 To ROWS − 1
     set highest = randomArray[row][0]
     For col = 0 To COLS − 1
        if 
        Set highest = sales[row][col]
     End For
  End For


## Tic-Tac-Toe Game

Design a program that allows two players to play a game of tic-tac-toe. Use a two-dimensional String array with three rows and three columns as the game board. Each element of the array should be initialized with an asterisk (*). The program should run a loop that does the following:
```
Displays the contents of the board array.

Allows player 1 to select a location on the board for an X. The program should ask the user to enter the row and column number.

Allows player 2 to select a location on the board for an O. The program should ask the user to enter the row and column number.

Determines whether a player has won or if a tie has occurred. If a player has won, the program should declare that player the winner and end. If a tie has occurred, the program should say so and end.

Player 1 wins when there are three Xs in a row on the game board. Player 2 wins when there are three Os in a row on the game board. The winning Xs or Os can appear in a row, in a column, or diagonally across the board. A tie occurs when all of the locations on the board are full, but there is no winner.
```
## Lo Shu Magic Square

The Lo Shu Magic Square is a grid with 3 rows and 3 columns shown in Figure below. The Lo Shu Magic Square has the following properties:
![image](https://user-images.githubusercontent.com/47218880/67577307-d1e73b00-f705-11e9-91ba-8acf75ad7a5d.png)

The grid contains the numbers 1 through 9 exactly.

The sum of each row, each column, and each diagonal all add up to the same number. This is shown in Figure below.
![image](https://user-images.githubusercontent.com/47218880/67577377-f9d69e80-f705-11e9-9907-1a522d98cc16.png)

In a program, you can simulate a magic square using a two-dimensional array. Design a program that initializes a two-dimensional array with values entered by the user. The program should determine whether the array is a Lo Shu Magic Square.
