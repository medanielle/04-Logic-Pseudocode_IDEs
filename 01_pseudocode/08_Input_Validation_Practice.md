# Input Validation Exercise Workbench

Design an algorithm that prompts the user to enter a positive nonzero number and validates the input.

Display "Enter a positive nonzero
input num
while num <= 0 then 
   Display "Invalid"
   input number
end while

Design an algorithm that prompts the user to enter a number in the range of 1 through 100 and validates the input.

Display "Enter a number (1-100)"
input num
while num < 1 OR num >100 then 
   Display "Invalid"
   input num
end while

Design an algorithm that prompts the user to enter “yes” or “no” and validates the input. (Use a case-insensitive comparison.)

Display "Enter “yes” or “no”"
input str
while toLower(str) != 'yes' AND toLower(str) != 'no' then 
   Display "Invalid"
   input str
end while

Design an algorithm that prompts the user to enter a number that is greater than 99 and validates the input.

Display "Enter a number over 99"
input num
while num >= 99 then 
   Display "Invalid"
   input num
end while

Design an algorithm that prompts the user to enter a secret word. The secret word should be at least 8 characters long. Validate the input.''

Display "Enter an 8 char secret word"
input str
while len(str) != 8 then 
   Display "Invalid"
   input str
end while

# Debugging Exercises

Why does the following pseudocode not perform as indicated in the comments?
Original:
```
// This program asks the user to enter a value
// between 1 and 10 and validates the input.
Declare Integer value

// Get a value from the user.
Display "Enter a value between 1 and 10."
Input value

// Make sure the value is between 1 and 10.
While value < 1 AND value > 10
   Display "ERROR: The value must be between 1 and 10."
   Display "Enter a value between 1 and 10."
   Input value
End While
```
Fixed:

// This program asks the user to enter a value
// between 1 and 10 and validates the input.
Declare Integer value

// Get a value from the user.
Display "Enter a value between 1 and 10."
Input value

// Make sure the value is between 1 and 10.
While value < 1 OR value > 10                        ***needs to be an OR
   Display "ERROR: The value must be between 1 and 10."
   Display "Enter a value between 1 and 10."
   Input value
End While

Why does the following pseudocode not perform as indicated in the comments?
```
// This program gets a dollar amount from the user
// and validates the input.
Declare Real amount

// Get the amount from the user.
Display "Enter a dollar amount"
Input amount

// Make sure the amount is not less than zero. If it is,
// get a new amount from the user.
While amount < 0
   Display "ERROR: The dollar amount cannot be less than 0."
   Display "Enter a dollar amount."
End While
```
Fixed:
// This program gets a dollar amount from the user
// and validates the input.
Declare Real amount

// Get the amount from the user.
Display "Enter a dollar amount"
Input amount

// Make sure the amount is not less than zero. If it is,
// get a new amount from the user.
While amount < 0
   Display "ERROR: The dollar amount cannot be less than 0."
   Display "Enter a dollar amount."
   input amount                                                      ***added this line
End While

The following pseudocode works, but it performs a case-sensitive validation of the user’s input. How could the algorithm be improved so the user does not have to pay attention to capitalization when entering a name?
```
// This program asks the user to enter a string
// and validates the input.
Declare String choice

// Get the user's response.
Display "Cast your vote for Chess Team Captain."
Display "Would you like to nominate Lisa or Tim?"
Input choice

// Validate the input.
While choice != "Lisa" AND choice != "Tim"
   Display "Please enter Lisa or Tim."
   Display "Cast your vote for Chess Team Captain."
   Display "Would you like to nominate Lisa or Tim?"
   Input response
End While
```
Fixed:

// This program asks the user to enter a string
// and validates the input.
Declare String choice

// Get the user's response.
Display "Cast your vote for Chess Team Captain."
Display "Would you like to nominate Lisa or Tim?"
Input choice

// Validate the input.
While toLower(choice) != "lisa" AND toLower(choice) != "tim"         **** added to lower() 
   Display "Please enter Lisa or Tim."
   Display "Cast your vote for Chess Team Captain."
   Display "Would you like to nominate Lisa or Tim?"
   Input response
End While