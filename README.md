# The-Rave-Game
# Exercise 45 of Learn Python the Hard Way by Zed Shaw

from sys import exit

#1.1 if yes, then go here

def raven():
    print "The door swings open, in the darkness appeared a Raven above the chamber door."
    print "The Raven then says 'Nevermore?''"
    print "How do you get rid of the Raven so you can go back to napping?"
    print "Select one: 'taunt' or 'shoo'"

    next = raw_input ("> ")

    if next == "taunt":
        end("The Raven gets pissed off and rips your eye off.")
    elif next == "shoo":
        end("The Raven flies out the open window so you can go back to bed.")
    else:
        start()
#1.3 if no, then go here

def demon():
    print "You ignore the Raven and go back to napping."
    print "Unbeknownst to you, a demon awaits for you inside."
    print "The demon locks eyes with you and you freak out."
    print "Do you flee for your life or passout?"
    print "Select one: 'flee' or 'passout'"

    next = raw_input ("> ")

    if next == "passout":
        end("The demon then says, 'Well that was tasty!")
    elif next == "flee":
        print "You run out into the hallway.  There is a door to your left and right."
        print "Which door do you take? Select one: 'left' or 'right' "
    else:
        start()

    next = raw_input ("> ")

    if next == "right":
        end("Good choice, you are safe for now.")
    elif next == "left":
        end("Bad choice, you just walked into an unkindness of hungry Ravens.")
    else:
        print "It's easy, type one of the following options: 'left' or 'right'"

def end(why):
    print why, "The end!"
    exit(0)


#1. start here

def start():
    print "Once upon a midnight dreary, there was a tapping at the chamber door."
    print "Do you open the door? (select one: 'yes' or 'no')"

    valid = ["yes", "no"]
    next = ''
    while next not in valid:
        next = raw_input("> ")

    if next == "yes":
        raven()
    elif next == "no":
        demon()
    #else:
    #     start()

start()

