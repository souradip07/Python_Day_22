# Python_Day_22
#Example Scenario Function
def forest_adventure():
    print("You are in a dark forest. You can go left or right.")
    choice = input("Enter 'left' or 'right': ").lower()
    if choice == "left":
        print("You encounter a friendly elf who guides you out of the forest.")
        return True  # Game ends
    elif choice == "right":
        print("You stumble into a pit and can't find your way out.")
        return False  # Game ends
    else:
        print("Invalid choice. Try again.")
        return forest_adventure()


        #Main Game Loop
def start_game():
    print("Welcome to the Text-Based Adventure Game!")
    outcome = forest_adventure()
    if outcome:
        print("Congratulations, you won the game!")
    else:
        print("Game over. Better luck next time!")

if __name__ == "__main__":
    start_game()
