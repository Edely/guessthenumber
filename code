import simplegui
import random
import math

n = 7
idi = 0
range1 = random.randrange(0, 100)
print "Let's play! The range goes from 0 to 100."
print "You have 7 guesses."


def new_game():
    
    global secret_number
    secret_number = range1
    


def range100():
    global range1
    range1 = random.randrange(0, 100)
    print "Let's play! The range goes from 0 to 100."
    print "You have 7 guesses."
    global n
    n = 7
    global idi
    idi = 0
    new_game()
    
    

def range1000():
    global range1
    range1 = random.randrange(0, 1000)
    print "Let's play! The range goes from 0 to 1000."
    print "You have 9 guesses."
    global n
    n = 9
    global idi
    idi = 1
    new_game()
    
def input_guess(guess):
    global n
    n = n - 1
    guess = int(guess)
    print "Guess was", guess
    if guess < secret_number:
        print "Higher"
        print "You have", n, "guesses."
    elif guess > secret_number:
        print "Lower"
        print "You have", n, "guesses."
    else:
        print "Correct!"
        if idi == 0:
            range100()
        elif idi == 1:
            range1000()
        
    if n < 1:
        print "You ran out of guesses. Game Over!"
        if idi == 0:
            range100()
        elif idi == 1:
            range1000()



frame = simplegui.create_frame('Guess the Number', 300, 300)
inp = frame.add_input('Your Guess:', input_guess, 40)
one_to_100 = frame.add_button('Range: 0 - 100', range100, 100)
one_to_1000 = frame.add_button('Range: 0 - 1000', range1000, 100)



new_game()


