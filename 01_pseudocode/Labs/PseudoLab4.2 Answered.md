# CHOOSE THREE PROMPTS (unless mandatory ones are assigned)

# Roman Numerals

Design a program that prompts the user to enter a number within the range of 1 through 10. The program should display the Roman numeral version of that number. If the number is outside the range of 1 through 10, the program should display an error message.

module main()
            //Decalre variables
        declare int userNum
        getData()
        getRoman()

    module getData()
                //get data from user function, and check for correctness
        Display "Enter a number 1-10: "
        input userNum
        if userNum <1 OR userNum >10 then
            Display "Error, number out of range"
    
    module getRoman()
                    ///this function prints the correct roman numeral
        select userNum
            Case 1:
                Display userNum, " is I in Roman numerals"
            Case 2:
                Display userNum, " is II in Roman numerals"
            Case 3:
                Display userNum, " is III in Roman numerals"
            Case 4:
                Display userNum, " is IV in Roman numerals"
            Case 5:
                Display userNum, " is V in Roman numerals"
            Case 6:
                Display userNum, " is VI in Roman numerals"
            Case 7:
                Display userNum, " is VII in Roman numerals"
            Case 8:
                Display userNum, " is VIII in Roman numerals"
            Case 9:
                Display userNum, " is IX in Roman numerals"
            Case 10:
                Display userNum, " is X in Roman numerals"
            Default:
                Display "Error, number out of range"
    
    


# Areas of Rectangles

The area of a rectangle is the rectangle’s length times its width. Design a program that asks for the length and width of two rectangles. The program should tell the user which rectangle has the greater area, or whether the areas are the same.

main module()
                //Declaration
    declare Real box1Length, box1Width, box2Length, box2Width, box1Area, box2Area 

    getBoxes(box1Length, box1Width, box2Length, box2Width)
    getArea(box1Area, box2Area)
    getResults(box1Area, box2Area)

    module getBoxes(Real Ref box1Length, Real Ref box1Width, Real Ref box2Length, Real ref box2Width,)
                //Get Data on Boxes from user
        Display "Enter 1st Boxes Length: "
        input box1Length
        Display "Enter 1st Boxes Width: "
        input box1Width       
        Display "Enter 2nd Boxes Length: "
        input box2Length
        Display "Enter 2nd Boxes Width: "
        input box2Width

    module getCalc(Real Ref box1Area, Real Ref box2Area)
                //get areas for the boxes
        Set box1Area = box1Length * box1Width
        Set box2Area = box2Length * box2Width 

    module getResults()
                //Display results to user
        if box1Area > box2Area then
            Display "The first box has the greater area!"
        else if box2Area > box1Area then
            Display "The second box has the greater area!"
        else
            Display "They have the same area!"


# Mass and Weight

Scientists measure an object’s mass in kilograms and its weight in Newtons. If you know the amount of mass of an object, you can calculate its weight, in Newtons, with the following formula:

![image](https://user-images.githubusercontent.com/47218880/67404289-c6b2d480-f578-11e9-80c0-9bfa15de3df7.png)

        Weight = mass * 9.8

Design a program that asks the user to enter an object’s mass, and then calculates its weight. If the object weighs more than 1,000 Newtons, display a message indicating that it is too heavy. If the object weighs less than 10 Newtons, display a message indicating that it is too light.

main module()
                //Declaration
    declare Real mass, newtons 

    getMass(mass)
    getNewtons(newtons)
    getResults(newtons)

    module getMass(Real ref mass)
                //Get Data on Mass from user
        Display "Enter Mass in kg: "
        input mass
    end module

    module getNewtons(Real ref newtons)
                //calculate newtons from kilograms
        set newtons = mass * 9.8
    end module

    module getResults(Real newtons)
                //Display results to user
        if newtons > 1000 then
            Display "It is too heavy!"
        else if newtons < 10 then
            Display "It is too light!"
        else
            Display "It's weight is ", newtons, " Newtons!"
    end module

# Magic Dates

The date June 10, 1960, is special because when it is written in the following format, the month times the day equals the year:

![image](https://user-images.githubusercontent.com/47218880/67404336-d92d0e00-f578-11e9-9801-6742f67d71fe.png)

        6/10/60

Design a program that asks the user to enter a month (in numeric form), a day, and a two-digit year. The program should then determine whether the month times the day equals the year. If so, it should display a message saying the date is magic. Otherwise, it should display a message saying the date is not magic.

# Color Mixer

The colors red, blue, and yellow are known as the primary colors because they cannot be made by mixing other colors. When you mix two primary colors, you get a secondary color, as shown here:
```
When you mix red and blue, you get purple.

When you mix red and yellow, you get orange.

When you mix blue and yellow, you get green.
```
Design a program that prompts the user to enter the names of two primary colors to mix. If the user enters anything other than “red,” “blue,” or “yellow,” the program should display an error message. Otherwise, the program should display the name of the secondary color that results.

main module()
                // Declaration
    declare string primary1, primary2
                //Get colors from users
    GetColors()
        Display "Enter first primary color: "
        input primary1
        Display "Enter second Primary color: "
        input primary2
    
    checkColors()
        if primary1 == 'red' OR primary1 == 'blue' OR primary1 == "yellow" then
            pass
        else 
            Display "Error, you didn't enter a primary color"
            exit
    
    printResults()
        if p



# Book Club Points

Serendipity Booksellers has a book club that awards points to its customers based on the number of books purchased each month. The points are awarded as follows:
```
If a customer purchases 0 books, he or she earns 0 points.

If a customer purchases 1 book, he or she earns 5 points.

If a customer purchases 2 books, he or she earns 15 points.

If a customer purchases 3 books, he or she earns 30 points.

If a customer purchases 4 or more books, he or she earns 60 points.
```

Design a program that asks the user to enter the number of books that he or she has purchased this month and displays the number of points awarded.

# Software Sales

A software company sells a package that retails for $99. Quantity discounts are given according to the following table:

![image](https://user-images.githubusercontent.com/47218880/67404439-04aff880-f579-11e9-8496-6a778d4ce7d1.png)

Design a program that asks the user to enter the number of packages purchased. The program should then display the amount of the discount (if any) and the total amount of the purchase after the discount.

# Change for a Dollar Game

Design a change-counting game that gets the user to enter the number of coins required to make exactly one dollar. The program should ask the user to enter the number of pennies, nickels, dimes, and quarters. If the total value of the coins entered is equal to one dollar, the program should congratulate the user for winning the game. Otherwise, the program should display a message indicating whether the amount entered was more than or less than one dollar.

# Shipping Charges

The Fast Freight Shipping Company charges the following rates:
![image](https://user-images.githubusercontent.com/47218880/67404533-26a97b00-f579-11e9-8944-5cfaa2dc2729.png)
Design a program that asks the user to enter the weight of a package and then displays the shipping charges.

# Time Calculator

Design a program that asks the user to enter a number of seconds, and works as follows:

* There are 60 seconds in a minute. If the number of seconds entered by the user is greater than or equal to 60, the program should display the number of minutes in that many seconds.

* There are 3,600 seconds in an hour. If the number of seconds entered by the user is greater than or equal to 3,600, the program should display the number of hours in that many seconds.

* There are 86,400 seconds in a day. If the number of seconds entered by the user is greater than or equal to 86,400, the program should display the number of days in that many seconds.

# Leap Year Detector

Design a program that asks the user to enter a year, and then displays a message indicating whether that year is a leap year or not. Use the following logic to develop your algorithm:

* If the year is evenly divisible by 100 and is also evenly divisible by 400, then it is a leap year. For example, 2000 is a leap year but 2010 is not.

* If the year is not evenly divisible by 100, but it is evenly divisible by 4, it is a leap year. For example, 2008 is a leap year but 2009 is not.
