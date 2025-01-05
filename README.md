Hangman Game Implementation
Overview
This project involves implementing a classic word game called Hangman. The game allows a user to guess letters to reveal a secret word selected by the computer.

Getting Started
Download Files:
Download hangman.py and words.txt and save them in the same directory.
Run hangman.py to check if everything is set up correctly. 

You should see:
Loading word list from file...
55900 words loaded.

Initial Setup:
Ensure both files are in the correct directory to avoid errors.

Game Requirements
Word Selection: The computer selects a random word from words.txt, which contains only lowercase words.
Guesses: Players start with 6 guesses.
Gameplay:
The user guesses one letter at a time.
Correct guesses reveal letters in the word; incorrect guesses reduce remaining guesses.
The game ends if the word is guessed or if guesses are exhausted.

Helper Functions
Before implementing the main game, three helper functions are provided:
is_word_guessed(secret_word, letters_guessed): Checks if all letters in secret_word have been guessed.
Example: is_word_guessed('apple', ['e', 'i', 'k', 'p', 'r', 's']) returns False.
get_guessed_word(secret_word, letters_guessed): Returns the word with guessed letters filled in, others as underscores (_ ).
Example: get_guessed_word('apple', ['e', 'i', 'k', 'p', 'r', 's']) returns '_ pp_ e'.
get_available_letters(letters_guessed): Provides a string of all unguessed letters in alphabetical order.
Example: get_available_letters(['e', 'i', 'k', 'p', 'r', 's']) returns 'abcdfghjlmnoqtuvwxyz'.

Game Implementation
hangman(secret_word):
Initially, set the secret_word manually for testing. Later, let the computer choose randomly.
Game flow includes:
Displaying number of letters, guesses, and available letters before each guess.
Handling user input for guesses, with considerations for warnings (3 initial warnings):
Invalid inputs (non-alphabet characters) or repeated guesses decrease warnings or guesses.
Vowels guessed incorrectly cost 2 guesses, consonants 1 guess.
Game termination:
If the word is guessed, congratulate the player and show the score (guesses remaining * unique letters in word).
If guesses are exhausted, reveal the word and announce loss.

Additional Notes
User-Friendliness: Focus on usability by providing clear feedback and using underscores for unknown letters.
Error Handling: Use warnings for invalid inputs to enhance gameplay experience.

Example Game Flow
See the provided examples in the problem statement for expected game output.




