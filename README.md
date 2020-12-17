# Wheel of Python
The final project for the course __[Python Class and Inheritance](https://www.coursera.org/learn/python-classes-inheritance)__ .The course is offered by University of Michigan on Coursera     
    
This project will take you through the process of implementing a simplified version of the game Wheel of Fortune. Here are the rules of our game:  
- **There are `num_human` human players and `num_computer` computer players.**
     - Every player has some amount of money ($0 at the start of the game)   
     - Every player has a set of prizes (none at the start of the game)   
- **The goal is to guess a phrase within a category. For example:**   
     - Category: **Artist & Song**
     - Phrase: **Whitney Houston’s I Will Always Love You**   
- **Players see the category and an obscured version of the phrase where every alphanumeric character in the phrase starts out as hidden (using underscores: `_`):**   
     - Category: **Artist & Song**
     - Phrase: `______ ______'_ _ ____ ______ ____ ___`   
- Note that case (capitalization) does not matter   

   
- **During their turn, every player spins the wheel to determine a prize amount and:**   
     
     - **If the wheel lands on a cash square, players may do one of three actions:**  
         
         - **Guess any letter that hasn’t been guessed by typing a letter (a-z)**  
             - Vowels (a, e, i, o, u) cost $250 to guess and can’t be guessed if the player doesn’t have enough money.
               All other letters are “free” to guess
             - The player can guess any letter that hasn’t been guessed and gets that cash
               amount for every time that letter appears in the phrase









