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

