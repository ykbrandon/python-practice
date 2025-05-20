# Number Guessing Game

A simple Python CLI game where the player guesses a random number between 1 and 10.

## Features
- Random number generation
- Input validation (handles non-integer inputs and out-of-range numbers)
- Hints ("Too high/Too low")
- Clean, structured code

## Code Preview

```python
import random

def main():
    number = random.randint(1, 10)
    
    while True:
        try:
            guess = int(input("Guess a number between 1 and 10: "))
            if guess < 1 or guess > 10:
                print("Please enter a number between 1 and 10")
                continue
            
            if guess < number:
                print("Too low! Try again.")
            elif guess > number:
                print("Too high! Try again.")
            else:
                print("Correct! You guessed the number.")
                break
                
        except ValueError:
            print("Please enter a valid integer.")

if __name__ == "__main__":
    main()
