import random

def number_guessing_game():
    print("Welcome to the Number Guessing Game!")
    
    # Define the range of numbers
    lower_bound = int(input("Enter the lower bound of the range: "))
    upper_bound = int(input("Enter the upper bound of the range: "))
    
    # Randomly select a number within the range
    secret_number = random.randint(lower_bound, upper_bound)
    
    print(f"Guess the number between {lower_bound} and {upper_bound}.")
    
    # Initialize the number of attempts
    attempts = 0
    
    while True:
        # Increment the attempt count
        attempts += 1
        
        # Take the user's guess
        guess = int(input("Enter your guess: "))
        
        # Provide feedback on the guess
        if guess < secret_number:
            print("Too low! Try again.")
        elif guess > secret_number:
            print("Too high! Try again.")
        else:
            print(f"Congratulations! You guessed the number in {attempts} attempts.")
            break
    
    print("Thank you for playing the Number Guessing Game!")

if __name__ == "__main__":
    number_guessing_game()
