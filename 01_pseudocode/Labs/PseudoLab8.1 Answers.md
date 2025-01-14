# Choose Two additional Programming Projects along with the (Mandatory) one. (Three Total) 

##  Payroll Program with Input Validation


Design a payroll program that prompts the user to enter an employee’s hourly pay rate and the number of hours worked. Validate the user’s input so that only pay rates in the range of $7.50 through $18.25 and hours in the range of 0 through 40 are accepted. The program should display the employee’s gross pay.

module main()
            //Declaration
    declare Real hours, payRate, grossPay

            //Get hours from user and check for 0-40
    Display "Enter number of hours worked: "
    input hours
    while hours < 0 OR hours > 40 then
        Display "Hours must be between 0 and 40. Try Again!"
        input hours
    end while
    
            //get pay rate and check for 7.5-18.25
    Display "Enter hourly pay rate: "
    input payRate
    while pay rate < 7.5 OR payRate > 18.25 then
        Display "Pay Rate must be between $7.50 - $18.25. Try Again!"
        input payRate
    end while

            //get gross pay and display
    set grossPay = hours * payRate
    Display "The gross pay is $", grossPay

end module

## Theater Seating Revenue with Input Validation

A dramatic theater has three seating sections, and it charges the following prices for tickets in each section: section A seats cost $20 each, section B seats cost $15 each, and section C seats cost $10 each. The theater has 300 seats in section A, 500 seats in section B, and 200 seats in section C. Design a program that asks for the number of tickets sold in each section and then displays the amount of income generated from ticket sales. The program should validate the numbers that are entered for each section.

module main()
                //Declaration
    declare integer ticketsA, ticketsB, ticketsC, total

                //Get A section tickets from user and check for 0-300
    Display "Enter # of tickets sold in A: "
    input ticketA
    while ticketA < 0 OR ticketA > 300
        Display "Invalid! Tickets must be btween 0 and 300"
        input ticketA
    end while

                //Get B section tickets from user and check for 0-500
    Display "Enter # of tickets sold in B: "
    input ticketB
    while ticketB < 0 OR ticketB > 500
        Display "Invalid! Tickets must be btween 0 and 500"
        input ticketB
    end while

                //Get C section tickets from user and check for 0-200
    Display "Enter # of tickets sold in C: "
    input ticketC
    while ticketC < 0 OR ticketC > 200
        Display "Invalid! Tickets must be btween 0 and 200"
        input ticketC
    end while

                //Display total sales from all tickets
    Display "Total sales in those sections were $", getTicketSales(ticketsA, ticketsB, ticketsC)

                //function to get total sales section A $20 each, section B $15 each, and section C $10 each
    function integer getTicketSales(integer a, integer b, integer c)
        declare integer total
        total = (a*20)+(b*15)+(c*10)
        return total
    end function
    
end module

## Fat Gram Calculator

Design a program that asks for the number of fat grams and calories in a food item. Validate the input as follows:

Make sure the number of fat grams and calories is not less than 0.

According to nutritional formulas, the number of calories cannot exceed "fat grams X 9 "

Make sure that the number of calories entered is not greater than "fat grams X 9"

Once correct data has been entered, the program should calculate and display the percentage of calories that come from fat. Use the following formula:

![image](https://user-images.githubusercontent.com/47218880/67504468-0ba93a80-f64f-11e9-85d0-f080ac66a64a.png)


percentage = (fatgrams * 9) / calories

Some nutritionists classify a food as “low fat” if less than 30 percent of its calories come from fat. If the results of this formula are less than 0.3, the program should display a message indicating the food is low in fat.

module main()
                //Declarations
    declare real fatGrams, calories, percentFat

                //get input and validate
    do
        display "Enter # of fat grams: "
        input fatGrams
        display "Enter total calories: "
        input calories
        if fatGrams < 0 OR calories < 0 OR calories > (fatGrams*9) then
            Display "Invalid! Cannot be a negative number and the number of calories cannot exceed fat grams X 9
        end if
    while fatGrams < 0 OR calories < 0 OR calories > (fatGrams*9)   

                //calculate percent 
    set percentFat = getPercentFat(fatGrams, calories)

                //display messages
    if percentFact <= 0.3 then
        Display "This is a Low Fat food! Only ", percentFat*100, " % of its calories come from fat."
    else
        Display "This food has ", percentFat*100, " % of its calories come from fat.

                //function for fat percentage
    function real getPercentFat(real fat, real cal)
        return ((fat * 9) / cal)


## Speeding Violation Calculator

Design a program that calculates and displays the number of miles per hour over the speed limit that a speeding driver was doing. The program should ask for the speed limit and the driver’s speed. Validate the input as follows:

The speed limit should be at least 20, but not greater than 70.

The driver’s speed should be at least the value entered for the speed limit ­(otherwise the driver was not speeding).
Once correct data has been entered, the program should calculate and display the number of miles per hour over the speed limit that the driver was doing.

module main()
                //Declaration
    declare integer speeder, limit

            //get speed limit and validate it is between 20-70 mph
    display "Enter speed limit: "
    input limit
    while limit < 20 OR limit > 70
        Display "The speed limit needs to be 20-70 mph. Please try again"
        input limit
    end while
        
            // get speeder's speed and validat that it is larger than the speed limit
    display "Enter speed of speeder: "
    input speeder
    while speeder < limit
        Display "The Speed should be bigger than the speed limit ­(otherwise the driver was not speeding)."
        input speeder
    end while

    Display "Your speeder was", (speeder-limit), " mph over the limit"




# Rock, Paper, Scissors Modification (MANDATORY)

In a previous Programming Exercise option you were asked to design a program that plays the Rock, Paper, Scissors game. In the program, the user enters one of the three strings—"rock", "paper", or "scissors"—at the keyboard. Add input validation (with a case-insensitive comparison) to make sure the user enters one of those strings only.
(If you didnt design one, here is a version of that game program to work with) 

/// declare string doAgain = 'n'

module main()

    declare integer computerNum, userNum
    declare string userString
                        // do while will continue until players give different answers, no ties allowed
    do 
                        // set computer's random guess
        set computerNum = random(1, 3)
                        //get user's guess
        display "Enter 'rock', 'paper' or 'scissors': "
        input userString
                        // validate user's guess
        while toLower(str) != 'rock' AND toLower(str) != 'paper' AND toLower(str) != 'scissors' then
            Display "Invalid! Please try again!"
            input userString
        end while
                        //turn string that user entered into 1,2, or 3
        set userNum = getWordsToNum(userString)
                        //display computer's random guess
        display "Computers choice was ", getNumToWords(computerNum)
                        //check the guesses for a winner
        Call getWinner(computerNum, userNum)
    until computerNum != userNum

                        //this function has no return but displays output if winner
    function integer getWinner(integer computer, integer user)
        if computer == 1 AND user == 3 then
            Display "The computer won!"
        else if computer == 3 AND user == 1 then
            Display "The user won!"
        else if computer == 2 AND user == 1 then
            Display "The computer won!"
        else if computer == 1 AND user == 2 then
            Display "The user won!"
        else if computer == 3 AND user == 2 then
            Display "The computer won!"
        else if computer == 2 AND user == 3 then
            Display "The user won!"
        else
            Display "Both players make the same choice, the game must be played again!"
        return 0
    end function

                    //this function changes the string to integer
    function integer getWordsToNum(string str)
        declare integer num
        if toLower(str) == "rock" then
            set num = 1
        else if toLower(str) == "paper" then
            set num = 2
        else if toLower(str) == "scissors" then
            set num = 3
    return num
    end function

                // function to turn integer into strings
    function string getNumToWords(integer num)
        declare string str
        if num ==1 then
            set str = "rock"
        else if num ==2 then
            set str = "paper"
        else if num == 3 then
            set str = "scissors"
    return str
    end function
end module





### Program "Rock,Paper,Scissors"

```
                // main module
Module main()
                // Local variables
    Declare Integer computer, player

                // Get computer number
    Set computer = Rand(1, 3)

                // Get player number
    Call getNumber(player)

                // Show winner
    Call showWinner(computer, player)

End Module

                // The getNumber module gets an integer
Module getNumber(Integer Ref inputAnswer)
		Display “Enter 1 for rock, 2 for paper, 3 for scissors:  “
		Input inputAnswer
End Module

                // The showWinner module shows if number is a prime
Module showWinner(Integer computer, player)
Declare Integer which

Display “Computer chose “, whichChoice(computer)
If computer == player Then
	Display “Player made same choice.  Play again.”
Else
Set which = whoWon(computer, player)
If which == 1 Then
		Display “Computer wins.”
Else
If which == 2 Then
			Display “Player wins.”
		Else
			Display “No winner.”
		End If
End If
End If

End Module

                // The whichChoice function displays choice 
Function String whichChoice (Integer number)

    If number == 1 Then
	    Return “rock”
    Else if number == 2 Then
		Return “paper”
    Else if
		Return “scissors"
    End If

End Function

            // The whoWon function selects winner 
Function Integer whoWon(computer, player)
            // 1 = rock, 2 = paper, 3 = scissors
            // rock smashes scissors
            // scissors cuts paper
            // paper wraps rock

	        // both choose same no winner
If computer == player then
		Return 0
	End If

	            // test computer chose rock
	If computer == 1 then
		If player == 2 then
			Return 2  // paper wraps rock
		End If
Else
		If player == 3 then
			Return 1  // rock smashes scissors
		End If
End If

	        // test computer chose paper
	If computer == 2 then
		If player == 1 then
			Return 1  // paper wraps rock
		End If
Else
		If player == 3 then
			Return 2  // scissors cuts paper
		End If
End If

	            // test computer chose scissors
	If computer == 3 then
		If player == 1 then
			Return 2  // rock smashes scissors 
		End If
Else
		If player == 2 then
			Return 1  // scissors cuts paper
		End If
End If

	Return 0

End Function
```
