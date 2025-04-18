<!DOCTYPE html>
<html>
<body>
<h1>Hello World</h1>
<p>I'm hosted with GitHub Pages.</p>
</body>
</html>

## test

import random

## Randomizing the number that is being guessed
number = random.randint(1, 100)

print("A random number has been chosen 1-100. Try to figure out what it is in as few guesses as possible")
print("Choose a number and I will tell you whether my number is higher or lower than your guess.")

## Guessing the number 
def get_user_choice():
    while True:
        try:
            user_choice = int(input("Guess here: "))
            if user_choice > 100 or user_choice < 1:
                raise ValueError("Number must be between 1 and 100")

            if user_choice == number:
                print("Congrats, you got it right!")
                break
            elif user_choice > number:
                print(f"My number is lower than {user_choice}.")
                print("Try again.")
            elif user_choice < number:
                print(f"My number is above {user_choice}.")
                print("Try again.")
        except ValueError as e:
            print(f"Error: {e}")

get_user_choice()
