# Introduction to Python 2024/2025

Masters in Data Science applied to agricultural and food sciences, environment, and forestry engineering.

Instructor: Manuel Campagnolo (mlc@isa.ulisboa.pt)

<details markdown="block">
<summary> 
 
# Online resources for the course (to be completed)

</summary>
 
* **Required:** [CS50’s Introduction to Programming with Python](https://cs50.harvard.edu/python/2022): lectures (videos and notes), problems sets, shorts; The platform allows you to test your code at the [CS50 codespace](https://cs50.dev/) for the proposed problems (you need to have your own GitHub account to access the codespace).
* Python Programming course at [PP.fi](https://programming-23.mooc.fi/): same features as CS50 but to test your solutions to problems you are required to pass previous tests 
* [Learn Python](https://v2.scrimba.com/learn-python-c03): lectures (videos) and interactive examples and exercises 
* [Introduction to Python (VScode)](https://vscodeedu.com/courses/intro-to-python): interactive lectures and exercises 
* Basic concepts and features of the Python language and system: [The Python Tutorial at python.org](https://docs.python.org/3/tutorial/index.html).
* Fenix webpage for the course (https://fenix.isa.ulisboa.pt/courses/intpy-283463546571610)
* Moodle (https://elearning.ulisboa.pt/course/view.php?id=9100)

<details markdown="block">
  
<summary> 
 
#### Comparison of CS50P and PP.fi

</summary>

| CS50P     | Contents |  PP.fi | Contents |
| ----------- | ----------- |----------- | ----------- |
| Lecture 0    | Creating Code with Python; Functions; Bugs; Strings and Parameters; Formatting Strings; More on Strings; Integers or int; Readability Wins; Float Basics; More on Floats; Def; Returning Values    | Part 1 |   Intro; I/O; More about variables; Arithmetic operations; Conditional statements |
| Lecture 1    | Conditionals, if Statements, Control FlowModulo; Creating Our Own Parity Function; Pythonic; match | Part 2  |  Programming terminology; More conditionals; Combining conditions; Simple loops |
| Lecture 2    | Loops; While Loops; For Loops; Improving with User Input; More About Lists; Length; Dictionaries, More on code modularity  |  Part 3 |  Loops with conditions; Working with strings; More loops; Defining functions |
|  |   | Part 4 |    The Visual Studio Code editor, Python interpreter and built-in debugging tool; More functions; Lists; Definite iteration; Print statement formatting; More strings and lists |
|   |   | Part 5 |  More lists; References; Dictionary; Tuple |
| Lecture 3 | Exceptions, Runtime Errors, try, else, Creating a Function to Get an Integer, pass | Part 6  |  Reading files; Writing files; Handling errors; Local and global variables |
| Lecture 4 |  Libraries, Random, Statistics, Command-Line Arguments, slice, Packages, APIs, Making Your Own Libraries|  Part 7 | Modules; Randomness; Times and dates; Data processing; Creating your own modules; More Python features  |
| Lecture 5 | Unit Tests; assert; pytest; Testing Strings; Organizing Tests into Folders | | |
| Lecture 6| File I/O; open; with; CSV; Binary Files and PIL | | |
| Lecture 7 | Regular Expressions; Case Sensitivity; Cleaning Up User Input; Extracting User Input |||
| Lecture 8 | Object-Oriented Programming; Classes; raise; Decorators;  Class Methods; Static Methods; Inheritance; Inheritance and Exceptions; Operator Overloading| Part 8 | Objects and methods; Classes and objects; Defining classes; Defining methods; More examples of classes |
| | | Part 9 | Objects and references; Objects as attributes; Encapsulation; Scope of methods; Class attributes; More examples with classes |
| | | Part 10 | Class hierarchies; Access modifiers; Object oriented programming techniques; Developing a larger application |
| Lecture 9 | set; Global Variables; Constants; Type Hints; Docstrings; argparse; Unpacking; args and kwargs; map; List Comprehensions; filter; Dictionary Comprehensions; enumerate; Generators and Iterators | Part 11 |  List comprehensions; More comprehensions; Recursion; More recursion examples |
| | | Part 12 | Functions as arguments; Generators; Functional programming; Regular expressions|

</details>
</details>

<details markdown="block">
<summary> 
 
# Class 1 (September 13, 2024): data types, variables, functions

</summary>
 
1. Install Python and VS code: https://code.visualstudio.com/docs/python/python-tutorial. Alternatively, you can code in the CS50 cloud environment (VScode). Two steps: 1. log in into your github account; 2. access your code space at https://cs50.dev/. This environment allows you to test automatically your scripts for the CS50 problem sets.
2. Some useful keyworks for the command line interface (CLI) in terminal: 
 * `code filename.py` to create a new file 
 * `ls` to list files in folder
 * `cp filename newfilename` to copy a file, e.g. `cp ..\hello.py  farewell.py` (`..` represents parent folder)
 * `mv filename newfilename` to rename or move file, e.g. `my farewell.py goodbye.py` or `mv farewell.py ..` (move one folder up)
 * `rm filename` to delete (remove) file
 * `mkdir foldername` to create new folder
 * `cd foldername` change directory, e.g. `cd ..` 
 * `rmdir foldername` to delete folder
 * `clear` to clear terminal window
3. The REPL (interactive Read -Eval-Print-Loop) environment: see https://realpython.com/interacting-with-python/
4. All values in Python have a **type**. The five basic types are: integer, float, string, Boolean, and None.
   * strings (`str`), variables, print (a function), parameters (e.g. `end=`), input, comments, formatted strings (`f"..."`), `.strip()`, `.title` (methods)
   * integers (`int`), operations for integers, casting (e.g. `str`to `int`)
   * floating point values (`float`), round, format floats (e.g. `f"{z:.2f}`)
   * `True`, `False`, `and`, `or`, `not`
5. Functions, `def`, `return`
6. Suggested problems: [CS50 Problem set 0](https://cs50.harvard.edu/python/2022/psets/0/)
</details>

<details markdown="block">
 
<summary> 

# Class 2 (September 20, 2024): conditionals, lists, dictionaries

</summary>

1. Conditionals:
  - `if`, `elif`, `else`:
    ```
     if score >= 70:
         print("Grade: C to A")
     elif score >= 60:
         print("Grade: D")
     else:
         print("Grade: F")
     ```
  - `match`:
    ```
    match species:
        case 'versicolor':
            label=0
        case 'virginica'
            label=1
        case _:
            label=2
    ```
4. Pythonic coding: `def main()`, define other functions, call `main()`. The code must be modular.
5. While loops, for loops, `break`, `break` and `return`
6. Data type *list* `[]`: methods `append`, `extend`
7. Data type *dictionary* `{}`, `items()`, keys `.key()` and values `.values()`
   ```
   knights = {'gallahad': 'the pure', 'robin': 'the brave'}
   for k, v in knights.items():
       print(k, v)
   if 'gallahad' in knights:
       print('Go Gallahad')
   ```
9. Suggested problems: [CS50 Problem set 1 and 2](https://cs50.harvard.edu/python/2022/psets/). See the assignment on Moodle: problems [File extensions](https://cs50.harvard.edu/python/2022/psets/1/extensions/), [Coke machine](https://cs50.harvard.edu/python/2022/psets/2/coke/), [Plates](https://cs50.harvard.edu/python/2022/psets/2/plates/)

</details>

<details markdown="block">
 
<summary> 

# Class 3 (September 27, 2024): exercises, best practices

</summary>

Exercises from [CS50 Problem set 0, 1 and 2](https://cs50.harvard.edu/python/2022/psets/).

</details>

<details markdown="block">
<summary> 

# Class 4 (October 4, 2024): handling exceptions

</summary>

Handling exceptions in Python: raising and catching exceptions. 

1. Example from (https://cs50.harvard.edu/python/2022/shorts/handling_exceptions/). Exercise: adapt the proposed code to be more modular, where the main function is something like the one below:

```
def main():
    spacecraft = input("Enter a spacecraft: ")
    au=get_au(spacecraft)
    m = convert(au)
    print(f"{m} m")
```

2. Exercises from [CS50 Problem set 3](https://cs50.harvard.edu/python/2022/psets/3/).

For the *fuel gauge* problem (https://cs50.harvard.edu/python/2022/psets/3/fuel/), try to organize your code as follows. As suggested in *hints*, you should catch `ValueError` and  `ZeroDivisionError` exceptions in your code. In the code below, the user is being asked for correct values for `x,y` until they satisfy the requirements: `x,y` must be inputted as a string `x/y`, `x` has to be less or equal to `y`, and `y` cannot be zero. The function `get_string_of_integers_X_less_than_Y` in the code below should take care of that.

```
def main():
    # asks user for input until the input is as expected
    x,y=get_string_of_integers_X_less_than_Y()
    # compute percentage from two integers
    p=compute_percentage(x,y)
    # print output 
    print_gauge(p)
```

3. A few examples of code that can be helpful to solve problems in problem set 3:

Example of basic use of `try-except` to catch a `ValueError`:
```
try:
    x = int(input("What's x?"))
except ValueError:
    print("x is not an integer")
else:
    print(f"x is {x}")
```

Function for requesting an integer from the user until no exceptions are caught:
```
def get_int():
    while True:
        try:
            x = int(input("What's x?"))
        except ValueError:
            print("x is not an integer")
        else:
            break
    return x
```

We may want to exit the execution of our script if some exception is caught. This can be done with `sys.exit()`, which can also be used to print a message.
```
import sys # import module
try:
    x = int(input("What's x?"))
except ValueError:
    sys.exit("x is not an integer")
```

Example of code that catches `CRTL-C` or `CRTL-D`:

```
while True:
    try:
        x=int(input())
    except ValueError:
        print('x is not integer')
    except KeyboardInterrupt: #CTRL-C
        print('\n KeyboardInterrupt')
        break
    except EOFError: # CTRL-D
        print('\n EOFError')
        break
    else:
        print(x)
```

For a list of Python Built-in Exceptions, you can explore (https://www.w3schools.com/python/python_ref_exceptions.asp)
</details>

<details markdown="block">
<summary> 

# Class 5 (October 11, 2024): libraries, modules, APIs

</summary>

1. (modules) You can store your own functions in modules (which are just python scripts) and `import` then into your main code. Let's imagine you created a file named `mymodule.py` in a given folder. In your main script, you can import the file if the folder belongs to list of folders the Python interpreter will look for. You can check that by running the following lines of codes in the Python interpreter:
```
>>>import sys
>>>sys.path
```
If the folder where `mymodule.py` was created does not belong to that list, you can add it with `sys.path.append` which allows you to import your module. To that end, you can include the followings lines to your main script:
```
import sys
sys.path.append(r'path-to-folder') # folder where mymodule is
import mymodule
```
where `path-to-folder` is the path that you can easily copy in your IDE. 

If your module includes a function named, say,  `get_integer`, you can then use the function in your main script either by calling `mymodule.get_integer()` or you can instead load the function with `from mymodule import get_integer` and then just call it with `get_integer()` in the main script as in the following script.
```
import sys
sys.path.append(r'/workspaces/8834091/modules') # where file mymodule.py is
from mymodule import get_integer
def main():
    x=get_integer()
    print(x)
main()
```

Often, you import a module that is available at (https://pypi.org/project/pip/). Say you want to load the module `random` which provides a series of functions for sampling, shuffling, and extracting random numbers from a variety of probability distributions. If the module is not already available, you can typically load it in your terminal with 
```
$pip install random
```
and then import it on your main script with `import random`. If you want to know which is the folder where the module is located, you can get that information with `random.__file__`.

2. (`sys.argv`) Previously, we used module `sys`, in particular functions  `sys.exit()` and  `sys.path`. Another useful function is `sys.argv`,  that allows you to have access to what the user typed in at the command line `$` as in 
```
import sys
print(len(sys.argv)) # returns the number of words in the command line after $python
print(sys.argv[1]) # returns the 2nd word, i.e., the first word after $python myscript.py
```

For instance, the following script named `sum.py` prints the sum of two numbers that were specified in the command line with `$python sum.py 1.2 4.3`:
```
import sys
try:
    x,y = float(sys.argv[1]), float(sys.argv[2])
    print('the sum is',x+y)
except IndexError:
    print('missing argument')
except ValueError:
    print('The arguments are not numbers')
```
3. (APIs) *application program interfaces* allow you to communicate with a remote server. For instance,  `requests` is a package that allows your program to behave as a web browser would.  Consider the following script `myrequest.py` that allows you to explore the *itunes* database (https://performance-partners.apple.com/search-api):
```
import requests
import sys
try:
    response = requests.get("https://itunes.apple.com/search?entity=song&limit=1&term=" + sys.argv[1])
    print(response.json())
except IndexError:
    sys.exit('Missing argument')
except requests.RequestException:
   sys.exit('Request failed')
```
You can easily adapt that code to access a different database. For instance if you want to explore the GBIF database (https://data-blog.gbif.org/post/gbif-api-beginners-guide/), you can just replace the main line of code in `myrequest.py` with
```
response=requests.get('https://api.gbif.org/v1/species/match?name='+ sys.argv[1])
```
and execute it with, say,  `$python myrequest.py Tracheophyta` in the terminal.

There are many ways of running an API in Python. The following example shows how you can access satellite imagery through the *Google Earth Engine* API and compute the mean land surface temperature at some location from the MODIS11 product. To be able to use the API, you need to have a Google account, and an earth engine project associated to it.
```
# pip install earthengine-api
import ee
# Trigger the authentication flow.
ee.Authenticate()
# Initialize the library.
ee.Initialize(project='project-name') # e.g. 'ee-my-mlc-math-isa-utl'
# Import the MODIS land surface temperature collection.
lst = ee.ImageCollection('MODIS/006/MOD11A1')
# Selection of appropriate bands and dates for LST.
lst = lst.select('LST_Day_1km', 'QC_Day').filterDate('2020-01-01', '2024-01-01')
# Define the urban location of interest as a point near Lyon, France.
u_lon = 4.8148
u_lat = 45.7758
u_poi = ee.Geometry.Point(u_lon, u_lat)
scale = 1000  # scale in meters
# Calculate and print the mean value of the LST collection at the point.
lst_urban_point = lst.mean().sample(u_poi, scale).first().get('LST_Day_1km').getInfo()
print('Average daytime LST at urban point:', round(lst_urban_point*0.02 -273.15, 2), '°C')
```

4. Solve problems from CS50P [Problem_set_4](https://cs50.harvard.edu/python/2022/psets/4/). In particular, for problem *Bitcoin price index* organize your code so the main function is the following:

```
def main():
    x=read_command_line_input()
    price=get_bitcoin_price()
    print(f"${x*price:,.4f}")
```

</details>


<!---
#####################################################################################  last year and suggestions for this year
Assignments:
1. Functions, variables, conditionals, loops
[File extensions](https://cs50.harvard.edu/python/2022/psets/1/extensions/)
[Coke machine](https://cs50.harvard.edu/python/2022/psets/2/coke/)
[Nutrition facts](https://cs50.harvard.edu/python/2022/psets/2/nutrition/): dictionaries; loop

2. Exceptions, Libraries (e.g. random), venv?
[Little professor](https://cs50.harvard.edu/python/2022/psets/4/professor/)
[Bitcoin Price Index](https://cs50.harvard.edu/python/2022/psets/4/bitcoin/): api

3. OOP
[Seasons of Love](https://cs50.harvard.edu/python/2022/psets/8/seasons): datetime
[Cookie Jar](https://cs50.harvard.edu/python/2022/psets/8/jar/)

4. numpy and pandas, etc (file I/O; regex?; 


## Class contents:

<details markdown="block">
<summary> Class 1 (September 15, 2023): Install Python and VSCode; first examples; strings</summary>
 
1. [CS50P](https://cs50.harvard.edu/python/2022/weeks/0/), Section on "Functions, Variables"
   * **Do before next class.** [Visual Code for CS50P](https://cs50.harvard.edu/python/2022/shorts/visual_studio_code_for_cs50/)
    
2. Some useful keyworks for the command line interface in terminal:
* `code filename.py` to create a new file 
* `ls` to list files in folder
* `cp filename newfilename` to copy a file, e.g. `cp ..\hello.py  farewell.py` (`..` represents parent folder)
* `mv filename newfilename` to rename or move file, e.g. `my farewell.py goodbye.py` or `mv farewell.py ..` (move one folder up)
* `rm filename` to delete (remove) file
* `mkdir foldername` to create new folder
* `cd foldername` change directory, e.g. `cd ..` 
* `rmdir foldername` to delete folder
* `clear` to clear terminal window

3. [CS50P](https://cs50.harvard.edu/python/2022/weeks/0/), Section on "Functions, Variables"
   * Notes: [Lecture 0](https://cs50.harvard.edu/python/2022/notes/0/)
    Creating Code with Python; 
    Functions; 
    Bugs; 
    Improving Your First Python Program:
        Variables,
        Comments,
        Pseudocode;
    Further Improving Your First Python Program;
    Strings and Parameters; 
        A small problem with quotation marks;
    Formatting Strings;
    More on Strings.

   
   * **Do before next class.** Video on [CS50 Video Player](https://video.cs50.io/JP7ITIXGpHk) or [YouTube](https://youtu.be/JP7ITIXGpHk): follow video and recreate exercises on VS Code up to 59' approximately (up to the section on integers 'int').

</details>

<details markdown="block">

 <summary> Class 2 (September 22, 2023): Floats; Conditionals; ...</summary>

1. Questionnaire Q0 (test) on the topics of the previous class;
2. Work on [Problem set 0](https://cs50.harvard.edu/python/2022/psets/0/): "indoor voice", "playback speed", and "making faces". For this last one, check [the emoji chart](https://unicode.org/emoji/charts/full-emoji-list.html) and follow the instructions: Every emoji has a unique Unicode assigned to it. When using Unicode with Python, replace "+" with "000" from the Unicode. And then prefix the Unicode with "\\". For example, "U+1F605" will be used as "\U0001F605". But there are alternative ways to encode emojis in your Python code: check [this link](https://www.makeuseof.com/how-to-include-emojis-in-your-python-code/)
4. **Do before next class.** Complete [Lecture 0](https://cs50.harvard.edu/python/2022/notes/0/) and video [CS50 Video Player](https://video.cs50.io/JP7ITIXGpHk) until the end, on the following topics: Integers or int; Readability Wins; Float Basics; More on Floats; Def; Returning Values
5. **Do before next class.** Study [Lecture 1](https://cs50.harvard.edu/python/2022/notes/1/) up to "Modulo" and watch video  [CS50 Video Player: Lecture 1](https://video.cs50.io/_b6NgY_pMdw) up to approximately 34' on the topics: Conditionals, if Statements, Control Flow, or, and.

**All topics to prepare before next class**: *Integers or int; Readability Wins; Float Basics; More on Floats; Def; Returning Values; Conditionals, if Statements, Control Flow, or, and, How to organize a program with `main()` and auxiliary functions.*

</details>

<details markdown="block">

 <summary> Class 3 (September 29, 2023): Loops; Lists; ...</summary>


1. Questionnaire Q1 on the topics of the homework;
2. Work on [Problem set 0](https://cs50.harvard.edu/python/2022/psets/0/): Einstein. Work on [Problem set 1](https://cs50.harvard.edu/python/2022/psets/1/): The Hitchhiker’s Guide to the Galaxy's Deep Thought, Home Federal Savings Bank, File Extensions.
5. **Do before next class.** Study the remainder of [Lecture 1](https://cs50.harvard.edu/python/2022/notes/1/) starting at "Modulo" and watch video  [CS50 Video Player: Lecture 1](https://video.cs50.io/_b6NgY_pMdw) after 34'.
6. **Do before next class.** Study [Lecture 2](https://cs50.harvard.edu/python/2022/notes/2/) up to "More about lists" and "Length" and watch video  [CS50 Video Player: Lecture 2](https://video.cs50.io/-7xg8pGcP6w) up to approximately 45'.
7. **Do before next class.** Try solving problems from [Problem Set 2](https://cs50.harvard.edu/python/2022/psets/2/): Camel; Coke Machine; Just setting up my twttr

**Topics to prepare before next class**: *Modulo; Creating Our Own Parity Function; Pythonic; match, Loops; While Loops; For Loops; Improving with User Input; More About Lists; Length*



</details>

<details markdown="block">

 <summary> Class 4 (October 6, 2023): Dictionaries; Functions; ...</summary>

1. Questionnaire Q2 on the topics of the homework;
2. Work on problems from [Problem Set 2](https://cs50.harvard.edu/python/2022/psets/2/): Camel; Coke Machine; Just setting up my twttr (P1: submit in Fenix one of those problems to be indicated in class)
6. **Do before next class.** Study remainder of [Lecture 2](https://cs50.harvard.edu/python/2022/notes/2/)  watch video  [CS50 Video Player: Lecture 2](https://video.cs50.io/-7xg8pGcP6w) starting at Dictionaries (~45').
7. **Do before next class.** [Lecture 3](https://cs50.harvard.edu/python/2022/notes/3/) and video [CS50 Video Player: Lecture 3](https://video.cs50.io/LW7g1169v7w)
8. **Do before next class.** Try solving problems from [Problem Set 3](https://cs50.harvard.edu/python/2022/psets/3/). Note: for the "Taqueria" problem: EOFError is the error raised by "CRTL-D" in Mac and "CTRL-Z" in Windows.
   
**Topics to prepare before next class**: *Dictionaries, More on code modularity (Mario example), Exceptions, Runtime Errors, try, else, Creating a Function to Get an Integer, pass*


</details>

<details markdown="block">

 <summary> Class 5 (October 13, 2023):  Libraries; … </summary>


1. Questionnaire Q3 on the topics of the homework 
2. Work on problems from [Problem Set 3](https://cs50.harvard.edu/python/2022/psets/3/).
7. **Do before next class.** [Lecture 4](https://cs50.harvard.edu/python/2022/notes/4/) and video [CS50 Video Player: Lecture 4](https://video.cs50.io/MztLZWibctI)
8. **Do before next class.** Try solving problems from [Problem Set 4](https://cs50.harvard.edu/python/2022/psets/4/). Try problem "Guessing Game" (not hard) and "Little Professor" (group assignment). For the group assigment, the goal is to fill the missing code in [professor_incomplete.py](https://github.com/isa-ulisboa/greends-ipython/blob/main/assignments/professor_incomplete.py). The completed code should pass the correctness test in [https://cs50.dev/](https://cs50.dev/).
   
**Topics to prepare before next class**: *Libraries, Random, Statistics, Command-Line Arguments, slice, Packages, APIs, Making Your Own Libraries*



</details>

<details markdown="block">

 <summary>Class 6 (October 20, 2023): Organizing and testing code; Unit tests</summary>


1. Questionnaire Q4 on the topics of the homework 
2. Evaluated group assignment ("Little Professor") in class
3. Discussed references in Python with examples from Part 5 of [PP.fi](https://programming-23.mooc.fi/) and made experiments with PythonTutor: [Visualize code](https://pythontutor.com/visualize.html#mode=edit).
4. **Do before next class.** Some groups still have to improve the previous assignment. All groups should solve Problem P3 (also a group assigment):
   - [P3_distances description and file](https://github.com/isa-ulisboa/greends-ipython/tree/main/assignments/P3_distances)
   - Groups members should try to collaborate by syncronizing their work through VSCode and GitHub using the Source Control menu in VSCode:
    * [Working with GitHub in VS Code (VSCode documentation)](https://code.visualstudio.com/docs/sourcecontrol/github)
    * Notes on [how to clone GitHub repository and syncronize it with local folder](https://github.com/isa-ulisboa/greends-ipython/blob/main/github_vscode/Clone_GitHub_repository_and_syncronize_with_local_folder.pdf)
    * Notes on [how to publish a local folder to GitHub](https://github.com/isa-ulisboa/greends-ipython/blob/main/github_vscode/VSCode_local_folder_to_GitHub.pdf)

</details>

<details markdown="block">

 <summary>  Class 7 (October 27, 2023):  File I/O</summary>


1. Questionnaire Q5 on recent topics 
2. Evaluate group assignment P3 ("Distances") in class
3. Unit tests with `pytest`: examples 
4. **Do before next class (November, 11).**
   * [Lecture 5 on Unit tests](https://cs50.harvard.edu/python/2022/notes/5/) and video [CS50 Video Player: Lecture 5](https://video.cs50.io/tIrcxwLqzjQ)
   * Group assignment, which is mostly about creating unit tests for code. Groups members should collaborate through VSCode and GitHub using Source Control menu in VSCode or git command lines. The problem description and the necessary files are available at [P4_haversine](https://github.com/isa-ulisboa/greends-ipython/tree/main/assignments/P4_haversine).
   * [Lecture 6 on File I/O](https://cs50.harvard.edu/python/2022/notes/6/) and video [CS50 Video Player: Lecture 6](https://video.cs50.io/KD-Yoel6EVQ)

</details>

<details markdown="block">

<summary> Class 8 (November 10, 2023): Pandas </summary>

1. Questionnaire Q6 on recent topics. 
2. Evaluate group assignment on Unit Tests in class (P4 "Haversine").
3. Pandas: series and dataframes; I/O; first examples.
4. **Do before next class (November 17).**
   * [Pandas documentation/getting started tutorials](https://pandas.pydata.org/docs/getting_started/intro_tutorials/index.html) up to section "How to combine data from multiple tables".
   * Optional: Check videos on Pandas on [Python Tutorials by Corey Schafer](https://www.youtube.com/playlist?list=PL-osiE80TeTt2d9bfVyTiXJA-UTHn6WwU): from [Python Pandas Tutorial (Part 2): DataFrame and Series Basics - Selecting Rows and Columns](https://www.youtube.com/watch?v=zmdjNSmRXF4&list=PL-osiE80TeTt2d9bfVyTiXJA-UTHn6WwU&index=129) to [Python Pandas Tutorial (Part 6): Add/Remove Rows and Columns From DataFrames](https://www.youtube.com/watch?v=HQ6XO9eT-fc).

</details>

<details markdown="block">

<summary> Class 9 (November 17, 2023): Regular expressions </summary>

1. Questions about Pandas.
2. Questionnaire Q7 on recent topics. 
3. Finish to evaluate group assignment P4 on Unit Tests ("Haverside") in class (remaining groups)
4. Regular expressions (regex)
5. **Do before next class (November 24).**
 * [Lecture 7](https://cs50.harvard.edu/python/2022/notes/7/) and video [CS50 Video Player: Lecture 7](https://video.cs50.io/hy3sd9MOAcc)
 * Solve problems from [Problem Set 7](https://cs50.harvard.edu/python/2022/psets/7/). In particular, you should solve problems "NUMB3RS" and "Regular, um, Expressions", following the instructions (i.e. solve and test your solution).
 * Try [https://regex101.com/](https://regex101.com/) to do experiments and understand better how "regex" works.


</details>

<details markdown="block">

<summary> Class 10 (November 24, 2023): Object-oriented programming </summary>

1. Questions about regular expressions and problems  "NUMB3RS" and "Regular, um, Expressions". Indication on how to submit the assignment.
2. Questionnaire Q8 on recent topics. 
3. Presentation of the **semester project**.
4. Object-oriented programming: see script [mage_v1.py](https://github.com/isa-ulisboa/greends-ipython/blob/main/OOP/mage_v1.py)
5. **Do before next class (December 15).**
 * [Lecture 8](https://cs50.harvard.edu/python/2022/notes/8/) on OOP
 * Video [CS50 Video Player: Lecture 8](https://video.cs50.io/e4fwY9ZsxPw)

</details>

<details markdown="block">

<summary> Class 11 (December 15, 2023): Object-oriented programming; sets, global, unpacking, args and kwargs </summary>

1. Solve [Cookie jar problem ](https://cs50.harvard.edu/python/2022/psets/8/jar/) and submit code in Fenix (P6)
2. Questionnaire Q9 on object-oriented programming; 
4. Presentation of some [additional Python topics](https://cs50.harvard.edu/python/2022/weeks/9/) with examples
5. **Do before next class (December 22).**
 * [Lecture 9](https://cs50.harvard.edu/python/2022/notes/9/); in particular, explore the following topics: sets, global variables, constants, unpacking, args (*) and kwargs (**), map, list comprehensions, filter, dictionary comprehensions.
 * Video [CS50 Video Player: Lecture 9](https://video.cs50.io/6pgodt1mezg)
 * Sugestion: Video [Python Tutorial: Comprehensions - How they work and why you should be using them](https://www.youtube.com/watch?v=3dt4OGnU5sM)
6. Example of use of `*args`and `**kwargs`. Check examples scripts in the [ETC folder](https://github.com/isa-ulisboa/greends-ipython/tree/main/ETC).
   

</details>


<details markdown="block">

<summary> Class 12 (December 22, 2023): Args and kwargs, list comprehension, dictionary comprehension, lambda, map, filter </summary>
 
1. Discussion of assigments P5 (*numb3rs* and *um*)
2. Discussion of guidelines for final project
3. Presentation of some topics from [Lecture 9](https://cs50.harvard.edu/python/2022/notes/9/):  args (*) and kwargs (**), list comprehensions, lambda functions, map, filter, dictionary comprehensions. Check examples scripts in the [ETC folder](https://github.com/isa-ulisboa/greends-ipython/tree/main/ETC).

   Example: distinct possible ways of creating a list with all the cubes of even numbers up to *N*. In the last cases, `map` applies a given function to each element of a list. Likewise, `filter` applies a boolean function to filter elements of a list. Both function can be executed in parallel over the elements of the list since each output is independent of the outputs for the remainder elements of the list.
   * With list comprehension:
     ```
     def cube(x):
         return x*x*x
     L=[cube(x) for x in range(N) if x%2==0]
     ```
   * With `filter` to select even numbers and `map`to compute cubes:
     ```
     def even(x):
         return x%2==0
     numbers=list(range(N))
     even_numbers=list(filter(even, numbers))
     cubes=list(map(cube,even_numbers))
     ```
   * Also with `filter` and `map` but defining implicitly the *cube* and *even* functions with `lambda` instead of `def`: 
     ```
     numbers=list(range(N))
     even_numbers=list(filter(lambda x: x%2==0, numbers))
     cubes=list(map(lambda x: x*x*x,even_numbers))
     ```
   * The most compact way of solving the problem involves `lambda` and list comprehension. In the example below, if one would just write `lambda x: x*x*x` instead pf `(lambda x: x*x*x)(x)` the output list would be a list of lambda functions. 
     ```
     L=[(lambda x: x*x*x)(x) for x in range(N) if x%2==0]
     ``` 
5. Observations about using vectorization to speed-up computations.

   A conditional can be replaced by arithmetic and logical operations. For example, let `L=[x/5 for x in range(-10,10)]` be a list of equally spaced numbers between -2 and 2, and say we want to apply the stepwise linear sigmoid function to the elements of the list. One could define *sigma* as below and then apply it to `L` with `map`.
   ```
   def sigma(x):
       if x>1:
           return 1
       elif x<-1:
           return -1
       else:
           return x
   list(map(sigma,L))
   ```
   However, instead of using the conditional `if` once can define *sigma* in a simpler way with logical and arithmetic operations. 
   ```
   def sigma(x):
       return (x>=1)*1+(-1<x<1)*x+(x<=-1)*-1
   list(map(sigma,L))
   ```
   Note that we don't need to define explicitly *sigma*: it could be encapsulated in a `lambda` function `lambda x: (x>=1)*1+(-1<x<1)*x+(x<=-1)*-1` as the first argument of `map`. One advantage of using arithmetic and logical operations is that computations can then be easily vectorized, which allows to speed them up, since the processing time for a pair of vectors is similar to the processing time for a pair of numbers.

   Similarly to *list comprehension*, Python provides *dictionary comprehension* which allows to create dictionaries. The example below uses `ord`which is a function that returns the *ascii* index of a character, to create a dictionary of vowels, where the key is the vowel in uppercase and the value is the rank of the letter starting at 0 for *a*.
   ```
   {x.upper(): ord(x.lower())-97 for x in 'aeiou'} # returns {'A': 0, 'E': 4, 'I': 8, 'O': 14, 'U': 20}
   ```

   
</details>


## Install Python 3 and Visual Studio Code (VS Code)

<details markdown="block">
  
<summary> Steps to install Python 3 and Visual Studio Code</summary>

[Python in VS Code](https://code.visualstudio.com/docs/python/python-tutorial):
  * Python 3 interpreter; For Windows, download either from python.org or from the Microsoft Store; For macOS install Python using Homebrew; Linux: built-in Python 3 installation
  * VS Code; Download from VS code site
  * VS Code Python extension: A Visual Studio Code extension with rich support for the Python language (for all actively supported versions of the language: >=3.7), including features such as IntelliSense (Pylance), linting, debugging, code navigation, code formatting, refactoring, variable explorer, test explorer, and more!

</details>

## Python documentation and tutorials

### CS50P
The main tutorial for the class is [CS50P](https://cs50.harvard.edu/python/2022/weeks/). The table below compares the contents of that course with another well-known 
free online Python Programming course at [PP.fi](https://programming-23.mooc.fi/). The **CS50P** course problem sets tend to be difficult, while you can find at **PP.fi** a set of problems with a larger range of difficulty, from very easy to advanced. Both online courses provide a platform for coding and testing the corretness of the solutions. Both courses provide recorded lectures: [CS50P](https://cs50.harvard.edu/python/2022/weeks/) and [PP.fi](https://programming-23.mooc.fi/#lectures).

<details markdown="block">
  
<summary> Comparison of CS50P and PP.fi</summary>

| CS50P     | Contents |  PP.fi | Contents |
| ----------- | ----------- |----------- | ----------- |
| Lecture 0    | Creating Code with Python; Functions; Bugs; Strings and Parameters; Formatting Strings; More on Strings; Integers or int; Readability Wins; Float Basics; More on Floats; Def; Returning Values    | Part 1 |   Intro; I/O; More about variables; Arithmetic operations; Conditional statements |
| Lecture 1    | Conditionals, if Statements, Control FlowModulo; Creating Our Own Parity Function; Pythonic; match | Part 2  |  Programming terminology; More conditionals; Combining conditions; Simple loops |
| Lecture 2    | Loops; While Loops; For Loops; Improving with User Input; More About Lists; Length; Dictionaries, More on code modularity  |  Part 3 |  Loops with conditions; Working with strings; More loops; Defining functions |
|  |   | Part 4 |    The Visual Studio Code editor, Python interpreter and built-in debugging tool; More functions; Lists; Definite iteration; Print statement formatting; More strings and lists |
|   |   | Part 5 |  More lists; References; Dictionary; Tuple |
| Lecture 3 | Exceptions, Runtime Errors, try, else, Creating a Function to Get an Integer, pass | Part 6  |  Reading files; Writing files; Handling errors; Local and global variables |
| Lecture 4 |  Libraries, Random, Statistics, Command-Line Arguments, slice, Packages, APIs, Making Your Own Libraries|  Part 7 | Modules; Randomness; Times and dates; Data processing; Creating your own modules; More Python features  |
| Lecture 5 | Unit Tests; assert; pytest; Testing Strings; Organizing Tests into Folders | | |
| Lecture 6| File I/O; open; with; CSV; Binary Files and PIL | | |
| Lecture 7 | Regular Expressions; Case Sensitivity; Cleaning Up User Input; Extracting User Input |||
| Lecture 8 | Object-Oriented Programming; Classes; raise; Decorators;  Class Methods; Static Methods; Inheritance; Inheritance and Exceptions; Operator Overloading| Part 8 | Objects and methods; Classes and objects; Defining classes; Defining methods; More examples of classes |
| | | Part 9 | Objects and references; Objects as attributes; Encapsulation; Scope of methods; Class attributes; More examples with classes |
| | | Part 10 | Class hierarchies; Access modifiers; Object oriented programming techniques; Developing a larger application |
| Lecture 9 | set; Global Variables; Constants; Type Hints; Docstrings; argparse; Unpacking; args and kwargs; map; List Comprehensions; filter; Dictionary Comprehensions; enumerate; Generators and Iterators | Part 11 |  List comprehensions; More comprehensions; Recursion; More recursion examples |
| | | Part 12 | Functions as arguments; Generators; Functional programming; Regular expressions|

</details>


### Documentation
You can find information on basic concepts and features of the Python language and system at  [The Python Tutorial at python.org](https://docs.python.org/3/tutorial/index.html). 

### Other tutorials

<details markdown="block">
<summary> w3schools, etc </summary>

1. A nice interactive site is W3schools' [Python Tutorial](https://www.w3schools.com/python/default.asp) where you can find in particular an easy to use  [Python reference documentation](https://www.w3schools.com/python/python_reference.asp).

2. Another nice and very clear series of videos on Python are available in this Youtube channel: [Python Tutorials by Corey Schafer](https://www.youtube.com/playlist?list=PL-osiE80TeTt2d9bfVyTiXJA-UTHn6WwU). In particular, you might be interested in the following specific topics discussed in class:
* [text](https://docs.python.org/3/tutorial/introduction.html#text) and video [Python Tutorial for Beginners 2: Strings - Working with Textual Data](https://www.youtube.com/watch?v=k9TUPpGqYTo&list=PL-osiE80TeTt2d9bfVyTiXJA-UTHn6WwU&index=2)
* [numbers](https://docs.python.org/3/tutorial/introduction.html#numbers) and video [Python Tutorial for Beginners 3: Integers and Floats - Working with Numeric Data](https://www.youtube.com/watch?v=khKv-8q7YmY&list=PL-osiE80TeTt2d9bfVyTiXJA-UTHn6WwU&index=3)
* [f-strings and other formatting options](https://docs.python.org/3/tutorial/inputoutput.html);
* [Lists](https://docs.python.org/3/tutorial/introduction.html#lists) and video [Python Tutorial for Beginners 4: Lists, Tuples, and Sets](https://www.youtube.com/watch?v=W8KRzm-HUcc&list=PL-osiE80TeTt2d9bfVyTiXJA-UTHn6WwU&index=4&t=1223s)
* [Dictionaries](https://docs.python.org/3/tutorial/datastructures.html#dictionaries), see video [Python Tutorial for Beginners 5: Dictionaries - Working with Key-Value Pairs](https://www.youtube.com/watch?v=daefaLgNkw0&list=PL-osiE80TeTt2d9bfVyTiXJA-UTHn6WwU&index=5&pp=iAQB)
* I/O and csv files: [File Objects - Reading and Writing to Files](https://www.youtube.com/watch?v=Uh2ebFW8OYM&list=PL-osiE80TeTt2d9bfVyTiXJA-UTHn6WwU&index=25); [CSV Module - How to Read, Parse, and Write CSV Files](https://www.youtube.com/watch?v=q5uM4VKywbA&list=PL-osiE80TeTt2d9bfVyTiXJA-UTHn6WwU&index=28)
* List and dictionary comprehensions, zip: [Python Tutorial: Comprehensions - How they work and why you should be using them](https://www.youtube.com/watch?v=3dt4OGnU5sM)

</details>

### Problem sets

1. List of both simple and more advanced programming exercises that you can run and test online: [programming-23.mooc.fi](https://programming-23.mooc.fi/all-exercises). Sign-in to have access to code editor and testing.
   
2. Compiled list of [CS50P proposed problems](https://raw.githack.com/isa-ulisboa/greends-ipython/main/problems.html)  (to be completed)

### Other interactive links
1. PythonTutor, that show how Python manages variables in memory: [Visualize code](https://pythontutor.com/visualize.html#mode=edit)
2. Regular expressions: [https://regex101.com/](https://regex101.com/)

### Student projects

<details markdown="block">
<summary> Project repositories </summary>
 
1. [Calculation of the Enteric Fermentation Methane Emission Factor of Cows](https://github.com/PauloCanaveira/project)
 
2. [Scrabble Training](https://github.com/domwelsh/scrabble_training/tree/main)
   
4. [Forecast Hunter: A toolbox for assessing seasonal weather forecast data usability on ETo estimation](https://github.com/dgarcian9/ForecastHunter)
   
6. [Customized and fast downloading of satellite images](https://github.com/Emmanuel461/Final_project)
   
8. [Pest Tracker: simular uma aplicação para a previsão da praga da mosca da azeitona no olival](https://github.com/filipefelisardo/PestTracker)
   
10. [Pokemon_battle_simulator](https://github.com/nachiet/Pokemon_battle_simulator)
    
12. [Forest roads under the influence of heavy rain events](https://github.com/justusnoe/forest_roads)
    
14. [Weather Report](https://github.com/marianadc01/weather-report/tree/main)
    
16. [As suas receitas na palma da mão](https://github.com/marianavalho/python_project)
    
18. [Word Wizardry](https://github.com/Sofs27/Final_Project_Alicia_Sofia)
    
20. [Calculation of Urban Density with QGIS and Python](https://github.com/laurafi97/submission-python-qgis-)
    
22. [Avaliação do risco de tempestades](https://github.com/Damiao97/isa_python_final_rep)
    
24. [Fertilização: auxiliar a fertilização com base em resultados de análises de solo](https://github.com/RubenRomeroTorrado/Fertilizacao/)
</details>

--->
