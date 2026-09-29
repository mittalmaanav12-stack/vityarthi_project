# Random Password Generator

A simple command-line Python script that generates a random password of a chosen minimum length. You can choose whether the password must include numbers and/or special characters.

## Features

- Set a minimum password length
- Optionally require at least one digit
- Optionally require at least one special character
- Always includes upper- and lowercase letters in the character pool
- Guarantees the password meets your selected criteria before returning it

## Usage

1. Save the script as `password_generator.py`.
2. Run it from a terminal:

   ```bash
   python password_generator.py
   ```

3. Answer the prompts:

   ```
   Enter the minimum length : 12
   do you want to have numbers(y/n)?y
   do you want to have special characters(y/n)?y
   the generated password is : kT#9aQ!x2$mLpW
   ```

## How It Works

1. **Build the character pool.** Starts with all letters (`a-z`, `A-Z`). Digits (`0-9`) and punctuation (`!"#$%&'()*+,-./:;<=>?@[\]^_`{|}~`) are added depending on your choices.
2. **Generate characters.** A loop picks random characters from the pool and appends them to the password.
3. **Track requirements.** Flags (`has_number`, `has_special`) record whether a digit or special character has appeared.
4. **Stop when satisfied.** The loop ends only when the password is at least `min_length` characters long **and** all selected requirements are met.
