Exercise Workbench  Day 4 Functions

    1. As shown in this chapter, write a pseudocode statement that generates a random number in the range of 1 through 100 and assigns it to a variable named rand.

        decalre real rand
        set rand = random(1, 100)

    2. The following pseudocode statement calls a function named half, which returns a value that is half that of the argument. (Assume both the result and number variables are Real.) Write pseudocode for the function.

        Set result = half(number)

        Function Integer half(integer num)
            return num / 2
        End Function

    3. A pseudocode program contains the following function definition:

	Function Integer cube(Integer num)
        Return num * num * num
    End Function

    Write a statement that passes the value 4 to this function and assigns its return value to the variable result.

    set result = cube(4)

    4. Design a pseudocode function named timesTen that accepts an Integer argument. When the function is called, it should return the value of its argument multiplied times 10.

        Function Integer timesTen(integer num)
            return num * 10
        End Function


    5. Design a pseudocode function named getFirstName that asks the user to enter his or her first name, and returns it.

        Function String getFirstName()
            Display "WHat your name?"
            input firstName
            return firstName
        end Function

    6. Assume that a program has two String variables named str1 and str2. Write a pseudocode statement that assigns an all uppercase version of str1 to the str2 variable.

        Function string getSomething(string str1)
            set str2 = toUpper(str1)
            return str2
        end Function


Debugging Exercises
The programmer intends for this pseudocode to display three random numbers in the range of 1 through 7. According to the way we’ve been generating random numbers in this book, however, there appears to be an error. Can you find it?

Original:
    1. // This program displays three random numbers
    2. // in the range of 1 through 7.
    3. Declare Integer count
    4. 
    5. // Display three random numbers.
    6. For count = 1 To 3
    7.    Display random(7, 1)
End For

Fixed:
    1. // This program displays three random numbers
    2. // in the range of 1 through 7.
    3. Declare Integer count
    4. 
    5. // Display three random numbers.
    6. For count = 1 To 3
    7.    Display random(1, 7)                              *** wrong order
End For

Can you find the reason that the following pseudocode function does not return the value indicated in the comments?

Original:
    1. // The calcDiscountPrice function accepts an item's price and
    2. // the discount percentage as arguments. It uses those
    3. // values to calculate and return the discounted price.
    4. Function Real calcDiscountPrice(Real price, Real percentage)
    5.    // Calculate the discount.
    6.    Declare Real discount = price * percentage
    7. 
    8.    // Subtract the discount from the price.
    9.    Declare Real discountPrice = price – discount
    10. 
    11.    // Return the discount price.
    12.    Return discount
End Function

Fixed:    
    1. // The calcDiscountPrice function accepts an item's price and
    2. // the discount percentage as arguments. It uses those
    3. // values to calculate and return the discounted price.
    4. Function Real calcDiscountPrice(Real price, Real percentage)
    5.    // Calculate the discount.
    6.    Declare Real discount = price * percentage
    7. 
    8.    // Subtract the discount from the price.
    9.    Declare Real discountPrice = price – discount
    10. 
    11.    // Return the discount price.
    12.    Return discountPrice                             *** wrong variable returned
End Function

Can you find the reason that the following pseudocode does not perform as indicated in the comments?

Original:
    1. // Find the error in the following pseudocode.
    2. Module main()
    3.     Declare Real value, result
    4. 
    5.     // Get a value from the user.
    6.     Display "Enter a value."
    7.     Input value
    8. 
    9.     // Get 10 percent of the value.
    10.     Call tenPercent(value)
    11.
    12.     // Display 10 percent of the value.
    13.     Display "10 percent of ", value, " is ", result
    14. End Module
    15. 
    16. // The tenPercent function returns 10 percent
    17. // of the argument passed to the function.
    18. Function Real tenPercent(Real num)
    19.     Return num * 0.1
End Function

Fixed:
    1. // Find the error in the following pseudocode.
    2. Module main()
    3.     Declare Real value, result
    4. 
    5.     // Get a value from the user.
    6.     Display "Enter a value."
    7.     Input value
    8. 
    9.     // Get 10 percent of the value.
    10.    set result = tenPercent(value)           *** just called function didn't set it(results)
    11.
    12.    // Display 10 percent of the value.
    13.    Display "10 percent of ", value, " is ", result
    14. End Module
    15. 
    16. // The tenPercent function returns 10 percent
    17. // of the argument passed to the function.
    18. Function Real tenPercent(Real num)
    19.     Return num * 0.1
End Function
