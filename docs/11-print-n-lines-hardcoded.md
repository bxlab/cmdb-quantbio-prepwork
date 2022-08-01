

# Applied Python Exercise 3

## Goal -- Print some specified number of lines from the beginning of an input file: `random_snippet.vcf`

Write Python code that works towards recreating the Bash tool `head`, displaying a specified number of lines from the beginning of a file.

## Learning Objectives

After going through this module, students should be able to:

* State the sub-steps needed to meet the coding goal
* Use the following datatypes, structures, and fundamentals to meet the coding goal:
  * variable assignment
  * strings
  * opening a file
  * for loop
  * integers
  * logical expression
  * conditional statement
  * printing output

## Coding Blueprint

Let's again start with and edit the pseudocode from the last module to meet the needs of this module.

Last module's pseudocode:

First, we need to SET the input file <br />
Second, FOR every line in the open file <br />
&nbsp;&nbsp;  IF the first line <br />
&nbsp;&nbsp;&nbsp;&nbsp;    PRINT the line <br />
&nbsp;&nbsp;  END IF <br />
END FOR <br />

In this module, we no longer want to print the line if and only if it's the first line of the file. We now want to print the line if it's any of the first several lines of the file, where the actual number of lines is specified or set or defined, much like how we define the input file name. Edit the pseudocode, adding one line, and editing another line to reflect this change in the goal.

***
<details><summary> ANSWER: </summary>

First, we need to SET the input file <br />
Next, we need to SET the desired number of displayed lines <br />
Then, FOR every line in the open file <br />
&nbsp;&nbsp;  IF a desired line (by its numerical position) <br />
&nbsp;&nbsp;&nbsp;&nbsp;    PRINT the line <br />
&nbsp;&nbsp;  END IF <br />
END FOR <br />

</details>
***

## Building the code

**Create a new Python script**

Much like how we added one line and edited one line of the previous module's pseudocode, for the actual code, you will only need to add one line of code, and edit one line of code. 

### SET the input file 

To SET what the input file is, we will use the variable assignment code from the first and second Python exercise modules. Within your Python script, write that variable assignment expression. 

***
<details><summary> ANSWER: </summary>


```python
filename = "random_snippet.vcf"
```

</details>
***

### SET the desired number of lines

To SET the desired number of beginning lines to display, write a variable assignment expression, using some integer value as the desired number. Add this new line of code within your Python script.

***
<details><summary> ANSWER: </summary>


```python
n_lines = 10
```

</details>
***

### FOR every line in the open file

To loop through every line in the open file, use the `for` statement structure from the second Python exercise module. Write this line of code within your Python script.

***
<details><summary> ANSWER: </summary>


```python
for i, line in enumerate(open(filename)):
```

</details>
***

### IF a desired line (by its numerical position)

Next, edit the body of the `for` loop, specifically the conditional expression, such that it asks if the line is one of the desired beginning lines. Consult your notes on indexing in python to see what numerical comparison operator (e.g., `<=`, `<`, `==`) is necessary. Add this edited line of code within the `for` loop body within your Python script.

***
<details><summary> ANSWER: </summary>


```python
  if i < n_lines:
```

</details>
***

### PRINT the line

Finally, resue the code from the first two Python exercise modules to print the line, adding this `print()` statement indented correctly under the conditional within your Python script.

***
<details><summary> ANSWER: </summary>


```python
    print(line.strip('\r\n'))
```

</details>
***

Within your Python script, you should have the five lines of code together which makes our complete intended goal code -- code that prints a specified number of lines from the beginning of a file.

**Use the command line to run the Python script and look at the output**

## Complete Intended Goal Code

***
<details><summary> ANSWER: </summary>


```python
filename = "random_snippet.vcf" #SET the input filename
n_lines = 10 #SET the desired number of lines
for i, line in enumerate(open(filename)): #FOR every line in the open file
  if i < n_lines: #IF a desired line by its numerical position
    print(line.strip('\r\n')) #PRINT the line
```

</details>
***
