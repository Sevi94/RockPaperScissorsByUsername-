# RockPaperScissorsByUsername-
import random

rock = "Rock"
paper = "Paper"
scissors = "Scissors"


print("Choose your move: 'r' for Rock, 'p' for Paper, 's' for Scissors")
player_input = input("Your choice: ")


if player_input == "r":
    player_move = rock
elif player_input == "p":
    player_move = paper
elif player_input == "s":
    player_move = scissors
else:
    print("Invalid input! Please choose 'r', 'p', or 's'.")
    raise SystemExit


computer_choice = random.randint(0, 2)
if computer_choice == 0:
    computer_move = rock
elif computer_choice == 1:
    computer_move = paper
else:
    computer_move = scissors


print(f"The computer chose {computer_move}.")


if player_move == computer_move:
    print("It's a tie!")
elif (player_move == rock and computer_move == scissors) or \
     (player_move == paper and computer_move == rock) or \
     (player_move == scissors and computer_move == paper):
    print("You win!")
else:
    print("You lose!")
