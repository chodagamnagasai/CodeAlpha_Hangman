import random

# Expanded list of predefined words
WORDS = [
    'apple', 'bread', 'chair', 'house', 'plant',
    'cloud', 'river', 'mountain', 'school', 'guitar',
    'python', 'window', 'bottle', 'garden', 'island',
    'rocket', 'planet', 'jungle', 'forest', 'castle',
    'machine','sky','speed','vision','university',
    'moon','cup','bed','shoe','ball',
    'lighthouse','raccoon','thermometer','asteroid','hyposis',
    'circumference','perpendicular','noodle','giraffe','pickle',
    'jellyfish','whisper','candy','android','castle',
    
    'dinosaur','elephant','watermelon'
]

# Select a random word
word_to_guess = random.choice(WORDS)
guessed_letters = set()
correct_letters = set(word_to_guess)
max_attempts = 6
attempts = 0

print("Welcome to Hangman!")

while attempts < max_attempts:
    print("\n" + "-" * 30)
    print(f"Incorrect guesses left: {max_attempts - attempts}")
    print(f"Guessed letters: {' '.join(sorted(guessed_letters)) if guessed_letters else 'None'}")

    # Display current state of the word
    display_word = [letter if letter in guessed_letters else '_' for letter in word_to_guess]
    print('Current word:', ' '.join(display_word))

    # Get user input
    guess = input("Guess a letter: ").lower()

    # Input validation
    if not guess.isalpha() or len(guess) != 1:
        print("Invalid input. Please enter a single alphabet letter.")
        continue

    if guess in guessed_letters:
        print("You already guessed that letter. Try again.")
        continue

    guessed_letters.add(guess)

    if guess in correct_letters:
        print(f"Good guess! '{guess}' is in the word.")
        if correct_letters.issubset(guessed_letters):
            print(f"\nCongratulations! You guessed the word: {word_to_guess}")
            break
    else:
        attempts += 1
        print(f"Sorry, '{guess}' is not in the word.")

else:
    print(f"\nGame over! You've used all attempts. The word was: {word_to_guess}")
