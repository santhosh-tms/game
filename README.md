import random

def play_game():
    print("Welcome to Rock Paper Scissors!")
    print("Please choose one of the following options:")
    print("1. Rock")
    print("2. Paper")
    print("3. Scissors")
    
    user_choice = int(input("Enter your choice (1-3): "))
    
    while user_choice < 1 or user_choice > 3:
        print("Invalid choice. Please try again.")
        user_choice = int(input("Enter your choice (1-3): "))
    
    if user_choice == 1:
        user_choice_name = "Rock"
    elif user_choice == 2:
        user_choice_name = "Paper"
    else:
        user_choice_name = "Scissors"
    
    print("You chose:", user_choice_name)
    
    computer_choice = random.randint(1, 3)
    
    if computer_choice == 1:
        computer_choice_name = "Rock"
    elif computer_choice == 2:
        computer_choice_name = "Paper"
    else:
        computer_choice_name = "Scissors"
    
    print("Computer chose:", computer_choice_name)
    
    if user_choice == computer_choice:
        print("It's a tie!")
    elif (user_choice == 1 and computer_choice == 3) or (user_choice == 2 and computer_choice == 1) or (user_choice == 3 and computer_choice == 2):
        print("Congratulations! You win!")
    else:
        print("Sorry, you lose!")
    
    play_again = input("Do you want to play again? (yes/no): ")
    
    if play_again.lower() == "yes":
        play_game()
    else:
        print("Thank you for playing!")

play_game()
