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
