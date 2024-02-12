# PASSWORD-GENERATOR
import random
import string

def generate_password(length):
    characters = string.ascii_letters + string.digits + string.punctuation
    password = ''.join(random.choice(characters) for _ in range(length))
    return password

def main():
    length = int(input("Enter the desired length of the password: "))
    if length <= 0:
        print("Please enter a valid length greater than 0.")
        return
    password = generate_password(length)
    print("Generated Password:", password)

if __name__ == "__main__":
    main()
