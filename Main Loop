from pygame import *

#import Renpy

stack = []

#created by TheCorruptedBit

#quick note: this engine parses text files. It can be simplified if parsing is
#the only thing we want to do. Currently, the features are:
#Parse, Wait

#bugs: Clock isn't defined, so its commented out.

#comment if not setting up for pygame (altho Ren'Py is a version of Pygame, so
#it may be redundant

init()
screen = display.set_mode((1280,960))
display.set_caption("Conspiracy College Empty Loop")

running = True

#oh, by the way, test it with a blank text file named Foo, or whatever name
#      V         you're testing it with (uncomment first!)         V

#loadedScript = open("Foo")

#parse the stack
def ParseStack():
    for x in stack[0]:
        if stack[0][x] == "parse":
            ParseScript()
            stack[1].append("parse")
            #follows next script instruction
        elif stack[0][x][0:4] == "wait":
            for y in range(0,int(stack[0][x][5])+1):
                stack.insert(0,[])
            #Creates Y actionless frames until the next instruction
    stack.remove(0)

def ParseScript():
    #parse the script... Something with LoadedScript
    pass

while running:
    for e in event.get():        
        if e.type == QUIT:
            running = False   
    print("tick " + str(time.get_ticks()))
    
    ParseStack()
    
    #clock.tick(60)
