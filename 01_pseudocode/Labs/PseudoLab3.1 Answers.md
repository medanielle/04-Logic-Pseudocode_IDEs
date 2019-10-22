1. Design an If-Then statement (or a flowchart with a single alternative decision structure) that assigns 20 to the variable y and assigns 40 to the 
variable z if the variable x is greater than 100.

if x > 100 then
	y = 20
	z =40
end if

2. Design an If-Then statement (or a flowchart with a single alternative decision structure) that assigns 0 to the variable b and assigns 1 to the 
variable c if the variable a is less than 10.

if a < 10 then	
	b = 0
	c = 1
end if

3. Design an If-Then-Else statement (or a flowchart with a dual alternative decision structure) that assigns 0 to the variable b if the variable a is less than 10. 
Otherwise, it should assign 99 to the variable b.

if a < 10 then
	b = 0
else 
	b = 99
end if

4. The following pseudocode contains several nested If-Then-Else statements. Unfortunately, it was written without proper alignment and indentation. 
Rewrite the code and use the proper conventions of alignment and indentation.
```
If score < 60 Then
Display "Your grade is F."
Else
If score < 70 Then
Display "Your grade is D."
Else
If score < 80 Then
Display "Your grade is C."
Else
If score < 90 Then
Display "Your grade is B."
Else
Display "Your grade is A."
End If
End If
End If
End If
```

If score < 60 Then
	Display "Your grade is F."
Else
	If score < 70 Then
		Display "Your grade is D."
	Else
		If score < 80 Then
			Display "Your grade is C."
		Else
			If score < 90 Then
				Display "Your grade is B."
			Else
				Display "Your grade is A."
			End If
		End If
	End If
End If


5. Design nested decision structures that perform the following: If amount1 is greater than 10 and amount2 is less than 100, display the greater of amount1 and amount2.

if amount1 > 10 AND amount2 <100 then
	if amount1 > amount2 then
		Display amount1
	else 
		Display amount2
	end if
end if
	

6. Rewrite the following If-Then-Else If statement as a Select Case statement.
```
If selection == 1 Then
   Display "You selected A."
Else If selection == 2 Then
   Display "You selected 2."
Else If selection == 3 Then
   Display "You selected 3."
Else If selection == 4 Then
   Display "You selected 4."
Else
   Display "Not good with numbers, eh?"
End If
```

Case based on selection
	Case == 1
		Display "You selected A."
	Case == 2 
		Display "You selected 2."
	Case == 3 Then
		Display "You selected 3."
	Case == 4 Then
		Display "You selected 4."
	Default
		Display "Not good with numbers, eh?"
End Case


7. Design an If-Then-Else statement (or a flowchart with a dual alternative decision structure) that displays “Speed is normal” if the speed variable is 
within the range of 24 to 56. If speed holds a value outside this range, display “Speed is abnormal.”


if speed > 24 AND speed < 56 then
	Display “Speed is normal”
Else
	Display “Speed is abnormal.”
End if


8. Design an If-Then-Else statement (or a flowchart with a dual alternative decision structure) that determines whether the points variable 
is outside the range of 9 to 51. If the variable holds a value outside this range it should display “Invalid points.” Otherwise, it should display “Valid points.”

if points < 9 AND points > 51 then
	Display “Invalid points.”
Else 
	Display “Valid points.”
End if


9. Design a case structure that tests the month variable and does the following:

* If the month variable is set to 1, it displays “January has 31 days.”

* If the month variable is set to 2, it displays “February has 28 days.”

* If the month variable is set to 3, it displays “March has 31 days.”

* If the month variable is set to anything else, it displays “Invalid selection.”


Case based on month
	Case == 1
		Display “January has 31 days.”
	Case == 2 
		Display “February has 28 days.”
	Case == 3 Then
		Display “March has 31 days.”
	Default
		Display “Invalid selection.”
End Case

10. Write an If-Then statement that sets the variable hours to 10 when the flag variable minimum is set.

if flag = 0 then
	hours == 10
end if



Design a flowchart or pseudocode for a program that accepts three numbers from a user and displays a message if the sum of any two numbers equals the third.
TEACH:
Start
	Declarations 
		num firstNum, secondNum, thirdNum
		string MSG= "Got it!"
	
		GetNum()
		Calc()
		finish()
	stop
	
	GetNum()
		output "Enter three Numbers: "
		input firstNum, secondNum, thirdNum
	return
	
	Calc()
		if ((firstNum + secondNum == thirdNum) OR (secondNum + thirdNum == firstNum) OR (firstNum + thirdNum ==secondNum) then
			output MSG
			
Stop


ME:
	Display "Enter first number:"
	input firstnum
	Display "Enter second number:"
	input secondNum
	Display "Enter third number:"
	input thirdNum

ALONE:


ShoppingBay is an online auction service that requires several reports. Data for each auctioned item includes an ID number, item description, 
length of auction in days, and minimum required bid. Design a flowchart or pseudocode for the following:

	A program that accepts data for one auctioned item. Display data for an auction only if the minimum required bid is more than $250.00.
TEACH:


ME:
Main
Start
	Declare num IDnum, LengthDays, MinBid
	Declare string Descrip
	Declare CONSTANT integer MinReqBid = 250
	GetData()
	GetMinReq()
	
	GetMinReq()	
		if MinBid > MinReqBid then
			Output "ID number is " IDnum, ", item description is ", Descrip, ", length of auction is ", LengthDays, " days, and minimum required bid is $", MinBid
		end if
	return
		
	GetData()
		Output "Enter ID number: "
		Input IDnum
		Output "Enter item description: "
		Input Descrip
		Output "Length of auction in days: "
		Input LengthDays
		Output "Minimum required bid: "
		Input MinBid
	return
stop
	

	A program that continuously accepts auction item data until a sentinel value is entered and displays all data for auctions in which the 
	minimum required bid is more than $300.00.
	
Main 
Start
	Declare integer IDnum, LengthDays
	Declare REAL MinBid
	Declare string Descrip
	Declare CONSTANT integer MinReqBid = 300
	Declare integer num flagVar = 1
	
	GetLoop()
	
	GetLoop()
		while flagVar == 1 then
			GetData()
			GetMinReq()
			Output "Do you want to add another item? enter 1 for yes, and 0 for no :"
			Input flagVar
		end while
	return
	
	GetMinReq()	
		if MinBid > MinReqBid then
			Output "ID number is " IDnum, ", item description is ", Descrip, ", length of auction is ", LengthDays, " days, and minimum required bid is $", MinBid
		end if
	return
		
	GetData()
		Output "Enter ID number: "
		Input IDnum
		Output "Enter item description: "
		Input Descrip
		Output "Length of auction in days: "
		Input LengthDays
		Output "Minimum required bid: "
		Input MinBid
	return
Stop
	
	A program that continuously accepts auction item data and displays data for every auction in which there are no bids yet (in other words, 
	the minimum bid is $0.00) and the length of the auction is seven days or less.
	
Main 
Start
	Declare integer IDnum, LengthDays
	Declare REAL MinBid
	Declare string Descrip
	Declare CONSTANT integer MinReqBid = 0
	Declare integer num flagVar = 1
	
	GetLoop()
	
	GetShortZero()
		if MinBid == 0 AND LengthDays < 8 then
			Output "ID number is " IDnum, ", item description is ", Descrip, ", length of auction is ", LengthDays, " days, and minimum required bid is $", MinBid
		end if
	return
	
	GetLoop()
		while flagVar == 1 then
			GetData()
			GetShortZero()
			Output "Do you want to add another item? enter 1 for yes, and 0 for no :"
			Input flagVar
		end while
	return
	
	GetMinReq()	
		if MinBid > MinReqBid then
			Output "ID number is " IDnum, ", item description is ", Descrip, ", length of auction is ", LengthDays, " days, and minimum required bid is $", MinBid
		end if
	return
		
	GetData()
		Output "Enter ID number: "
		Input IDnum
		Output "Enter item description: "
		Input Descrip
		Output "Length of auction in days: "
		Input LengthDays
		Output "Minimum required bid: "
		Input MinBid
	return
Stop
	
	A program that continuously accepts auction data and displays data for every auction in which the length is between 14 and 28 days inclusive.

Main 
Start
	Declare integer IDnum, LengthDays
	Declare REAL MinBid
	Declare string Descrip
	Declare CONSTANT integer MinReqBid = 0
	Declare integer num flagVar = 1
	
	GetLoop()
	
	Get2or3Weeks()
		if LengthDays <= 14 AND LengthDays >= 28 then
			Output "ID number is " IDnum, ", item description is ", Descrip, ", length of auction is ", LengthDays, " days, and minimum required bid is $", MinBid
		end if
	return
	
	GetShortZero()
		if MinBid == 0 AND LengthDays < 8 then
			Output "ID number is " IDnum, ", item description is ", Descrip, ", length of auction is ", LengthDays, " days, and minimum required bid is $", MinBid
		end if
	return
	
	GetLoop()
		while flagVar == 1 then
			GetData()
			Get2or3Weeks()
			Output "Do you want to add another item? enter 1 for yes, and 0 for no :"
			Input flagVar
		end while
	return
	
	GetMinReq()	
		if MinBid > MinReqBid then
			Output "ID number is " IDnum, ", item description is ", Descrip, ", length of auction is ", LengthDays, " days, and minimum required bid is $", MinBid
		end if
	return
		
	GetData()
		Output "Enter ID number: "
		Input IDnum
		Output "Enter item description: "
		Input Descrip
		Output "Length of auction in days: "
		Input LengthDays
		Output "Minimum required bid: "
		Input MinBid
	return
Stop


	A program that prompts the user for a maximum required bid, and then continuously accepts auction data and displays data for every auction in 
	which the minimum bid is less than or equal to the amount entered by the user.

Main 
Start
	Declare integer IDnum, LengthDays, MinReqBid
	Declare REAL MinBid
	Declare string Descrip
	Declare integer flagVar = 1
	
	Output "What is your max req bid?"
	input MinReqBid
	
	GetLoop()
	
	Get2or3Weeks()
		if LengthDays <= 14 AND LengthDays >= 28 then
			Output "ID number is " IDnum, ", item description is ", Descrip, ", length of auction is ", LengthDays, " days, and minimum required bid is $", MinBid
		end if
	return
	
	GetShortZero()
		if MinBid == 0 AND LengthDays < 8 then
			Output "ID number is " IDnum, ", item description is ", Descrip, ", length of auction is ", LengthDays, " days, and minimum required bid is $", MinBid
		end if
	return
	
	GetLoop()
		while flagVar == 1 then
			GetData()
			GetMinReq()
			Output "Do you want to add another item? enter 1 for yes, and 0 for no :"
			Input flagVar
		end while
	return
	
	GetMinReq()	
		if MinBid > MinReqBid then
			Output "ID number is " IDnum, ", item description is ", Descrip, ", length of auction is ", LengthDays, " days, and minimum required bid is $", MinBid
		end if
	return
		
	GetData()
		Output "Enter ID number: "
		Input IDnum
		Output "Enter item description: "
		Input Descrip
		Output "Length of auction in days: "
		Input LengthDays
		Output "Minimum required bid: "
		Input MinBid
	return
Stop























