# Using GitHub for Social Data Science: Best Practise Guidelines

This document sets out the best practise guidelines for using GitHub for the Social Data Science Course at the Oxford Internet Institute.

**I recommend that you create you own personal GitHub repository to makesure all of your code is backed up and tracked.**

It is important that the structure of the *Organisation* is maintained for the sake of consistency across years and courses. 
The structure of the materials are laid out in the diagram below.

<img src="Images/Organisation_Structure.PNG" height=400>

## Code Formatting
These guidelines are generally for Python, but the principles hold accross R and other programming languages you might use in your time at the Oxford Interent Institute.

### The Zen of Python
Tim Peters (major contributor to the Python) wrote this short poem to express what values you should follow while coding in Python. You can get this by running “import this” in the IDLE:
``` Python
import this
```
The principle to always remember is that: **Code is read more than it is written**. 

### Follow Style Guidelines
The PEP8 holds some great community-generated proposals. PEP stands for Python Enhancement Proposals - these are guidelines and standards for development. 
There are other PEPs like the PEP20, but PEP8 is the Python community bible for you if you want to properly style your code. 
This is to make sure all Python code looks and feels the same. 
For example:
- Use proper naming conventions for variables, functions, methods, and more.
- Variables, functions, methods, packages, modules: this_is_a_variable
- Classes and exceptions: CapWords
- Protected methods and internal functions: _single_leading_underscore
- Private methods: __double_leading_underscore
- Constants: CAPS_WITH_UNDERSCORES
- Use 4 spaces for indentation. 
For more conventions, refer to PEP8: https://www.python.org/dev/peps/pep-0008/

#### Use Long and Descriptive Variable Names
Have you noticed anything about the examples above? The names of functions and variables almost always quite long. That’s no coincidence.
It may seem superfluous to use so many characters for a bit of code, but it’s a lot better for reading the code. Besides, it doesn’t take that much longer to code — most editors have autocomplete anyway.

### Comment Well
Make sure you keep your comments short and to-the-point. I like to think about what somebody would like to read if they’d never seen my code but had a look at it now because they wanted to change something. 
Comments are designated with a hash mark (#). Python ignores everything after the hash mark and up to the end of the line. You can insert them anywhere in your code, even inline with other code.

``` python
print("This with Run.") # This won't run.
```
There is a two ways to do multiline comments in python. You can indent hashed on newlines:

``` python
def multiline_example():
    # This is a pretty good example
    # of how you can spread comments
    # over multiple lines in Python
```
Or if you don't want to use multiple hashes:
``` python    
"""
If I really hate pressing `enter` and
typing all those hash marks, I could
just do this instead
"""
```
While this gives you the multiline functionality, this isn’t technically a comment. It’s a string that’s not assigned to any variable, so it’s not called or referenced by your program. Be nice to your fellow devs and use comments to help them skim through your code. Inline comments should be used sparingly to clear up bits of code that aren’t obvious on their own. (Of course, your first priority should be to make your code stand on its own, but inline comments can be useful in this regard.)

#### Avoid W.E.T. Comments
This is taken from the [Real Python Guide] (https://realpython.com/python-comments-guide/). The guide states that comments should be D.R.Y. The acronym stands for the programming maxim **“Don’t Repeat Yourself.”** This means that your code should have little to no redundancy. You don’t need to comment a piece of code that sufficiently explains itself, like the one below:
```python
return a  # Returns a
```
We can clearly see that a is returned, so there’s no need to explicitly state this in a comment. This makes comments W.E.T., meaning you **“wrote everything twice.”** (Or, for the more cynical out there, “wasted everyone’s time.”)
W.E.T. comments can be a simple mistake, especially if you used comments to plan out your code before writing it. But once you’ve got the code running well, be sure to go back and remove comments that have become unnecessary.

#### Avoid Rude Comments (Including Swearing!)
This is something that’s likely to come up when working on a development team. When several people are all working on the same code, others are going to be going in and reviewing what you’ve written and making changes. From time to time, you might come across someone who dared to write a comment like this one:

``` python
# Put this here to fix Sian's stupid f***king mistake

```
It’s just a good idea to not do this. It’s not okay if it’s your friend’s or classmate's code, and you’re sure they won’t be offended by it. You never know who might see it, and how is it going to look if you’d accidentally left that comment in there, and a professor or client discovered it down the road? You’re a professional, and including vulgar words in your comments is not the way to show that.

### Correct Broken Code Immediately
Like with the broken code theory, correct your broken code immediately. If you let it be while you work on something else, it can lead to worse problems later. This is what Microsoft does. It once had a terrible production cycle with MS Word’s first version. So now, it follows a ‘zero defects methodology’, and always corrects bugs and defects before proceeding.

### Write Readable Code
You should use line breaks and indent your code. Use naming conventions for identifiers (Vars)- this makes it easier to understand the code. Use comments, and whitespaces around operators and assignments. Keep the maximum line length 79 characters. You should stay consistent and write readable code.

Some IDE's, like Pycharm, automatically tell you if you are making formatting mistakes.

#### Don’t Write Spaghetti Code
Spaghetti code is a slang term used to refer to a tangled web of programming source code where control within a program jumps all over the place and is difficult to follow. Spaghetti code normally has a lot of GOTO statements and is common in old programs, which used such statements extensively.
But nobody reads a thousand lines of monolithic code…
So make sure that you define functions and call them when necessary. This will make your code a thousand times more readable, and your colleagues will thank you for it.

### Use Virtual Environments
You should create a virtual environment for each project you create. This will avoid any library clashes, since different projects may need different versions of a certain library.
Virtual envs in Python: https://uoa-eresearch.github.io/eresearch-cookbook/recipe/2014/11/26/python-virtual-env/

### Getting Quick Help
Use the **help()** funtion before heading to StackOverflow.
If you’d like to see what a function does, just use help(). This is useful if you know in principle what you’re doing but aren’t too sure about the details of a function.
*You can also make your life easier by adding a help-message to your own functions*. That’s quite easy to do, as shown below.
``` python
>>> def mynewfunction(arg1, arg2):
...     """
...     This function does something really cool.
...     Hope that helps!
...     """
>>> help(mynewfunction)
This function does something really cool.
Hope that helps!
```
This help-message, a docstring, is also useful as a documentation of your code. In this example, you’d obviously need to add a body to the function and flesh the message out a bit. But you get the message.

#### Sources
* https://www.python.org/dev/peps/pep-0008/
* https://towardsdatascience.com/the-ultimate-guide-to-writing-better-python-code-1362a1209e5a
* https://realpython.com/python-comments-guide/


