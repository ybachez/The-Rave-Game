I created a word game during Halloween season.  I was inspired by Edgar Allan Poe's poem The Raven, I created a word game using Python for Exercise 45 of Learn Python the Hard Way by Zed Shaw.


Intro:

Once upon a midnight dreary, there was a tapping at the chamber door,
Do you open the door? (select one: 'yes' or 'no')

PART TWO:

> yes	> no
The door swings open, in the darkness appeared a Raven above the chamber door.
The Raven then says 'Nevermore.'
What did this grim, ghastly, ominous bird mean by 'Nevermore?'
How do you get rid of the Raven so you can go back to napping?
Select one: 'taunt' or 'shoo'	You ignore the Raven and go back to napping.
Unbeknownst to you, a demon awaits for you inside.
The demon locks eyes with you and you freak out.
Do you flee for your life or passout? 
Select one: ‘flee’ or ‘passout’
> taunt	> shoo	> flee	> passout
The Raven gets pissed off and rips your eye off. 	The Raven flies out the open window so you can go back to bed.	You run out into the hallway.  There is a door to your right and left.  Which one do you take? 	The demon then says, ‘Well that was tasty!’
The end!	> right	> left	The end!
		Good choice, you are safe for now.  	Bad choice, the Raven flew in here and rips your eye off.	
		The end!	




from sys import exit

#def gold_room():
    #print "Imagine the following scenario. How much do you take? (enter a number)"

    #next = raw_input("> ")
    #if "0" in next or "1" in next:
    #    how_much = int(next)
    #else:
    #    dead("Geez, learn to type a number.")

    #if how_much < 50:
    #    print "Nice, you're not greedy, you win!"
    #    exit(0)
# exit(0) the zero means there were no errors
    #else:
    #    dead("You took too many greedy bastard!")

def raven_room():
    print "The door swings open, in the darkness appeared a Raven above the chamber door."
    print "The Raven then says 'Nevermore.'"
    print "What did this grim, ghastly, ominous bird mean by 'Nevermore?'"
    print "How do you get rid of the Raven so you can go back to napping?"
    print "Do you taunt the Raven or shoo the Raven? 
    print “Select one: 'taunt' or 'shoo'"
    raven_moved = False

# bear_moved is a boolean variable
#
    while True:
        next = raw_input("> ")

        if next == "shoo Raven":
            print "The Raven flies out the open window."
            raven_moved = True
        elif next == "taunt the Raven":
            dead("The Raven gets pissed off and rips your eye off.")
        #elif next == "ignore Raven and close door" and raven_moved:
            gold_room()
# function "gold_room" was defined in line 3

        else:
            print "Try again."

def demon_room():
    print "You ignore the Raven and go back to napping."
    print "Unbeknownst to you, a demon awaits for you inside."
    print "The demon locks eyes with you and you go insane in the membrane."
    print "Do you flee for your life or passout?"

    next = raw_input("> ")

    if "flee" in next:
        start()
    elif "passout" in next:
        dead("The demon then says 'Well that was tasty!'")
    else:
        demon_room()

def dead(why):
    print why, "The end!"
    exit(0)

# First prompt to be asked on terminal

def start():
    print "Once upon a midnight dreary, there was a tapping at the chamber door,"
    print "Do you open the door? (type 'yes' or 'no')"

    next = raw_input("> ")

    if next == "yes":
        raven_room()
    elif next == "no":
        demon_room()
    else:
        dead("You stumble around the dark room until you die.")

start()





