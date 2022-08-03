

# Applied Python Exercise 2

## Goal -- Print the first line in a file

Write Python code that works towards recreating the Bash tool `head`, displaying only the first line in a file: `random_snippet.vcf`

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

Let's start with and edit the pseudocode from the last module to meet the needs of this module.

Note: you may write/edit pseudocode anywhere you would like. You will not have to turn in any pseudocode for any chapter. Just remember that since pseudocode doesn't follow the syntax of any one programming language, if you choose to write it in the online python text editor interface or your local python script, you'll want to make sure when you run the script that the pseudocode is commented out (with a `#` in front of it) so that Python does not try to treat it as real code which will cause errors.

Last module's pseudocode:

First, we need to SET the input file <br />
Second, FOR every line in the open file <br />
&nbsp;&nbsp;  PRINT the line <br />
END FOR <br />

In this module, we want to only print the line if it's the first line of the file. Keeping the for loop, edit the pseudocode, inserting a step that asks which line position it is numerically in the file.


***
<details><summary> ANSWER: </summary>

First, we need to SET the input file <br />
Second, FOR every line in the open file <br />
&nbsp;&nbsp;  IF the first line <br />
&nbsp;&nbsp;&nbsp;&nbsp;    PRINT the line <br />
&nbsp;&nbsp;  END IF <br />
END FOR <br />

</details>
***

### SET the input file

Much like how we reused the pseudocode of the last module, we'll be able to reuse much of the code from the last module. Do you think that defining a variable with the input file name is one of those reusable steps? 

***
<details><summary> ANSWER: </summary>

Yes, it is

</details>
***

### FOR every line in the open file

Let's again focus on building the `for` loop structure by considering the 2 components of the loop used in the first module

1. The `for` statement

  Do you think that the `for` statement from the last module is the best pattern for this problem? Consider that the `for` statement in the last module only provided you access to each line (or item) in the file (or collection of items), but did not provide you any information on which line position numerically it was in the file.
  
  ***
  <details><summary> ANSWER: </summary>
 
  We should use the third `for` statement pattern instead which provides both the item and the item's position or index.

  </details>
  *** 
  
### IF the first line and PRINT the line

2. The body of the `for` loop
  
  Considering that the body of the for loop is where the pseudocode was added, we also need to add to the body of the `for` loop. However, does the code that we already have from the first module still work well for this module?
  
  ***
  <details><summary> ANSWER: </summary>
  
  Yes, it does.
  
  </details>
  ***
  
  What can we use to see if the index or position of the line is the first line in the file? 
  
  ***
  <details><summary> ANSWER: </summary>
  
  We can use a conditional and logical expression such that we'll PRINT the line, but only if it's the first line in the file.
  
  </details>
  ***
  

## Building the code

**Create a new Python script**

### SET the input file

To SET what the input file is, we will use the variable assignment code from the first module. Within your Python script, write that variable assignment expression. 

***
<details><summary> ANSWER: </summary>


```python
filename = "random_snippet.vcf"
```

</details>
***

### FOR every line in the open file

Consult the notes on the third pattern of the `for` statement and edit the first modules `for` statement code to meet the needs of this module. Within your python script, write the revised `for` statement.

***
<details><summary> ANSWER: </summary>


```python
for i, line in enumerate(open(filename)):
```

</details>
***

### IF the first line

Next, edit the body of the `for` loop from the first module such that it asks if the line is the first line. Consult your notes on indexing to see what integer you want the index to be equal to (e.g., 0 or 1). Write the conditional and logical expression code within your Python script within the `for` loop body.

***
<details><summary> ANSWER: </summary>


```python
  if i == 0:
```

</details>
***

### PRINT the line

Finally, reuse the code from the first module to print the line (when it is the first line). Add this `print()` statement to your Python script, indenting correctly under the conditional statement.

***
<details><summary> ANSWER: </summary>


```python
    print(line.strip('\r\n'))
```

</details>
***

Within your Python script, you should have the four lines of code together which makes our complete indended goal code -- code that prints just the first line in a file.

**Use the command line or the Run button in the online interface to run the Python script and look at the output.**

## Complete Intended Goal Code

***
<details><summary> ANSWER: </summary>


```python
filename = "random_snippet.vcf" #SET the input filename
for i, line in enumerate(open(filename)): #FOR every line in the open file
  if i == 0: #IF the first line
    print(line.strip('\r\n')) #PRINT the line
```

</details>
***
