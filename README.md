# password_generator
This repository contains a python code for a password generator which can be run in web. 

import streamlit as st
import random
import string

def generate_password(length):
    # Define the possible characters: lowercase, uppercase, digits, and symbols
    characters = string.ascii_letters + string.digits + string.punctuation

 # Randomly select characters from the pool
password = ''.join(random.choice(characters) for i in range(length))
return password



# this is to run the code in a website
st.title("Password Generator")
length = st.number_input("Enter the length of the password", min_value=1, max_value=100, step=1)
if st.button("Generate"):
    password = generate_password(length)
    st.write("Generated password:", password)

# Example usage:
#password_length = 12  # You can change the length as needed
#password_length = int(input("Enter the length: "))
#print("Generated password:", generate_password(password_length))  

