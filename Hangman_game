

import random
# import turtle

from hangman_words import word_list
from hangman_art import logo, stages

print(logo)
game_is_finished = False
lives = len(stages)-1

chosen_word = random.choice(word_list).lower()
word_length = len(chosen_word)

display = []
for i in range(len(chosen_word)):
    display.append("_")

while not game_is_finished:
    guess_letter = input("Enter a random letter:").lower()

    # turtle.clear()

    if guess_letter in display:
        print(f"You've already guessed {guess_letter}")

    for position in range(word_length):
        letter = chosen_word[position]
        if letter == guess_letter:
            display[position] = guess_letter
    print(f"{' '.join(display)}")

    if not guess_letter in chosen_word:
        print(f"You guessed {guess_letter}, that is not in the word \nYou lose 1 life.")
        lives -= 1
        if lives == 0:
            game_is_finished = True
            print("You lose the game")
            print(f"The word is {chosen_word}")
        print(stages[lives])
    if not"_" in display:
        game_is_finished = True
        print("You Win")
