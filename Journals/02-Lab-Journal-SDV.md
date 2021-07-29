# SDV601 - Week 2 Blog

------

#### <u>Setting Up the Development Environment, Variables, and Code Convention</u>

------

What have I learned?


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

# Project Brief Continuation

I have decided that the data source I will be using is https://koordinates.com/ .  At this stage, I am looking at using https://koordinates.com/from/data.linz.govt.nz/layer/50804/ which is NZ Property Titles.

Data I can get from this looks like this:

![image-20210729150157543](https://i.imgur.com/av6BXbf.png)

The reason I have chosen the data from this data source is because I believe I can implement it well in a way that matches the criteria of needing too implement features such as zoom and pan. I believe that I can use the data well (such as property ID or coordinates) to plot different points on a graph and identify other key information about that set of data in a quick view.

