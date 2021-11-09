

# SDV601 - Week 1 Blog

------

#### <u>Setting Up the Development Environment, Variables, and Code Convention</u>

------

What have I learned?

This week I learned about setting up the environment that I will be working in as well as what the correct way to write code into a file in python.


------

How have I learned this?

I learned this by following some tutorials online that were provided in the documentation. The main source that I followed was the tutorial on using python as a calculator.

The python interpreter acts as a simple calculator. We can insert expressions into the terminal and it will return its value. Below we can see a table of what symbols do when entered in an expression:

| Symbol         | Use                                                          | Example           | Returned value |
| -------------- | ------------------------------------------------------------ | ----------------- | -------------- |
| +              | Used for addition                                            | 10 + 5            | 15             |
| -              | Used for subtraction                                         | 50 - 142          | -92            |
| *              | Used for multiplication                                      | -19 * -12         | 288            |
| /              | Used for division                                            | 100 / 5           | 20             |
| ()             | Used for grouping                                            | (10 * 3) ** 2     | 900            |
| //             | Used to return an integer result rounded down to the whole number (floor) | 8423.928 // 12.22 | 689.0          |
| %              | Used to return the remainder                                 | 1942 % 27         | 25             |
| **             | Use to calculate powers                                      | 10**4             | 10,000         |
| _ (Underscore) | Variable that the last printed expression is assigned too    | 20*2 = 40<br />_  | 40             |

I also learned that you can also manipulate strings using python:

| Symbol | Use                                                          | Example                               | Returned Value   |
| ------ | ------------------------------------------------------------ | ------------------------------------- | ---------------- |
| '...'  | To enclose the text                                          | 'Hello World'                         | 'Hello World'    |
| "..."  | To enclose the text                                          | "Hello World"                         | 'Hello World'    |
| \      | Escape quotes                                                | "Doesn\\'t"                           | "Doesn't"        |
| \n     | New Line                                                     | print('Hello \nworld')                | Hello <br/>world |
| r      | When you do not want \ to be identified as a special character | print(r'C:\users\daniel')             | C:\users\daniel  |
| +      | Concatenate multiple strings                                 | "Hello" + " " + "World"               | Hello World      |
| *      | Repeat a string a given amount of times                      | "LOL"*3                               | LOLLOLLOL        |
| +      | Can also be used to concatenate variables and literals       | \>>> x = "abc"<br />\>>> "Look: " + x | 'Look: abc'      |

Examples:

```python
((2**3)*2)-15 #Returns 1

((5*2)*16)+222 #Returns 328

"My" + " " + "Name" + " "  + "Is" + " " + "Daniel" #Returns 'My Name Is Daniel'

x = "Potato"
y = "Gravy"

"I" + " " + "Like" + " " + x + " " + "and" + " " + y #Returns 'I Like Potato and Gravy'
```

Below is an example of another way we can use Python:

```python
#This checks to see if the values in the arrays are all unique.
#True when unique, false when there are duplicates.

def all_unique(lst):
    return len(lst) == len(set(lst))
def jls_extract_def():
    
    x = [1,1,2,2,3,2,3,4,5,6]
    y = [1,2,3,4,5]
    print(all_unique(x)) #False
    print(all_unique(y)) #True
    return y

y = jls_extract_def()
```

------

Next I learned how to use Python to create a graphical plot. This required us to use the `matplotlib` library. Below we can see the code implemented to import the packages and create the graph:

```python
import matplotlib.pyplot as plt
import numpy as np

x = np.linspace(0, 20, 100)  # Create a list of evenly-spaced numbers over the range
plt.plot(x, np.sin(x))       # Plot the sine of each x point
plt.show()                   # Display the plot
```

This gives us the following results:

![image-20210723182835881](https://i.imgur.com/wykqnng.png)


------

Why have I learned this?

I believe that I have learned these techniques as they are basic skills that we will use when it comes to writing code for later tasks and assessments. I also believe that we have learned this to show that these techniques relate to other languages such as JavaScript and HTML. 


------

What will I do to remember this learning?
I will continue to practice and look at other code examples, implementing these learned skills into the tasks. I will also use these skill where necessary in our projects to come.

------

What is the point?

I believe that the point of this (as mentioned previously), is that they are basic skills that we will use when it comes to writing code for later tasks and assessments. I also believe that its to show that these techniques relate to other languages such as JavaScript and HTML. 

------

What do I know now, that I did not know before?

- How to create graphs using Python
- How to write Python code to the console

# PROJECT BRIEF

I'll be working on an application that enables live and interactive graphical presentations, including charts, enabling a business (or scientific) analyst to provide multiple graphical perspectives of data sources. Data Explorer Screens are live interactive graphical displays that allow users to explore data from a data source (DES). The programme receives text input and mouse clicks at each DES and provides a brief summary of the scenario in relation to the data in an adjustable chart. Data explorer panels are available in the programme. Each screen has a chart and allows both text and pointer (i.e. mouse) input.

The application will allow users to control and show at least three distinct DESs using console text input. Each DES includes graphics (each based on its own data source) as well as a summary or comparative analytical data. For analysts examining the current DES, the system will include a chat system that can be accessible via a remote http-based API using a remote data service. The final system will retrieve data from a remote data source that is shared. At each display, the screens will provide a number of alternatives for data viewing.

## PURPOSE

The purpose of the application is to allow more than one analyst to view the same DES at the same time and upload and retrieve data on a shared remote server. Two or more analysts can communicate with each other using a text chat system when they are viewing the same screen. This will be present in all of the DES.

FEATURES

The application will include the following (as stated previously):

- Live and interactive graphical displays

- Brief description of the situation relating to the displayed information/Brief summary

- Console text-based input to control and display at least three different DES’s

- Chat system

- Retrieves data from a shared remote data source

- Tools for adjusting the view (such as zoom, pan). Might include colour settings for easier viewing.

- Multi-user access to views.

- Ability to upload and retrieve the data.

- Login and logout system.


------

# SDV601 - Week 2 Blog

------

#### <u>Setting Up the Development Environment, Variables, and Code Convention</u>

------

What have I learned?

## Lesson One


**Task 1:**

```python
# Task one
def task_one():
    for x in range(1, 100):
        if x % 5 == 0 and x % 3 == 0:
            print("FizzBuzz")
        elif x % 3 == 0:
            print("Fizz")
        elif x % 5 == 0:
            print("Buzz")
        else:
            print(x)
```

**Task 2:**

```python
# Task two
def task_two():
    x = 0
    while x < 100:
        if x % 5 == 0 and x % 3 == 0:
            print(f"{x} is FizzBuzz")
            x = x + 1
        elif x % 3 == 0:
            print(f"{x} is Fizz")
            x = x + 1
        elif x % 5 == 0:
            print(f"{x} is Buzz")
            x = x + 1
        else:
            print(x)
            x = x + 1
```

**Task Three:**

```python
def task_three():
    ints = list(range(1, 51))

    for idx, val in enumerate(ints):
        if val % 5 == 0 and val % 3 == 0:
            print(f"\nIndex is: {idx+1} \nValue is: {val} \nResult is: FizzBuzz")
        elif val % 3 == 0:
            print(f"\nIndex is: {idx+1} \nValue is: {val} \nResult is: Fizz")
        elif val % 5 == 0:
            print(f"\nIndex is: {idx+1} \nValue is: {val} \nResult is: Buzz")
        else:
            print(f"\nIndex is: {idx+1} \nValue is: {val}")
```

**Task Four:**

```python
def task_four(fizz, buzz, up_too):
    ints = list(range(0, up_too))
    for idx, val in enumerate(ints):
        if val % fizz == 0 and val % buzz == 0:
            print(f"\nIndex is: {idx+1} \nValue is: {val} \nResult is: FizzBuzz")
        elif val % fizz == 0:
            print(f"\nIndex is: {idx+1} \nValue is: {val} \nResult is: Fizz")
        elif val % buzz == 0:
            print(f"\nIndex is: {idx+1} \nValue is: {val} \nResult is: Buzz")
        else:
            print(f"\nIndex is: {idx+1} \nValue is: {val}")
if __name__ == "__main__":
    task_four(3, 5, 50)
```

**Calling the method:**

```python
if __name__ == "__main__":
    methodName()
```

## Lesson Two

**Task One :**

  Return one value that is the sum of the column `column_name` of each "row" (dictionary)

```python
def sum_of(column_name, a_list_of_dictionary):
    """
    Return one value that is the sum of the column 
    column_name of each "row" (dictionary)
    """
    lines = ""
    
    # Get a header line
    a_dictionary = a_list_of_dictionary[0]
    header_line = ""
    for key in a_dictionary:
        if (key == column_name):
            header_line += f'{key}\t'
    header_line = header_line.strip()

    # Make up the table
    lines += header_line 
    vals = []
    for a_dictionary in a_list_of_dictionary:
        a_line = ''
        for key,value in a_dictionary.items():
            if (key == column_name):
                vals.append(int(value))
    a_line = a_line.strip()
    getSum = sum(vals)
    lines += f'\n{getSum}'
    print(lines)
    pass

if __name__ == "__main__":
   parser = argparse.ArgumentParser(description="Scan some rows into a list of one list per line.")
   parser.add_argument('--header',action='store_true',help='The first row is a header row.')
   args = vars(parser.parse_args())
   print(f'The args are {args}')
   #args = sys.argv
   #print(f'The args are {args}')
   dict_lst,values_lst = scan(args['header'])
   sum_of("Length", dict_lst)
```

**Output:**

```javascript
$ py data_scan.py --header<data_with_header.csv 
The args are {'header': True}
Length
7
```

**Task 2:**

  Return a new list of "rows" (dictionary) that multiples the values of the named columns

```python
import numpy as np

def multiple_cols(column_names,a_list_of_dictionary):
    """
    Return a new list of "rows" (dictionary)
    That multiples the values of the named columns
    """
    lines = ""
    
    # Get a header line
    a_dictionary = a_list_of_dictionary[0]
    header_line = ""
    for key in a_dictionary:
        header_line += f'{key}\t'
    header_line = header_line.strip()
    
    # Make up the table
    lines += header_line 
    length = []
    width = []
    for a_dictionary in a_list_of_dictionary:
        a_line = ''
        for key,value in a_dictionary.items():
            for rows in column_names:
                if (key == rows and rows == "Length"):
                    length.append(int(value))
                elif (key == rows and rows == "Width"):
                    width.append(int(value))
    length = "Length: " + str(np.prod(length))
    width = "Width: " + str(np.prod(width))
    print(f"{length}\n{width}")
    pass

if __name__ == "__main__":
   parser = argparse.ArgumentParser(description="Scan some rows into a list of one list per line.")
   parser.add_argument('--header',action='store_true',help='The first row is a header row.')
   args = vars(parser.parse_args())
   print(f'The args are {args}')
   #args = sys.argv
   #print(f'The args are {args}')
   dict_lst,values_lst = scan(args['header'])
   sum_of(["Length", "Width"], dict_lst)
```

**Output:**

```javascript
$ py data_scan.py --header<data_with_header.csv 
The args are {'header': True}
Length: 12
Width: 20
```

Task 3:

Fix display_table so that the columns all line up

```python
from tabulate import tabulate

def display_table(a_list_of_dictionary):
    lines = ""
    # Get a header line
    a_dictionary = a_list_of_dictionary[0]
    header_line = ""
    for key in a_dictionary:
        header_line += f'{key}\t'
    header_line = header_line.strip()
    # Make up the table
    lines += header_line 
    arr = [[],[]]
    i = 0;
    for a_dictionary in a_list_of_dictionary:
        a_line = ''
        for key,value in a_dictionary.items():
            if(i <= 4):
                arr[0].append(value)
                i = i + 1
            else:
                arr[1].append(value)
    print(tabulate(arr, headers=["Name", "Item","Value","Length","Width"]))

if __name__ == "__main__":
   parser = argparse.ArgumentParser(description="Scan some rows into a list of one list per line.")
   parser.add_argument('--header',action='store_true',help='The first row is a header row.')
   args = vars(parser.parse_args())
   print(f'The args are {args}')
   #args = sys.argv
   #print(f'The args are {args}')
   dict_lst,values_lst = scan(args['header'])
   display_table(dict_lst)
```

**Input Example One:**

```python
Name, Item,Value,Length,Width
aline, 1,2234,3,4
bline, 2234,3,4,5234
```

**Output Example One:**

```javascript
$ py data_scan.py --header<data_with_header.csv 
The args are {'header': True}
Name      Item    Value    Length    Width
------  ------  -------  --------  -------
aline        1     2234         3        4
bline     2234        3         4     5234
```

**Input Example Two:**

```python
Name, Item,Value,Length,Width
aline, 5342534253425345342,223535858568,226824352,34
bline, 223234,234634266,236,346326
```

**Output Example Two:**

```javascript
$ py data_scan.py --header<data_with_header.csv 
The args are {'header': True}
Name                    Item         Value     Length    Width
------  --------------------  ------------  ---------  -------
aline    5342534253425345342  223535858568  226824352       34
bline                 223234     234634266        236   346326
```




------

How have I learned this?

I have learned this by implementing methods that I have used in the past. I did some research into how if statements are structured, then implemented my knowledge. I already knew how to do a for loop with a range and use `%` to check for the remainder.


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

- That you use `and` instead of `&&`
- Use of a library reduces spaghetti code

# PROJECT BRIEF

I'll be working on an application that enables live and interactive graphical presentations, including charts, enabling a business (or scientific) analyst to provide multiple graphical perspectives of data sources. Data Explorer Screens are live interactive graphical displays that allow users to explore data from a data source (DES). The programme receives text input and mouse clicks at each DES and provides a brief summary of the scenario in relation to the data in an adjustable chart. Data explorer panels are available in the programme. Each screen has a chart and allows both text and pointer (i.e. mouse) input.

The application will allow users to control and show at least three distinct DESs using console text input. Each DES includes graphics (each based on its own data source) as well as a summary or comparative analytical data. For analysts examining the current DES, the system will include a chat system that can be accessible via a remote http-based API using a remote data service. The final system will retrieve data from a remote data source that is shared. At each display, the screens will provide a number of alternatives for data viewing.

## PURPOSE

The purpose of the application is to allow more than one analyst to view the same DES at the same time and upload and retrieve data on a shared remote server. Two or more analysts can communicate with each other using a text chat system when they are viewing the same screen. This will be present in all of the DES.

FEATURES

The application will include the following (as stated previously):

- Live and interactive graphical displays

- Brief description of the situation relating to the displayed information/Brief summary

- Console text-based input to control and display at least three different DES’s

- Chat system

- Retrieves data from a shared remote data source

- Tools for adjusting the view (such as zoom, pan). Might include colour settings for easier viewing.

- Multi-user access to views.

- Ability to upload and retrieve the data.

- Login and logout system.

I have decided that the data source I will be using is https://koordinates.com/ .  At this stage, I am looking at using https://koordinates.com/from/data.linz.govt.nz/layer/50804/ which is NZ Property Titles.

Data I can get from this looks like this:

![image-20210729150157543](https://i.imgur.com/av6BXbf.png)

The reason I have chosen the data from this data source is because I believe I can implement it well in a way that matches the criteria of needing too implement features such as zoom and pan. I believe that I can use the data well (such as property ID or coordinates) to plot different points on a graph and identify other key information about that set of data in a quick view.

------

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


------

# SDV601 - Week 4 Blog

------

What have I learned?

**Session 1**

In this session I learned how to create a simple application using Tkinter. Tkinter is an object oriented GUI package layer on top of the Tk package.  This is the most commonly used GUI package in the Python language.

Below is an example of a simple application with a button that prints to the console, and a button that closes the application

```python
class Application(tk.Frame):
    def __init__(self, master=None):
        super().__init__(master)
        self.master = master
        self.pack()
        self.create_widgets()

    def create_widgets(self):
        self.btn = tk.Button(self)
        self.btn["text"] = "Click Me"
        self.btn["command"] = self.say_hi
        self.btn.pack(side="top")
        self.quit = tk.Button(self, text="QUIT", fg="red",command=self.master.destroy)
        self.quit.pack(side="bottom")

    def say_hi(self):
        print("Hello World!")

root = tk.Tk()
app = Application(master=root)
app.mainloop()
```

Result:

![](https://i.imgur.com/1V9ETf3.png)

Button Clicked:

![](https://i.imgur.com/iic9ThD.png)


**Session 2**

In this lesson we learned about local and global variables. A local variable is one that is contained within a function and cannot be accessed by other methods. We can however pass their values to other methods as arguments. A global variable is one that is defined in the global scope (outside of any methods). This can be accessed anywhere within the scope of its environment. Below is an example of a global variable and a local variable:

```python
x = 6 #!This is a global variable that can be accessed outside the scope of a method

def foo():
    x = x * 2
    print(x)

def bar():
    x = x + 5
    print(x)
    
foo()
bar()
```

```python
def foo():
    y = 3 #! This is a local variable that can only be accessed within the scope of this method
    print(y)

foo()
```




------

How have I learned this?

I learned this by researching into how to use Tkinter and looking at different code examples. I practiced simple applications that perform simple tasks. These tasks were exactly the same as what we would see in normal python code such as printing to the console or creating a new file with some contents.

I also learned about another package called Kivy. This has the same concept of creating the application, but instead of inline styling, we create a file that we reference too and do the styling of elements in there. This was useful as it declutters the main python files from all of the styling needed to create a nice looking GUI.


------

Why have I learned this?

I believe that I have learned these techniques as they are basic skills that we will use when it comes to writing code for later tasks and assessments. As we are required to create an application with a GUI, it seems logical that we would choose the most popular package as there will likely be the most support and online tutorials available to help us.


------

What will I do to remember this learning?

I will continue to practice and look at other code examples, implementing these learned skills into the tasks. I will also use these skill where necessary in our projects to come.

------

What is the point?

I believe that the point of this is to show us one method to create a simple application.

------

What do I know now, that I did not know before?

As stated above, I learned about another package called Kivy. This has the same concept of creating the application, but instead of inline styling, we create a file that we reference too and do the styling of elements in there. This was useful as it declutters the main python files from all of the styling needed to create a nice looking GUI.

------

# SDV601 - Week 5 Blog

------

## Doc Strings

------

What have I learned?

This week I learned about doc strings.

Commenting is the process of describing your code to/for developers. The Python code maintainers and developers are the primary target audience. Comments, when used in conjunction with well-written code, assist the reader in better understanding your code, its purpose, and design. When you document code, you're telling your users how to use it and what it can do. While it may be useful in the development process, the users are the primary target audience.

There are many uses for commenting code. These include such things as planning and reviewing your code, description of code blocks, and tagging.

There are great extensions that help improve the styling and use of comments such as `Better Comments` and `Anchor Tags`. Below is a couple of implementations using these extensions.

![img](https://i.imgur.com/niNVwWk.png)

Doc stings are similar to general comments as their purpose is to help the users and yourself with documenting and understanding your code.

Below is an example of a class that has been well documented (Real Python, 2021):

```python
class Animal:
    """
    A class used to represent an Animal

    ...

    Attributes
    ----------
    says_str : str
        a formatted string to print out what the animal says
    name : str
        the name of the animal
    sound : str
        the sound that the animal makes
    num_legs : int
        the number of legs the animal has (default 4)

    Methods
    -------
    says(sound=None)
        Prints the animals name and what sound it makes
    """

    says_str = "A {name} says {sound}"

    def __init__(self, name, sound, num_legs=4):
        """
        Parameters
        ----------
        name : str
            The name of the animal
        sound : str
            The sound the animal makes
        num_legs : int, optional
            The number of legs the animal (default is 4)
        """

        self.name = name
        self.sound = sound
        self.num_legs = num_legs

    def says(self, sound=None):
        """Prints what the animals name is and what sound it makes.

        If the argument `sound` isn't passed in, the default Animal
        sound is used.

        Parameters
        ----------
        sound : str, optional
            The sound the animal makes (default is None)

        Raises
        ------
        NotImplementedError
            If no sound is set for the animal or passed in as a
            parameter.
        """

        if self.sound is None and sound is None:
            raise NotImplementedError("Silent Animals are not supported!")

        out_sound = self.sound if sound is None else sound
        print(self.says_str.format(name=self.name, sound=out_sound))
```


------

How have I learned this?

- By researching into key practices when commenting
- Looking at other examples of comments
- Practicing commenting code snippets


------

Why have I learned this?

When you build code, you have two audiences in mind: your users and your developers (including yourself). The importance of both audiences cannot be overstated. It's critical to document your code so that others can understand what it's doing and how it performs it.


------

What will I do to remember this learning?
Continue to practice commenting my code and ensure the my comments are concise and straight to the point.

------

What is the point?

As stated previously, when you build code, you have two audiences in mind: your users and your developers (including yourself). In order for our code to be more than just functional, we need to comment our code to ensure that other users will understand what elements of our code do and how they do it.

------

What do I know now, that I did not know before?

That there a many useful extensions that can help us style and generate comments/doc strings



Real Python. (2021, August 25). *Documenting Python Code: A Complete Guide*. https://realpython.com/documenting-python-code/

------

# SDV601 - Week 6 Blog

------

## **Graphs and Charts**

------

What have I learned?

This week I learned about the implementation of graphs and charts using the `matplotlib` library.

### Matplotlib

Matplotlib is a very useful tool for data analysis and is very easy to use. Many of the examples are very straight forward and allow us to visually represent data. There are many different simple and complex ways we can display this data from simple line graphs to 3D interactable models of data.

Below is several examples with their implementation:

<u>Simple Line Graph:</u>

```python
import numpy as np
import matplotlib.pyplot as plt

plt.plot([1, 2, 3, 4])
plt.show()
```

![line](https://i.imgur.com/UyobpiC.png)

<u>Dark Theme (My preferred):</u>

```python
import matplotlib.pyplot as plt
import numpy as np
plt.style.use('dark_background')

plt.plot([1, 2, 3, 4], [1, 4, 9, 16])
plt.show()
```

![dark](https://i.imgur.com/nieR08u.png)

<u>Sub Plots:</u>

```python
import numpy as np
import matplotlib.pyplot as plt

names = ['x', 'y', 'z']
values = [1, 10, 100]

plt.figure(figsize=(9, 3))

plt.subplot(131)
plt.bar(names, values)
plt.subplot(132)
plt.scatter(names, values)
plt.subplot(133)
plt.plot(names, values)
plt.suptitle('Sub Plots')
plt.show()
```

![sub](https://i.imgur.com/dmqj5Rn.png)

<u>Bar Graph:</u>

```python
import matplotlib.pyplot as plt
import numpy as np


labels = ['G1', 'G2', 'G3', 'G4', 'G5']
men_means = [20, 34, 30, 35, 27]
women_means = [25, 32, 34, 20, 25]

fig, ax = plt.subplots()
rects1 = ax.bar((np.arange(len(labels)) ) - 0.35/2, men_means, 0.35 , label='Men')
rects2 = ax.bar((np.arange(len(labels)) ) + 0.35/2, women_means, 0.35 , label='Women')

ax.set_ylabel('Scores')
ax.set_title('Scores by group and gender')
ax.set_xticks(np.arange(len(labels)) )
ax.set_xticklabels(labels)
ax.legend()

ax.bar_label(rects1, padding=3)
ax.bar_label(rects2, padding=3)

fig.tight_layout()

plt.show()
```

![bar](https://i.imgur.com/ehxyDk2.png)

<u>3D Modelling</u>:

```python
import numpy as np
import matplotlib.pyplot as plt

ax = plt.figure().add_subplot(projection='3d')

theta = np.linspace(-4 * np.pi, 4 * np.pi, 100)
z = np.linspace(-2, 2, 100)
r = z**2 + 1
x = r * np.sin(theta)
y = r * np.cos(theta)

ax.plot(x, y, z, label='3D Model')
ax.legend()

plt.show()
```

![3d](https://i.imgur.com/qs0ZEvO.png)


------

How have I learned this?

I have learned this by looking at tutorials online and following the steps to implement the different graph types. I have practiced using the different types and how to implement them.


------

Why have I learned this?

Python is a well used language when it comes to data analysis. The ability to implement a library such as matplotlib (or others such as plotly, seaborn, or ggplot) allows us to visually understand the data rather than reading numbers. 


------

What will I do to remember this learning?
I will continue to practice these techniques and find areas where I can implement this knowledge.

------

What do I know now, that I did not know before?

- I learned how to model a 3d graph
- How to change the them of the graphs from light to dark them


------

- # SDV601 - Week 7 Blog

  ------

  #### <u>Setting Up the Development Environment, Variables, and Code Convention</u>

  ------

  What have I learned?

  Although I have already done file manipulation, this week I improved my skills and understanding of file manipulation in Python. Like the name suggests, the concept of file manipulation revolves around anything to do with files whether it is opening and viewing the data, adding to the data, updating existing data, deleting data, saving to new files, or copying files (to name a few). 

  

  Tutorialspoint (n.d.)

  Here is a list of the different modes of opening a file −

  |      |                     Modes & Description                      |
  | :--: | :----------------------------------------------------------: |
  |  1   | **r**<br />Opens a file for reading only. The file pointer is placed at the beginning of the file. This is the default mode. |
  |  2   | **rb**<br />Opens a file for reading only in binary format. The file pointer is placed at the beginning of the file. This is the default mode. |
  |  3   | **r+**<br />Opens a file for both reading and writing. The file pointer placed at the beginning of the file. |
  |  4   | **rb+**<br />Opens a file for both reading and writing in binary format. The file pointer placed at the beginning of the file. |
  |  5   | **w<br />**Opens a file for writing only. Overwrites the file if the file exists. If the file does not exist, creates a new file for writing. |
  |  6   | **wb**<br />Opens a file for writing only in binary format. Overwrites the file if the file exists. If the file does not exist, creates a new file for writing. |
  |  7   | **w+**<br />Opens a file for both writing and reading. Overwrites the existing file if the file exists. If the file does not exist, creates a new file for reading and writing. |
  |  8   | **wb+<br />**Opens a file for both writing and reading in binary format. Overwrites the existing file if the file exists. If the file does not exist, creates a new file for reading and writing. |
  |  9   | **a<br />**Opens a file for appending. The file pointer is at the end of the file if the file exists. That is, the file is in the append mode. If the file does not exist, it creates a new file for writing. |
  |  10  | **ab**<br />Opens a file for appending in binary format. The file pointer is at the end of the file if the file exists. That is, the file is in the append mode. If the file does not exist, it creates a new file for writing. |
  |  11  | **a+<br />**Opens a file for both appending and reading. The file pointer is at the end of the file if the file exists. The file opens in the append mode. If the file does not exist, it creates a new file for reading and writing. |
  |  12  | **ab+<br />**Opens a file for both appending and reading in binary format. The file pointer is at the end of the file if the file exists. The file opens in the append mode. If the file does not exist, it creates a new file for reading and writing. |

  **Examples**

  1. Appending

     ```python
     f = open("test.txt", "a") #Opens the file if exists, else creates a new file
     f.write("This is appeneded to the end of the file")
     f.close()
     
     f = open("test.txt", "r") #Opens the file as read only
     print(f.read()) #Prints the contents of the file
     ```

  2. Overwriting

     ```python
     f = open("test2.txt", "w") #Opens the file if exists, else creates a new file
     f.write("This has overwritten the files content")
     f.close()
     
     f = open("test2.txt", "r") #Opens the file as read only
     print(f.read()) #Prints the contents of the file
     ```

  3. Updating rows

     ```python
     import csv
     
     with open('./test3') as inf:
         reader = csv.reader(inf.readlines())
     
     with open('./test3', 'w') as outf:
         writer = csv.writer(outf)
         for line in reader:
             if line[1] == '0':
                 writer.writerow(line[0], '1')
                 break
             else:
                 writer.writerow(line)
         writer.writerows(reader)
     ```

  4. Deleting File

     ```python
     import os
     if os.path.exists("test4.txt"):
       os.remove("test4.txt")
     ```

  5. Copying File

     ```python
     from shutil import copyfile
     copyfile(source, destination)
     #The destination location must be writable; otherwise, an IOError exception will be raised.
     #If destination already exists, it will be replaced.
     ```

  

  How have I learned this?

  These are basic skills we should know as these are common tasks that applications will perform. There are many scenarios where it will be useful to implement these techniques.


  ------

  Why have I learned this?

  I have learned this by watching YouTube videos and reading the python documentation to understand how to implement the code. i also looked at examples of where and how we can use file manipulation.


  ------

  What will I do to remember this learning?
  I will continue to practice these skills and find ways to implement file manipulation into my projects.

  ------

  What do I know now, that I did not know before?

  I had already done a fair bit of file manipulation prior to these lessons, thus there isn't anything that comes to mind that I have learned.



Tutorialspoint. (n.d.). *Python - Files I/O*. Retrieved September 12, 2021, from https://www.tutorialspoint.com/python/python_files_io.htm


------


# SDV601 - Week 8 Blog

------

#### <u>APP Modules and packages MVC Files</u>

------

What have I learned?

There was a few things that were covered this week. These included architectural patterns, packages, modules, classes, and a reading on OOP (Object-oriented programming). As we are pretty far into the project, these topics weren't anything new too us. We have used modules/packages in many other tasks as well as using them in other languages such as JavaScript.

Modules/Packages/Libraries are very useful when it comes to performing tasks in any coding languages. These libraries are prewritten code that we can import to increase the overall productivity and optimize the tasks we are performing. The main benefit to using libraries is that it reduces the need to hard code certain tasks. For instance, we can use the module `pandas` to read through a CSV file and create a dataframe from the CSV data. This can be done with a single line of code. However, if we were to hard code this task, this would likely require far more time and lines of code. The idea is that we can use these code libraries to perform the task we like, rather than trying to reinvent the wheel. Below is some examples of how we import libraries:

![](https://i.imgur.com/Khu93ks.png)

OOP is an interesting topic to read up on as its use is has its opinions. A lot of people tend to hate OOP and prefer the functional programming approach. The thing with OOP is that it works really well when done right, but when done wrong can be pretty bad. Whereas, we can take more of a lazy approach with functional programming and still achieve the end goal. OOP tends to have these design patterns that we should follow when performing tasks such as creating classes where we should create constructors. These design patterns include such things as singleton, dependency injection, factory methods, inheritance, abstraction, and so on. Whereas, with functional programming, its just function after function. A key benefit of functional programming is that we can use functions to return values from inside another function. Other key benefits to functional programming is that we can avoid things such as constructors, getters and setters, this statements, inheritance, classes, and more. 

Like I mentioned previously, OOP can be a great way and often intuitive option when done correctly, but might not be the best solution for the given task. In my opinion I prefer the functional route as I tend to perform a lot of the same tasks in fewer lines, while reducing the overall complexity. In doing so, this usually increases the overall reusability of my code.



------

What do I know now, that I did not know before?

There wasn't really anything that was covered that we hadn't already done in the past


------

# SDV601 - Week 9 Blog

------

#### <u>Appending Data</u>

------

What have I learned?

This week I learned about reading a CSV using the `pandas` module then using that data to view it on a graph using the `matplotlib` module. This was pretty straight forward as there was a lot of resources on the internet for performing different tasks, whether it was writing the source of the file inline, or using the `askopenfilename()` method in the `tKinter` module.

Here is two examples of reading a CSV:

```python
my_array = pandas.read_csv('/folder/file.csv') # Reads the file and sets the value of 'my_array' to the data
```

```python
filetypes = (
    ('CSV', '*.csv'),
    ('All files', '*.*')
) # Defining the different filetypes to select from

filename = fd.askopenfilename(
    title='Open a file', # Giving the modal box a title
    initialdir='./geodata/', # Defining the initial folder that will open too
    filetypes=filetypes) # Setting the filetypes to the filetypes variable

if filename is None: # If the user doesnt select a file
    Alert(title='Error', text='Please enter a name')
    temp.destroy()
    return

if filename:# If file exists
    with open(filename): # Opens the file
    	my_array = pandas.read_csv(filename) # Reads the file and sets the value of 'my_array' to the data
```

As we had already used the `matplotlib` module, it was not very difficult to take that data and put it into a graph.


------

How have I learned this?

I learned this by researching into how to use to read CSV files and looking at different code examples. I practiced by creating a simple application that reads the data then puts it into a graph.


------

Why have I learned this?

I believe that I have learned these techniques as they are basic skills that we will use when it comes to writing code for later tasks and assessments. As we are required to create an application that reads data from a CSV, it seems logical that we would use a package such as `pandas` to perform the tasks rather than hard coding a script to read a CSV file.


------

What will I do to remember this learning?
I will continue to practice and look at other code examples, implementing these learned skills into the tasks. I will also use these skill where necessary in our projects to come.

------

What do I know now, that I did not know before?

- How to use the `askopenfilename()` method
- Different ways of reading a CSV
- How to write to a CSV


------

# SDV601 - Week 10 Blog

------

#### <u>Milestone Two Work</u>

------

This weeks focus was finalizing my work on milestone two of the assessment. I was getting close to finishing what was required of the assessment and was fixing up minor bugs, proof reading my code, commenting code, and changing variable and function names to follow the coding standards. There wasn't much in the way of learning this week as my focus was getting the aspects of my application finished.

I decided that I wanted to make a start on some features that would be present in the following milestone. These included such things as the upload and download features. Currently I am using MySQL, but may look into other methods of data storage such as MongoDB if I can't set up a remote SQL server.

**Below is my method for uploading data:**

This method defines two variables, data_dictionary and data_arr of which are referenced to variables in the global scope. I then call the `GetData()` method from the Data class and set the returned values to a local variable called "values." The GetData method returns two values of which we append the first value to data_arr and set data_dictionary to the second value. We then perform a for loop which generates the banners on the screen which will display the records to the user. These banners allow the user to click a button that opens a data view screen specific to that record in the table.

```python
class DataListScreen(Screen):    
    def upload_file(root, self):
        """[Data reader for uploading a csv file and generating the list of data calling the banner method]

        Args:
            root ([screen]): [the base screen of which the widgets are being added to]
        """
        global data_arr
        global data_dictionary
        
        values = Data.GetData(self, root, data_dictionary)
        if values == None:
            return
        else:
            data_arr.append(values[0])
            data_dictionary = values[1]
        for publicID, value  in data_dictionary.items():    
            if value[0] == "eventtype" or value[0] == "publicid":
                continue
            else:
                record = value
                magnitude = value[5]
                root.ids["grid_banner"].add_widget(Banner(title=publicID, operation=magnitude, root=root, record=record))
                pass
```



**Below is the GetData method:**

This uses the `askopenfilename()` method so that the user can select a CSV file from their local machine. If the user does not select a file, it will display an alert message saying "Please select a file." If a file is selected, we set a local variable called reader_ and set its value to the values read from the file using the `csv.reader()` method. A for loop then cycles through each row of the variable and updates the values in our data dictionary. We then create a data frame from the same CSV file for other uses. Both the data_arr and the data_dictionary variables are returned.

```python
def GetData(root, self, data_dictionary):
    """[The method for reading the data from the csv file]

    Args:
        root ([screen]): [the base screen of which the widgets are being added to]
        data_dictionary ([dictionary]): [the dictionary of data that we will add too when we retrieve data]

    Returns:
        [type]: [description]
    """        
    temp = Tk()
    temp.wm_state('iconic')
    
    filetypes = (
        ('CSV', '*.csv'),
        ('All files', '*.*')
    )

    filename = fd.askopenfilename(
        title='Open a file',
        initialdir='./geodata/',
        filetypes=filetypes)
    
    if filename is None:
        Alert(title='Error', text='Please select a file')
        temp.destroy()
        return
    
    if filename:
        with open(filename):
            reader_ = csv.reader(open(filename, 'r'), delimiter=',', quotechar='"')
            for row in reader_:
                data_dictionary.update({row[0]: [
                    row[1], row[2], row[3], row[4], row[5], row[6], row[7], row[8], row[9], row[10], row[11], row[12], row[13], row[14], row[15], row[16], row[17], row[18], row[19], row[20]
                ]})
                
            data_arr = pd.read_csv(filename)
            temp.destroy()
            return data_arr, data_dictionary
    else:
        Alert(title='Error', text='Please select a file')
        temp.destroy()
        return
```

**Downloading Data:**

The method for downloading the data wasn't as extensive as uploading it. All that was required was to use the `asksaveasfile()` method and use the file that is created to write too. We do this by using the pandas library to concatenate the data frames in the dataframe variable. This was done as when we upload the data, they are stored in an array as separate data frames (This will be changed though). We then convert the dataframe variable to a CSV file. 

```python
def download_file(root, self, data_arr):
    """[The method for merging and downloading the data to a csv file]

    Args:
        root ([screen]): [the base screen of which the widgets are being added to]
        data_arr ([array]): [the array in which the data is stored]
    """        
    temp = Tk()
    temp.wm_state('iconic')
    if (len(data_arr) <= 0):
        Alert(title='Error', text='No data to download')
    else:
        file = asksaveasfile(mode='w', defaultextension='.csv', filetypes=[("All Files","*.*"),("CSV Documents","*.csv")])
        if file is None:
                Alert(title='Error', text='Please screen a file')
                temp.destroy()
                return
        else:
            dataframe = pd.concat(data_arr)
            dataframe.to_csv(file, header=True, index = False, sep=',', encoding='utf-8', line_terminator='\n')
            temp.destroy()
```

Overall there wasn't really anything to learn here as it was just a process of getting the code finished. There will definitely be learning done in the future to improve this code and change the methods in which methods perform their tasks. There is definitely room for improvement and better ways of performing these tasks. I believe that this is a good learning experience as I am trying different ways of performing tasks, while still achieving the same end goal.


------

# SDV601 - Week 11 Blog

------

#### <u>Connecting to an http (JSON) API</u>

------

What have I learned?

This week I learned about sending data to and from JSNDrop with different URL strings. Like the name suggests, the data that is sent and is received is in a JSON format. This is a simple and useful way to store data in a remote storage from anywhere.

Below is some examples of the different methods we can use:

**CREATE** - Creates a table

`https://newsimland.com/~todd/JSON/?tok={"tok":"Y O U R T O K E N GOES HERE","cmd":{"CREATE":"tblTest","EXAMPLE":{"PersonID PK":"Todd","Score":21}}}`

**STORE** - Stores data in a table

`https://newsimland.com/~todd/JSON/?tok={"tok":"Y O U R T O K E N GOES HERE","cmd":{"STORE":"tblTest","VALUE":[{"PersonID":"Todd","Score":21},{"PersonID":"Jane","Score":2000}]}}`

**ALL** - Selects all data from the table

`https://newsimland.com/~todd/JSON/?tok={"tok":"Y O U R T O K E N GOES HERE","cmd":{"ALL":"tblTest"}} `

**SELECT** - Selects data based on a clause

`https://newsimland.com/~todd/JSON/?tok={"tok":"Y O U R T O K E N GOES HERE","cmd":{"SELECT":"tblTest","WHERE":"Score > 200"}}`

**DELETE** - Deletes data from a table based on a clause

`https://newsimland.com/~todd/JSON/?tok={"tok":"Y O U R T O K E N GOES HERE","cmd":{"DELETE":"tblTest","WHERE":"PersonID = 'Jane'"}}`

**DROP** - Drops the table from the database

`https://newsimland.com/~todd/JSON/?tok={"tok":"Y O U R T O K E N GOES HERE","cmd":{"DROP":"tblTest"}}`

## Assessment ~ 

I managed to implement it into python so that I could pass a JSON object to the database as well as pull the data from the table. Below is how I did this:

**STORE**

```python
def UploadData(root, self, data):
	json_data = data.to_json(orient='records')[1:-1] # Converts the data to JSON
	url = 'https://newsimland.com/~todd/JSON/?tok={"tok":"fc82391c-71b3-4134-91b2-6a40f6b28a94","cmd":{"STORE":"sdv_data_daniel","VALUE":			['+ str(json_data) +']}}' # Defines the URL that we will pass with the json_data as the "VALUE"
    r = requests.get(url) # Uses the get method passing the url as a paramater
```

**ALL**

```python
    def RetireveData(self):
        url = 'https://newsimland.com/~todd/JSON/?tok={"tok":"fc82391c-71b3-4134-91b2-6a40f6b28a94","cmd":{"ALL":"sdv_data_daniel"}}'
        r = requests.get(url) # Request Data From Url
        data = r.json() # Defines data as the respons
        data = json.dumps(data['Msg']) # Convert data to JSON object
        df = pd.read_json(data)# Convert json to dataframe
```


------

How have I learned this?

I have learned this by following the steps provided to us on Moodle and testing if it works


------

Why have I learned this?

- A simple way of storing data in a remote database
- An alternative to options such as MySQL, Firebase, and MongoDB
- Will be useful for future tasks such as milestone three


------

What will I do to remember this learning?

- I will practice using this method
- Try and implement it into my code

------

# SDV601 - Week 12 Blog

------

#### <u>How to read a CSV file from a URL with Python?</u>

------

What have I learned?

This week I learned about reading a CSV file from a URL using Python. This was a pretty straight forward task.

There are a few different methods that we can achieve this, as shown by ExceptionsHub (2018), but the most concise method I found is as follows:

```python
import pandas as pd
data = pd.read_csv('http://winterolympicsmedals.com/medals.csv')
print(data)

Returns:
      Year      City       Sport      Discipline  NOC            Event Event gender   Medal
0     1924  Chamonix     Skating  Figure skating  AUT       individual            M  Silver
1     1924  Chamonix     Skating  Figure skating  AUT       individual            W    Gold
2     1924  Chamonix     Skating  Figure skating  AUT            pairs            X    Gold
3     1924  Chamonix   Bobsleigh       Bobsleigh  BEL         four-man            M  Bronze
4     1924  Chamonix  Ice Hockey      Ice Hockey  CAN       ice hockey            M    Gold
...    ...       ...         ...             ...  ...              ...          ...     ...
2306  2006     Turin      Skiing       Snowboard  USA        Half-pipe            M  Silver
2307  2006     Turin      Skiing       Snowboard  USA        Half-pipe            W    Gold
2308  2006     Turin      Skiing       Snowboard  USA        Half-pipe            W  Silver
2309  2006     Turin      Skiing       Snowboard  USA  Snowboard Cross            M    Gold
2310  2006     Turin      Skiing       Snowboard  USA  Snowboard Cross            W  Silver
```


------

How have I learned this?

I have learned this by looking at tutorials online and following the steps to execute methods that read CSV files from a URL. I have practiced using the different types and how to implement them. 


------

Why have I learned this?

Python is a well used language when it comes to data analysis. Being able to read a CSV file from a URL rather than requiring the user to download the file or for us to create our own data source such as JSON drop removes the repetition of data. By doing this, we can eliminate the middleman and read directly from the sources. Another benefit is if the data source is added to or updated, we do not need to redownload the data or update the data in our remote storage.


------

What will I do to remember this learning?
I will continue to practice these techniques and find areas where I can implement this knowledge.

------

What is the point?

As stated before, we can pull the data directly from its source rather than using up unnecessary space in our own remote storage. This data will always remain up to date when the source is updated. This is a useful alternative to downloading the CSV and reading it from there.

------

What do I know now, that I did not know before?

- How to read a CSV file from a URL
- That the pandas library can use the `read_csv()` method to read from a URL, not just a local file

------

# SDV601 - Week 13 Blog

------

#### <u>Threading</u>

------

This week I focused on finalizing my project and further improving the code where I could. The main focus was improving my chat thread. The problem I was having was that it would crash from time to time when I would close one DES, then open up another. I took a look at my code and read up on some documentation on Python threading. 

The main change I made was creating an if statement containing a global variable that would be checked every time the thread would loop through the function. By default, this would be set to false. This method is as follows:

```python
def chat_thread(self, session_id, window,):
        while True:
            Data.RetrieveMessages(self, app=App, session=session_id, window=window)
            global thread_status
            
            if thread_status:
                print('Chat thread has stopped')
                break
            
            print ('Chat has updated\n')
            time.sleep(2)
```

The value of `thread_status` is set prior to the chat thread running. In the case that `thread_status` is set to True, we break from the loop.

I set up a method that waits for the window event shown below. If this is detected, `thread_status` is set to True, causing it to be read as True the next time the thread method loops. We then use the `join()` method to terminate the thread.

```python
            if event in (sg.WIN_CLOSED, '_EXIT_'):
                thread_status = True
                t2.join()
                window.close()
                break
```

This subtle difference greatly improved the reliability of the application. In saying this, I cant guarantee that it will run as smoothly on my laptop as it has far less specs than my home PC. 

Another issue I was having was that there would be a delay from clicking the close button before the form would close. The reason this was happening is because the `time.sleep(2)` every time the loop was running. This meant that even if the thread was terminated, It would still run through the loop one last time. By adding `time.sleep(2)` at the end of the loop after the `if` statement, this removed the delay. If I were to have the sleep at the start of the loop, it would pause before checking the value of `thread_status.`

