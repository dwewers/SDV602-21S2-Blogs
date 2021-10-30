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
