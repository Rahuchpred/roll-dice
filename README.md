import random
counts = 0
total = 0
mode = input("Type 'count' to roll n time"
             + "or type 'limit' to roll until limit : ")
if mode == "count":
    quantity = int(input("How many time you want it to roll? "))
    while counts < quantity:
        first_die = random.randint(1, 6)
        second_die = random.randint(1, 6)

        dice_sum = first_die + second_die
        counts = counts + 1
        total += dice_sum
        print("You rolled a " + str(dice_sum) + "!")
        print("Dice sum is " + str(int(dice_sum)))

        if counts == int(quantity):
            average = total / quantity
            print("The Average is " + str(average))


elif mode == "limit":
    limit = int(input("How much total you want? "))
    counts = 0
    total = 0
    roll_dices = 0
    while total < limit:
        first_die = random.randint(1, 6)
        second_die = random.randint(1, 6)

        dice_sum = first_die + second_die
        counts = counts + 1
        total += dice_sum
        roll_dices += 1
        print("You rolled a " + str(dice_sum) + "!")
        print("Total reached:", total)
    average = total / roll_dices
    print("Average roll:", average)
else:
    print("Oops Eror")
