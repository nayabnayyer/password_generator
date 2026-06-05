# 🔐 Password Generator

A lightweight, no-nonsense password generator built with Python and Streamlit. Enter a length, click a button, get a strong password. That's it.

![Python](https://img.shields.io/badge/Python-3.7+-blue?style=flat-square&logo=python&logoColor=white)
![Streamlit](https://img.shields.io/badge/Streamlit-1.0+-red?style=flat-square&logo=streamlit&logoColor=white)
![License](https://img.shields.io/badge/License-MIT-green?style=flat-square)

---

## ✨ What It Does

- Generates a random password of any length (1–100 characters)
- Pulls from the full character pool: **uppercase**, **lowercase**, **digits**, and **symbols**
- Runs in your browser via a clean Streamlit interface
- Zero dependencies beyond Python's built-in `random` and `string` modules

---

## 🚀 Getting Started

### Prerequisites

- Python 3.7+
- pip

### Installation

```bash
# Clone the repo
git clone https://github.com/your-username/password-generator.git
cd password-generator

# Install Streamlit
pip install streamlit

# Run the app
streamlit run password_generator.py
```

Then open your browser at `http://localhost:8501` — and you're good to go.

---

## 🖥️ Usage

1. Enter your desired password length using the number input (min: 1, max: 100)
2. Click **Generate**
3. Copy your new password

That's the whole flow.

---

## 🧠 How It Works

```python
import random
import string

def generate_password(length):
    characters = string.ascii_letters + string.digits + string.punctuation
    return ''.join(random.choice(characters) for i in range(length))
```

The character pool includes:
| Type       | Example         |
|------------|-----------------|
| Lowercase  | `a b c ... z`   |
| Uppercase  | `A B C ... Z`   |
| Digits     | `0 1 2 ... 9`   |
| Symbols    | `! @ # $ % ...` |

Each character is chosen independently at random, giving you a password that's unpredictable and hard to crack.

---

## 📁 Project Structure

```
password-generator/
│
├── password_generator.py   # Main app file
└── README.md               # You're reading this
```

---

## 🔭 Future Ideas

- Copy-to-clipboard button
- Toggles to include/exclude symbols, digits, etc.
- Password strength indicator
- Generate multiple passwords at once

---

## 👩‍💻 Author

**Nayab Nayyer**
[GitHub](https://github.com/your-username) · [LinkedIn](https://linkedin.com/in/your-profile)

---

## 📄 License

This project is open source and available under the [MIT License](LICENSE).


# This is to run the code in a website

```
st.title("Password Generator")
length = st.number_input("Enter the length of the password", min_value=1, max_value=100, step=1)
if st.button("Generate"):
    password = generate_password(length)
    st.write("Generated password:", password)
```

# Example usage:
```
#password_length = 12  # You can change the length as needed
#password_length = int(input("Enter the length: "))
#print("Generated password:", generate_password(password_length))  
