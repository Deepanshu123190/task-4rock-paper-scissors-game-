import random

def rock_paper_scissors():
    print("Welcome to Rock-Paper-Scissors!")
    print("Choices:")
    print("1. Rock")
    print("2. Paper")
    print("3. Scissors")

    # Get user's choice
    user_choice = input("Enter your choice (Rock/Paper/Scissors): ").strip().lower()

    # Validate user's choice
    if user_choice not in ["rock", "paper", "scissors"]:
        print("Invalid choice. Please select Rock, Paper, or Scissors.")
        return

    # Random choice for the computer
    choices = ["rock", "paper", "scissors"]
    computer_choice = random.choice(choices)

    print(f"You chose: {user_choice.capitalize()}")
    print(f"Computer chose: {computer_choice.capitalize()}")

    # Determine the winner
    if user_choice == computer_choice:
        print("It's a tie!")
    elif (user_choice == "rock" and computer_choice == "scissors") or \
         (user_choice == "paper" and computer_choice == "rock") or \
         (user_choice == "scissors" and computer_choice == "paper"):
        print("You win!")
    else:
        print("You lose!")

# Run the game
rock_paper_scissors()
