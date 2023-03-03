# pyclock
This is a clock made with Python. It tells you the current date, time and day. It also has an apperance that you can change in the source code.
This is how it works: 
     
from tkinter import *  - Imports the time and
from time import *     - tkinter libraries

def update():                                   -
    time_string = strftime("%I:%M:%S %p")        |
    time_label.config(text=time_string)          |
                                                 |   
    day_string = strftime("%A")                  | 
    day_label.config(text=day_string)             - Updates the time and day every 1000 milliseconds and controls the date, time and day format.
                                                 |
    date_string = strftime("%B %d, %Y")          |
    date_label.config(text=date_string)          |
                                                 |
    window.after(1000,update)                   -
 

window = Tk()   -------------------------------------------------- Creates the window

time_label = Label(window,font=("Courier New",50),fg="#00FF00",bg="black")    -
time_label.pack()                                                              |
                                                                               |
day_label = Label(window,font=("Courier New",25),fg="#00FF00",bg="black")       -  Controls the appearance of the day, time and date, and loads the label packs.
day_label.pack()                                                               |
                                                                               |
date_label = Label(window,font=("Courier New",30),fg="#00FF00",bg="black")     |
date_label.pack()                                                             -

update() ----- Updates the window

window.mainloop() ---- Putting the update in a loop.
