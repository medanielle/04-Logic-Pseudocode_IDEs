~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

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

~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


ShoppingBay is an online auction service that requires several reports. Data for each auctioned item includes an ID number, item description, 
length of auction in days, and minimum required bid. Design a flowchart or pseudocode for the following:

1.	A program that accepts data for one auctioned item. Display data for an auction only if the minimum required bid is more than $250.00.
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
	

2.	A program that continuously accepts auction item data until a sentinel value is entered and displays all data for auctions in which the 
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
	
3.	A program that continuously accepts auction item data and displays data for every auction in which there are no bids yet (in other words, 
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
	
4.	A program that continuously accepts auction data and displays data for every auction in which the length is between 14 and 28 days inclusive.

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
	
	GetLoop()
		while flagVar == 1 then
			GetData()
			Get2or3Weeks()
			Output "Do you want to add another item? enter 1 for yes, and 0 for no :"
			Input flagVar
		end while
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


5.	A program that prompts the user for a maximum required bid, and then continuously accepts auction data and displays data for every auction in 
	which the minimum bid is less than or equal to the amount entered by the user.

Main 
Start
	Declare integer IDnum, LengthDays, MinReqBid
	Declare REAL MinBid
	Declare string Descrip
	Declare integer flagVar = 1
	
	Output "What is your max req bid?"
	input MaxReqBid
	
	GetLoop()
	
	GetLoop()
		while flagVar == 1 then
			GetData()
			GetMaxReq()
			Output "Do you want to add another item? enter 1 for yes, and 0 for no :"
			Input flagVar
		end while
	return
	
	GetMaxReq()	
		if MinBid <= MaxReqBid then
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
