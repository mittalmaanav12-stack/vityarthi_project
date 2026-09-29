# Python Password Generator

A lightweight, interactive command-line password generator written in Python. This tool generates secure, randomized passwords based on user-defined length and character set criteria (digits and special characters).

---

## Features

- **Custom Length:** Define the minimum number of characters required for your password.
- **Configurable Criteria:** Option to include or exclude numbers (`0-9`) and special characters/punctuation symbols (`!@#$%^&*...`).
- **Guaranteed Criteria Matching:** Ensures that generated passwords strictly contain requested character types (numbers, special characters) before returning the result.
- **Pure Standard Library:** No external dependencies required.

---

## Requirements

- Python 3.6 or higher

---

## Installation & Setup

1. **Clone the repository** (or download the script directly):
   ```bash
   git clone https://github.com/your-username/password-generator.git
   cd password-generator
   ```

2. **Save the script** as `password_generator.py` (if creating manually).

---

## How to Run

Execute the script from your terminal or command prompt:

```bash
python password_generator.py
```

### Example Usage

```text
Enter the minimum length : 12
do you want to have numbers(y/n)? y
do you want to have special characters(y/n)? y
the generated password is : k9#mP2$xL1!q
```

---

## Code Overview

- **`generate_password(min_length, number=True, special_characters=True)`**:
  - Dynamically builds the pool of available characters using Python's `string` module (`ascii_letters`, `digits`, and `punctuation`).
  - Iteratively picks characters at random using `random.choice()`.
  - Validates that the output meets both the length threshold and all active criteria flags.

---

## Security Note

This script uses Python's built-in `random` module, which is suitable for standard, general-purpose passwords. For cryptographically secure passwords used in production-grade authentication systems, consider swapping `random` with the [`secrets`](https://docs.python.org/3/library/secrets.html) module (`secrets.choice()`).

---

## License

This project is open-source and available under the [MIT License](LICENSE).
