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
             - If there is a prize, the user also gets that prize (in addition to any prizes they already had)  
             - If the letter does appear in the phrase, the user keeps their turn. Otherwise, it’s the next player’s turn  
             - **Example: The user lands on $500 and guesses ‘W’**  
                 - Example: The user lands on $500 and guesses ‘W’  
         - **Guess the complete phrase by typing a phrase (anything over one character that isn’t ‘pass’)**  
             - If they are correct, they win the game  
             - If they are incorrect, it is the next player’s turn  
         - **Pass** their turn by entering `'pass'`  
         
     - If the wheel lands on **“lose a turn”**, the player loses their turn and the game moves on to the next player  
     - If the wheel lands on **“bankrupt”**, the player loses their turn and loses their money but they keep all of the prizes they have won so far.  
     
- The game continues until the entire phrase is revealed (or one player guesses the complete phrase)

   
 ## User defined class 
 
 #### WOFPlayer
 Every instance of `WOFPlayer` has three instance variables:  
   - `.name` : The name of the player (should be passed into the constructor)
   - `.prizeMoney` : The amount of prize money for this player (an integer, initialized to 0)
   - `.prizes` : The prizes this player has won so far (a list, initialized to [])  
 Of these instance variables, only `name` should be passed into the constructor.

It should also have the following methods (note: we will exclude `self` in our descriptions):  
  - `.addMoney(amt)` : Add amt to self.prizeMoney
  - `.goBankrupt()` : Set self.prizeMoney to 0
  - `.addPrize(prize)` : Append prize to self.prizes
  - `.__str__()` : **Returns the player’s name and prize money in the following format:**
    - `Steve ($1800)` (for a player with instance variables `.name == 'Steve'` and `prizeMoney == 1800`)
    
 #### WOFHumanPlayer  
 
 This class is going to represent a human player.`WOFHumanPlayer` should inherit from `WOFPlayer`.
 In addition to having all of the instance variables and methods that `WOFPlayer` has, `WOFHumanPlayer`
 should have an additional method:
   - `.getMove(category, obscuredPhrase, guessed)` : Should ask the user to enter a move (using input())
      and **return whatever string they entered**.  
`.getMove()`’s prompt should be:
     
<div class = "alert alert-block alert-warning">
    {name} has ${prizeMoney}  

   Category: {category}  
   Phrase:  {obscured_phrase}  
   Guessed: {guessed}  
  
   Guess a letter, phrase, or type 'exit' or 'pass':  
   </div>








         













