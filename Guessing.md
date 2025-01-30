```mermaid
flowchart TD
Start([Start]) -->     A[Ask user if he wants to play a random number guessing game] -->|if user types yes| B(Generate random number from 1 - 20 and put the number on a variable called generated_number)
    A --> |If user types no| C(Reload the page to play the game)
    B --> D(Ask user to input a number from 1 - 20)
    D --> |if user guess > 20| E(The guess is out of range, reload the page to try again!)
    D --> |If user guess is a letter or a special digit| F(You need to type a number, reload the page to try again)
    D --> |if user guess < 0| E(The guess is out of range, reload the page to try again!)
    D --> |if user guess is in bounds but lower than generated_number| G(You guessed too low, try again!)
    D --> |if user guess is in bounds but higher than generated_number| H(You guessed too high, try again!)
    D --> |if user guess==generated_number| I(Congrats!, you guessed the number right)
    I --> J(If you wanna play again just reload the page)
End([End])
```
Description of process:
The user opens the page and get asked for input to see if he wants to play,
if the user says no the program ends but if he says yes then the program generates a random number from 1 - 20,
then the program asks the user to type a number from 1 - 20,
if the user types a number thats outside of bounds a message pops up telling him that the number is out of bounds and to try again,
if the user types a letter or a specia digit the program tells the user to type a number and to try again,
if the user guess meets all the requirements but its lower than the number generated the program tells him that his guess was too low,
if the user guess meets all the requirements but its higher than the number generated the program tells him that his guess was too high,
if the guess was correct the program sends out a message congratulating the user and telling him to reload the page if he wanted to play the game again.
