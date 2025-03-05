# first_project
import random

possible_actions = ["rock", "paper", "scissors"]


def check_win(player, computer):

  if player == computer:
    return (f"Both players selected {player} It's a tie!")
  elif player == "rock":
    if computer == "scissors":
      return "Rock smashes scissors! You win!"
    else:
      return "Paper covers rock. You lose."
  elif player == "paper":
    if computer == "rock":
      return "Paper covers rock, you win!"
    else :
      return "Scissors cuts paper! You lose!"
  elif player == "scissors":
    if computer == "paper":
      return "Scissors cuts paper! You win!"
    else :
      return "Rock crushes scissors! You lose!"

def should_play_again(play_again):
    while True:
        play_again_lower = play_again.lower()

        if play_again_lower in {"y", "yes"}:
            return True
        elif play_again_lower in {"n", "no"}:
            print ("Thank you for playing! Goodbye!")
            return False     
        else:
            print(f"{play_again} is an invalid response")
            continue

wants_to_play = True 
while wants_to_play is True:
  
  player = input("Enter a choice(rock, paper, scissors):")
  computer = random.choice (possible_actions)
  if player in possible_actions:
      print (f"You chose {player}, Computer chose {computer}.")
      print(check_win(player, computer))           
  else: 
      print (f"{player} is an invalid input")
      continue
  play_again = input("Would you like to play again Y/N: ")
  wants_to_play = should_play_again(play_again)    

    
    
    
    
      
