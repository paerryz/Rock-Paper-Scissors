# Rock-Paper-Scissors

import random
rock = '''
    _______
---'   ____)
      (_____)
      (_____)
      (____)
---.__(___)
'''

paper = '''
    _______
---'   ____)____
          ______)
          _______)
         _______)
---.__________)
'''

scissors = '''
    _______
---'   ____)____
          ______)
       __________)
      (____)
---.__(___)
'''
---------------------------------------------------------------------------------------------------------
#Code below 👇
game_images = [rock, paper, scissors]
user_choice = int(input("What is your choice? Type 0 for Rock, 1 for Paper, and 2 for Scissors.\n"))

if user_choice > 2 or user_choice < 0:
    print("You typed an invalid number. Please Try again.")
else:
    print(game_images[user_choice])

    computer_choice = random.randint(0, 2)
    print(f"Computer choice: {computer_choice}.")
    print(game_images[computer_choice])

    if user_choice == 0 and computer_choice == 2:
        print("You WIN")
    elif user_choice == 2 and computer_choice == 0:
        print("You LOSE")
    elif user_choice > computer_choice:
        print("You Win!")
    elif user_choice < computer_choice:
        print("You Lose!")
    elif user_choice == computer_choice:
        print("It's a draw.")
