# Select 5 Programming projects from the list

## Rectangle Area

The area of a rectangle is calculated according to the following formula:

![image](https://user-images.githubusercontent.com/47218880/67446156-3e165180-f5d5-11e9-8673-1dab25034bff.png)

Area = Width * Length

Design a function that accepts a rectangle’s width and length as arguments and returns the rectangle’s area. Use the function in a program that prompts the user to enter the rectangle’s width and length, and then displays the rectangle’s area.

module Main()
    declare integer userWidth, userLength

    display "Please enter width: "
    input userWidth
    display "please enter length: "
    input userLength
    Display "Here is the area: ", getArea(userWidth, userLength)

    Function Integer getArea(width, length)
        return width * length
    end function
end Module

## Feet to Inches

One foot equals 12 inches. Design a function named feetToInches that accepts a number of feet as an argument, and returns the number of inches in that many feet. Use the function in a program that prompts the user to enter a number of feet and then displays the number of inches in that many feet.

module Main()
    declare integer userFeet

    Display "Enter number of feet: "
    input userFeet

    Display "the number of inches: ", feetToInches(userFeet)

    Function integer feetToInches(integer feet)
        return feet * 12
    end function
end Module

## Math Quiz

Design a program that gives simple math quizzes. The program should display two random numbers that are to be added, such as:
```
  247
+ 129
```
The program should allow the student to enter the answer. If the answer is correct, a message of congratulations should be displayed. If the answer is incorrect, a message showing the correct answer should be displayed.

module main()
    declare rand1, rand2, userAnswer, randAnswer

    set rand1 = random(1, 300)
    set rand2 = random(1, 300)
    display "    ", rand1, "/n+  ", rand2
    input userAnswer
    randAnswer = rand1 + rand2

    if userAnswer == randAnswer then
        Display "congrats!"
    else
        Display "Correct answer is ", randAnswer
end module
    


## Maximum of Two Values

Design a function named max that accepts two integer values as arguments and returns the value that is the greater of the two. For example, if 7 and 12 are passed as arguments to the function, the function should return 12. Use the function in a program that prompts the user to enter two integer values. The program should display the value that is the greater of the two.

module main()
    declare integer number1, number2

    display "Enter 1st number: "
    input number1
    display "Enter 2nd number: "
    input number2
    display getMax(number1, number2), "is Bigger"

    function integer getMax(integer num1, integer num2)
        if num1 > num2 then
            return num1
        else if num2 > num1 then
            return num2
        else
            Display "The numbers are equal"
end module


## Falling Distance

When an object is falling because of gravity, the following formula can be used to determine the distance the object falls in a specific time period:

![image](https://user-images.githubusercontent.com/47218880/67446204-67cf7880-f5d5-11e9-9375-bbde7f1473b5.png)

d = 1/2 * g * t^2

The variables in the formula are as follows: d is the distance in meters, g is 9.8, and t is the amount of time, in seconds, that the object has been falling.

Design a function named fallingDistance that accepts an object’s falling time (in seconds) as an argument. The function should return the distance, in meters, that the object has fallen during that time interval. Design a program that calls the function in a loop that passes the values 1 through 10 as arguments and displays the return value.

module main()
    declare real value

    for value = 1 to 10 step 1
        display "if Time = ", value, " then Distace = ", fallingDistance(value)
    end for

    function real fallingDistance(real time)
        return .5 * 9.8 * time * time
    end function
end module

## Kinetic Energy

In physics, an object that is in motion is said to have kinetic energy. The following formula can be used to determine a moving object’s kinetic energy:

![image](https://user-images.githubusercontent.com/47218880/67446241-8fbedc00-f5d5-11e9-94c6-460160036f3f.png)

KE = .5 * mass * velocity * velocity

The variables in the formula are as follows: KE is the kinetic energy, m is the ­object’s mass in kilograms, and v is the object’s velocity, in meters per second.

Design a function named kineticEnergy that accepts an object’s mass (in ­kilograms) and velocity (in meters per second) as arguments. The function should return the amount of kinetic energy that the object has. Design a program that asks the user to enter values for mass and velocity, and then calls the kineticEnergy function to get the object’s kinetic energy.

module main()
    declare real userMass, userVelocity

    display "Enter mass (in ­kilograms): "
    input userMass
    display "Enter velocity (in meters per second): "
    input userVelocity

    Display "This is the Kinetic Energy: ", kineticEnergy(userMass, userVelocity)

    function real kineticEnergy(mass, velocity)
        return .5 * mass * velocity * velocity
end module

## Odd/Even Counter

In this chapter you saw an example of how to design an algorithm that determines whether a number is even or odd. Design a program that generates 100 random numbers, and keeps a count of how many of those random numbers are even and how many are odd.

module main()
    declare integer number, even, odd

    for 1 to 100 step 1
        number = random(1, 10)
        if number % 2 = 0 then
            even +=1
        else 
            odd += 1

    display "There were ", odd, " odd numbers, and ", even, " even numbers."
end module

## Guess the Number

Design a number guessing game program. The program should generate a random number and then ask the user to guess the number. Each time the user enters his or her guess, the program should indicate whether it was too high or too low. The game is over when the user correctly guesses the number. When the game ends, the program should display the number of guesses that the user made.

module main()
    declare integer number, guess, count

    number = random (1, 20)

    Do 
        Display "Enter Guess: "
        input guess
        count += 1
        if guess > number then
            Display "Too High!"
        else if guess < number then
            Display "Too Low!"
        else
            Display "Correct! That took ", count, " guesses."
        end if
    until guess == number
end module

## Prime Numbers

A prime number is a number that is only evenly divisible by itself and 1. For example, the number 5 is prime because it can only be evenly divided by 1 and 5. The number 6, however, is not prime because it can be divided evenly by 1, 2, 3, and 6.

Design a Boolean function named isPrime, which takes an integer as an argument and returns True if the argument is a prime number, or False otherwise. Use the function in a program that prompts the user to enter a number and then displays a message indicating whether the number is prime.

module main()
    declare integer number

    Display "Enter an integer: "
    input integer
    
    if isPrime(number) == True then 
        Display "That's a prime!"
    else if prime == False then
        Display "That's not a prime
    else 
        Display "Error"
    end if

    function Boolean isPrime(integer num)
        declare boolean prime
        for count = 2 to (num-1) step 1
            if num % count == 0 then
                set prime = False 
                break
            else
                set prime = True
            end
        end for
    return prime
        
end module

 ### TIP:
Recall that the MOD operator divides one number by another and returns the remainder of the division. In an expression such as num1 MOD num2, the MOD operator will return 0 if num1 is evenly divisible by num2.

## Prime Number List

This exercise assumes you have already designed the isPrime function in Programming Exercise 10. Design another program that displays all of the prime numbers from 1 through 100. The program should have a loop that calls the isPrime function.

module main()
    declare interger count

    Display "Here are all the prime numbers (1-100): "

    for count = 1 to 100 step 1
        if isPrime(count) == True then
            Display count
        end if
        
    function Boolean isPrime(integer num)
        declare boolean prime
        for count = 2 to (num-1) step 1
            if num % count == 0 then
                set prime = False 
                break
            else
                set prime = True
            end
        end for
    return prime

## Rock, Paper, Scissors Game

Design a program that lets the user play the game of Rock, Paper, Scissors against the computer. The program should work as follows:
```
When the program begins, a random number in the range of 1 through 3 is generated. If the number is 1, then the computer has chosen rock. If the number is 2, then the computer has chosen paper. If the number is 3, then the computer has chosen scissors. (Don’t display the computer’s choice yet.)

The user enters his or her choice of “rock,” “paper,” or “scissors” at the keyboard.

The computer’s choice is displayed.

The program should display a message indicating whether the user or the computer was the winner. A winner is selected according to the following rules:

If one player chooses rock and the other player chooses scissors, then rock wins. (The rock smashes the scissors.)

If one player chooses scissors and the other player chooses paper, then scissors wins. (Scissors cut paper.)

If one player chooses paper and the other player chooses rock, then paper wins. (Paper wraps rock.)

If both players make the same choice, the game must be played again to determine the winner.
```


declare string doAgain = 'n'

module main()

    declare integer computerNum, userNum
    declare string userString

    do 
        set computerNum = random(1, 3)
        display "Enter 'rock', 'paper' or 'scissors': "
        input userString
        set userNum = getWordsToNum(userString)
        display "Computers choice was ", getNumToWords(computerNum)
        
        if computerNum == 1 AND userNum == 3 then
            Display "The computer won!"
        else if computerNum == 3 AND userNum == 1 then
            Display "The user won!"
        else if computerNum == 2 AND userNum == 1 then
            Display "The computer won!"
        else if computerNum == 1 AND userNum == 2 then
            Display "The user won!"
        else if computerNum == 3 AND userNum == 2 then
            Display "The computer won!"
        else if computerNum == 2 AND userNum == 3 then
            Display "The user won!"
        else
            Display "both players make the same choice, the game must be played again"
            set doAgain = "y"
    until doAgain == "y"

    function integer getWordsToNum(string str)
        declare integer num
        if str == "rock" then
            set num = 1
        else if str == "paper" then
            set num = 2
        else if str =="scissors" then
            set num = 3
        else
            Display "Error invalid entry, try again!"
            set doAgain = "y"
    return num

    function string getNumToWords(integer num)
        declare string str
        if num ==1 then
            set str = "rock"
        else if num ==2 then
            set str = "paper"
        else if num == 3 then
            set str = "scissors"
        else
            Display "Error invalid entry, try again!"
            set doAgain = "y"
    return str
end module





## Slot Machine Simulation

A slot machine is a gambling device that the user inserts money into and then pulls a lever (or presses a button). The slot machine then displays a set of random images. If two or more of the images match, the user wins an amount of money, which the slot machine dispenses back to the user.

Design a program that simulates a slot machine. When the program runs, it should do the following:
```
Ask the user to enter the amount of money he or she wants to insert into the slot machine.

Instead of displaying images, the program will randomly select a word from the following list:

Cherries, Oranges, Plums, Bells, Melons, Bars

The program will select and display a word from this list three times.

If none of the randomly selected words match, the program will inform the user that he or she has won $0. If two of the words match, the program will inform the user that he or she has won two times the amount entered. If three of the words match, the program will inform the user that he or she has won three times the amount entered.

The program will ask whether the user wants to play again. If so, these steps are repeated. If not, the program displays the total amount of money entered into the slot machine and the total amount won.
```
## ESP Game

Design a program that tests your ESP, or extrasensory perception. The program will randomly pick a color, and you will be asked to predict the program’s selection before it is revealed. Design the program to randomly select one of the following words:
```
Red, Green, Blue, Orange, Yellow
```
To select a word, the program can generate a random number. For example, if the number is 0, the selected word is Red, if the number is 1, the selected word is Green, and so forth.

Next, the program should ask the user to enter the color that the computer has selected. After the user has entered his or her guess, the program should display the name of the randomly selected color. The program should repeat this 10 times and then display the number of times the user correctly guessed the selected color.
