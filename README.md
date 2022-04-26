# Hangman_game

# Milestone 1
In this milestone, the ask_letter() function was implemented, which will ask the user for a letter. The flow chart is as follows:
![This is an image](https://github.com/Kevin-MrYe/Hangman_game/blob/main/images/ask_letter.png)

# Milestone 2
In this milestone, the attributes were added to the __init__ method. Then the ask_letter() function was updated to whether the typed letter has been tried already.

1.**word**: The word to be guessed picked randomly from the word_list

2.**word_guessed**: A list of the letters of the word, with '\_' for each letter not yet guessed

3.**num_letters**: The number of UNIQUE letters in the word that have not been guessed yet

4.**num_lives**: The number of lives the player has

5.**list_letters**: A list of the letters that have already been tried

The flow chart is as follows:
![This is an image](https://github.com/Kevin-MrYe/Hangman_game/blob/main/images/ask_letter%20updated.png)

# Milestone 3
In this milestone, the check_letter() function was implemented, which will check if the letter is in the word. If it is, it replaces the '\_' in the word_gressed list with the letter. If it is not, it reduces the number of lives by 1.

1. Using the **if letter in word:** to check if the letter is in word.
2. Using the following code to replace the '\_' in the word_gressed list with the letter

```python
for i in range(0,len(self.word)):
     if self.word[i] == lower_letter:
         self.word_gessed[i] = lower_letter
```

The flow chart is as follows:
![This is an image](https://github.com/Kevin-MrYe/Hangman_game/blob/main/images/check_letter.png)


# Milestone 4
In this milestone, ask the user to enter a letter until the user guesses the word. In addition, whenever the user lose a life, an additional part of hangman will be visualised. A list name show_status will store the visualizations which correspond to num_lives. The core code is as follows:

```python
game = Hangman(word_list, num_lives=6)
    while True:
        game.ask_letter()
        if '_' not in game.word_gessed:
            print("Congratulation! You won!")
            exit()
        elif game.num_lives == 0:
            print(f"You lost! The word was {game.word}")
```


