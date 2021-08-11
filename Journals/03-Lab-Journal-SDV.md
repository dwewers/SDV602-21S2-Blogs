# SDV601 - Week 3 Blog

What have I learned?

This week I learned about tuples, input(), and improved my knowledge on lists.

As stated by Edpresso Team (2021), "A tuple is an immutable list of Python objects which means it can not be changed in any way once it has been created. Unlike sets, tuples are an ordered collection."

input() is used when we want to read what the user has put into the console. This acts as a pause in the code while the system waits for the user input. We can set a variable to the value of the input for further use, whether it is comparison or to display.

## Task one 

Add a new menu method called "run_menu_two" that is executed when the top level menu item for Menu Two is selected. That method is to show a new menu using the same tuple format – with different menu items.

```python
def run_menu_two(a_value):
    menu_two =  (\
                   "Select a number.",\
                   (1,"I am the first option",test_cmd),  \
                   (2,"I am the second option",test_cmd),   \
                   (3,"Quit",quit_cmd)\
                 )
    run_menu(menu_two)
    return True
    
    if __name__ == "__main__":
    menu_tuple = (\
                   "Select a number.",\
                   (1,"Menu One",run_menu_one),  \
                   (2,"Menu Two",run_menu_two),   \ #added the method here
                   (3,"Menu Three",test_cmd), \
                   (4,"Quit",quit_cmd)\
                 )
    run_menu(menu_tuple)
```

## Task Two

Change menu_example.py, replace menu_tuple with menu_list. Adjust all existing code to work with menus as lists.

```python
def run_menu_one(a_value):
    menu_one =  ["Select a number.",(1,"Menu Burger",test_cmd),  (2,"Menu Chips",test_cmd),   (3,"Quit",quit_cmd)] #Changed to list
    run_menu(menu_one)
    return True

def run_menu_two(a_value):
    menu_two =  ["Select a number.",(1,"I am option one",test_cmd),  (2,"I am option two",test_cmd),   (3,"Quit",quit_cmd)] #Changed to list
    run_menu(menu_two)
    return True


if __name__ == "__main__":
    menu_list = ["Select a number.",(1,"Menu One",run_menu_one),  (2,"Menu Two",run_menu_two),   (3,"Menu Three",test_cmd), (4,"Quit",quit_cmd)] #Changed to list
    run_menu(menu_list)
```

## Text based adventure game

```python
import random

items = []


def chest(score):
    random_Number = random.randint(10, 1000)
    score = score + random_Number
    randItem = random.sample(
        {'Sword', 'gold', 'diamond', 'shield', 'food'}, 1)
    print("you have found a chest")
    print("Press enter to open the chess")
    inputType = input()
    print(f"Congratulations. You have found: {randItem}")
    items.append(randItem)
    print("Your score is:" + f" {score}")


def set_Location(location):
    return (f"Your location is: {location}")


def get_Input():
    return input()


def fight():
    random_Number = random.randint(1, 5)
    print("Oh no, a rouge skeleton has appeared")
    print("Type a number between 1 and 5 to kill the skeleton")
    print(random_Number)
    if(get_Input() == random_Number):
        print("You have killed the skeleton")
        return 1
    else:
        print("You have died")
        return 0


def main():
    score = 0
    print(set_Location("The Shire"))
    print("Type left to go to the castle, right to go too the cave")
    if (get_Input() == "left"):
        print(set_Location("Castle"))
        print("Type left to go to up the spiral stairs, right to go down to the catacombs")

        if (get_Input() == "left"):
            print(set_Location("Castle Spire"))
            chest(score)
            get_Input()
            print("Heading back down...")
            print("Type left to leave the castle or right to go down to the catacombs")
            if (get_Input() == "left"):
                print(
                    "Type left to go to the distant village, right to enter the dark thicket, or forward to the beach")
                if (get_Input() == "left"):
                    print(set_Location("Village"))
                elif (get_Input() == "forward"):
                    print(set_Location("Beach"))
                elif (get_Input() == "right"):
                    print(set_Location("Dark Thicket"))
            else:
                print(set_Location("Catacombs"))
                if(fight()):
                    chest(score)
                else:
                    return
        else:
            print(set_Location("Catacombs"))
            if(fight()):
                chest(score)
            else:
                return
    else:
        set_Location("Cave")
        get_Input()


if __name__ == "__main__":
    """ This is executed when run from the command line """
    main()


```

------

How have I learned this?

I have learned this by implementing methods that I have used in the past. I did some research into how we use tuples and input(), then implemented my knowledge. I already knew what lists were and how to use them, which meant that this was a bit easier than other tasks that were new to me


------

Why have I learned this?

I believe that I have learned these techniques as they are basic skills that we will use when it comes to writing code for later tasks and assessments. I also believe that we have learned this to show that these techniques relate to other languages such as JavaScript and HTML. On top of this, I believe that this is to show that there is not just one method when it comes to performing a task. Each of these examples show a different way to essentially perform the same task.


------

What will I do to remember this learning?

I will continue to practice and look at other code examples, implementing these learned skills into the tasks. I will also use these skill where necessary in our projects to come.

------

What is the point?

I believe that the point of this (as mentioned previously), is that they are basic skills that we will use when it comes to writing code for later tasks and assessments. I also believe that its to show that these techniques relate to other languages such as JavaScript and HTML.

------

What do I know now, that I did not know before?

I learned how to use the `random` library to get a random number in a specified range. Here is an example: `random.randint(10, 1000)`, which returns a value in the range of 10-1000

**References**

Edpresso Team. (2021, August 10). *What are tuples in Python?* Educative: Interactive Courses for Software Developers. https://www.educative.io/edpresso/what-are-tuples-in-python
