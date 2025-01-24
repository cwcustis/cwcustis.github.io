## Guessing Game

```mermaid
flowchart TD
A[Start] --> |Program generates a random number between 1 and 10|B[User Input]
B --> |User enters a number|C{Determination}
C --> |User guessed the right number|D[Win!]
C --> |User entered a number beyond the range|J[Choose between 1 and 10!]
J --> F
C --> |User guessed a lower number|E[Too Low!]
E --> F[Guess again...]
C --> |User Guessed a higher number|H[Too High!]
H --> F
F --> |Game loops back to User Input|B
```

### Explanation
The game works by generating a random number (1-10) and comparing user input to the number.  
>* In cases where the user guesses correctly, the game simply outputs "Win!" and ends.  
>* In cases where the user guesses incorrectly, there are three possibilities.
>    * The user's number was beyond the range of the game
>    * The user's number was lower than the correct number
>    * The user's number was higher than the correct number
 
Regardless of the circumstances, in the case of an incorrect guess, the game loops back to the user guessing until victory.