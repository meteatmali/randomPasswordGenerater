# randomPasswordGenerater
letters = ['a', 'b', 'c', 'd', 'e', 'f', 'g', 'h', 'i', 'j', 'k', 'l', 'm', 'n', 'o', 'p', 'q', 'r', 's', 't', 'u', 'v', 'w', 'x', 'y', 'z', 'A', 'B', 'C', 'D', 'E', 'F', 'G', 'H', 'I', 'J', 'K', 'L', 'M', 'N', 'O', 'P', 'Q', 'R', 'S', 'T', 'U', 'V', 'W', 'X', 'Y', 'Z']
numbers = ['0', '1', '2', '3', '4', '5', '6', '7', '8', '9']
symbols = ['!', '#', '$', '%', '&', '(', ')', '*', '+']
import random
print("Welcome to the PyPassword Generator!")
nr_letters = int(input("How many letters would you like in your password?\n"))
nr_symbols = int(input(f"How many symbols would you like?\n"))
nr_numbers = int(input(f"How many numbers would you like?\n"))
numberscheck=0
symbolscheck=0
letterscheck=0
while (numberscheck+symbolscheck+letterscheck<nr_symbols+nr_letters+nr_numbers):
    c =random.randint(0,2)
    if c ==0 and   numberscheck<nr_numbers:
            x = random.randint(0,len(numbers)-1)
            print(numbers[x],end="")
            numberscheck+=1
    elif c ==1 and letterscheck<nr_letters:
            y =random.randint(0, len(letters)-1)
            print(letters[y],end="")
            letterscheck += 1
    elif c ==2 and symbolscheck<nr_symbols:
            z = random.randint(0, len(symbols)-1)
            print(symbols[z],end="")

            symbolscheck+=1



