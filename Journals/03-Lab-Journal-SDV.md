# SDV601 - Week 3 Blog

What have I learned?

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



------

How have I learned this?


------

Why have I learned this?


------

What will I do to remember this learning?
sdasd

------

What is the point?

------

What do I know now, that I did not know before?
