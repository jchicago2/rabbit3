# rabbit3
import random

def display_rabbits():
    print("\nHere are the rabbits:")
    print("1: 🐰  2: 🐰  3: 🐰  4: 🐰\n")

def play_game():
    print("Welcome to the Rabbit Guessing Game!")
    print("One of the rabbits has a gold cup behind it. Can you guess which one?")
    
    rabbits = ['🐰', '🐰', '🐰', '🐰']
    cup_position = random.randint(0, 3)  # Randomly place the cup behind one rabbit

    # Display rabbits to the player
    display_rabbits()

    # Ask the player for a guess
    guess = int(input("Choose a rabbit (1, 2, 3, or 4): ")) - 1

    # Check if the player guessed correctly
    if guess == cup_position:
        print("\nCongratulations! You found the gold cup! 🏆")
    else:
        print(f"\nSorry, no gold cup behind rabbit {guess + 1}. The cup was behind rabbit {cup_position + 1}.")
    
    # Ask if they want to play again
    play_again = input("Do you want to play again? (yes/no): ").lower()
    if play_again == 'yes':
        play_game()
    else:
        print("Thanks for playing! Goodbye!")

# Start the game
play_game()
