'''mermaid
flowchart TD
    Start([Start]) --> GenerateRandomNumber
    GenerateRandomNumber[Generate Random Number]
    GenerateRandomNumber --> PromptUserInput[Prompt User for Guess]
    PromptUserInput --> ValidateInput{Is Input Valid?}
    
    ValidateInput -->|Yes| CheckGuess[Check User Guess]
    ValidateInput -->|No| InvalidInput[Display Invalid Input Message]
    
    InvalidInput --> PromptUserInput
    
    CheckGuess -->|Correct| CorrectGuess[Display Correct Guess Message]
    CheckGuess -->|Too High| TooHigh[Display Too High Message]
    CheckGuess -->|Too Low| TooLow[Display Too Low Message]

    CorrectGuess --> PlayAgain{Play Again?}
    TooHigh --> PlayAgain
    TooLow --> PlayAgain
    
    PlayAgain -->|Yes| GenerateRandomNumber
    PlayAgain -->|No| 
    End([End])
'''



#  Description 
## 1. Start: 
      The game begins when the user initiates it.

## 2. Generate Random Number: 
      The program generates a random number within the specified range.

## 3. Prompt User for Guess: 
      The user is prompted to enter their guess.

## 4. Validate Input: 
      The input provided by the user is validated to check if it's numeric and within the acceptable range.

     - If Yes: The game proceeds to check the user’s guess.
     - If No: An error message is displayed, indicating that the input is invalid. The user is prompted to enter their guess again.
## 5. Check User Guess: The program compares the user’s guess to the generated random number.

     - If Correct: A message is displayed confirming the guess is correct, and the user is prompted to play again.
     - If Too High: A message is displayed indicating the guess is too high, and the user is prompted to guess again.
     - If Too Low: A message is displayed indicating the guess is too low, and the user is prompted to guess again.

## 6. Play Again?: The user is asked if they would like to play again.

     - If Yes: The program returns to the random number generation step.
     - If No: The game ends.
    
