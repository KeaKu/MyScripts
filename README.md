def guess_game():
    import random
    rand = random.randint(1, 1000)
    name = str(input("Hello! What is your name? "))
    print("Hi, " + str(name), "I have just chosen a number from 1 - 1,000 ")
    print("Try guessing the number, ill help you.  Trust me :)  ")
    number = int(input())
    count = 1

    if 0 < number < 1000:
        while rand != number:
            if rand > number:
                print("The number i chose is bigger ! Tty again >")
                number = int(input())
                count += 1
                if 0 > number or number > 1000:
                    print("Error, ive asked for a number between 1 - 1000 !!! ")
                    break
            if rand < number:
                print("The number i chose is smaller ! Try again >")
                number = int(input())
                count += 1
                if 0 > number or number > 1000:
                    print("Error, ive asked for a number between 1 - 1000 !!! ")
                    break
    else:
        print("Error, ive asked for a number between 1 - 1000 !!! ")
    if rand == number:
        print("My number was ---->> " + str(rand), " <<---- Well done!")
        print(name, ", It took you ", count, " times to guess. ")

def calculator():
