# Project2
#Simple snake water gun game in python
# Label program
# author:Bhagyashree
# Location:Pune
# Date:15/11/2020
#Simple snake water gun game in python

import random
#snake=s water=s gun=g

def gameWin(comp,you):
    #if two values are equal declare a tie!
    if comp==you:
        return None
    #check for all possibilities when compute choose s
    elif comp=='s':
        if you=='w':
            return False
        elif you=='g':
            return True

    # check for all possibilities when compute choose w
    elif comp=='w':
        if you=='g':
            return False
        elif you=='s':
            return True

    # check for all possibilities when compute choose g
    elif comp=='g':
        if you=='s':
            return False
        elif you=='w':
            return True
print("comp turn:snake(s),water(w)or gun(g)?")
randNo=random.randint(1,3)
if randNo==1:
    comp='s'
elif randNo==2:
    comp='w'
elif randNo==3:
    comp='g'
you=input("your turn:snake(s),water(w)or gun(g)?")
a=gameWin(comp,you)
print(f"computer choose {comp}")
print(f"you choose {you}")
if a==None:
    print("the game is a tie!")
elif a:
    print("you win!")
else:
    print("you lose!")
'''#OUTPUT:
comp turn:snake(s),water(w)or gun(g)?
your turn:snake(s),water(w)or gun(g)?s
computer choosew
you chooses
you win!'''
