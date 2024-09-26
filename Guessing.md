'''mermaid
flowchart TD
Start([Start]) --> Generate-Random-Number 
Generate-Random-Number[Generate Random Number]
Genereate-Random-Number --> PromptUserIntput[Prompt User for guess]
PromptUserInput --> ValidateInput{Is Input Valid?}
ValidateInput -->|Yes| CheckGuess[check User Guess]







End([End])
'''
