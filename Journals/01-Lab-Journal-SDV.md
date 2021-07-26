

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
