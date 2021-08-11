# Number-Guessing
Make a program in which the computer randomly chooses a number between 1 to 10, 1 to 100, or any range. Then give users a hint to guess the number. Every time the user guesses wrong, he gets another clue, and his score gets reduced. The clue can be multiples, divisible, greater or smaller, or a combination of all.


import random

n = random.randint(1, 101)
count = 0
guess_number = 10

while count < guess_number:
    num = int(input("Guess the number: "))
    if num > n:
        print("Your guess was too high: Guess a number lower than", num)
    elif num < n:
        print("Your guess was too low: Guess a number higher than", num)
    else:
        print("You win!")

    count += 1
    print("You have taken", count, "tries")

if count >= guess_number:
    print("Game over")
    print("The number is %d" %n)




