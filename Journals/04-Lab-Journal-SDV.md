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

