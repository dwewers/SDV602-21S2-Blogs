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

Calling the method:

```python
if __name__ == "__main__":
    methodName()
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
