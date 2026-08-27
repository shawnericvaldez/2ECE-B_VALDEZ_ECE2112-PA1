# 2ECE-B, VALDEZ | ECE2112 | PA1

**By: Shawn Eric M. Valdez**

The notebook in this repository is the submission for Programming Assignment 1 for ECE2112, wherein 3 problems were required to be solved using our understanding of Python from Module 1 of this course.

# **A: Word Rotation Problem**

Create a function named rotate_word() that accepts a non-empty string. Move the first character
of the string to the end while keeping all remaining characters in their original order. Preserve the
capitalization of every character.

The function **rotate_word(text)** is defined with the parameter **text** to accept an input string. **text[1:]** takes the characters from index 1 to the end, while **text[0]** takes the first character. Using the operator **+**, the two components are combined to form a new concatenated string, with the initial letter moved to the end.

**The Function Defined:**
```python
def rotate_word(text): 
  return text[1:] + text[0]
```

# **B: Username Builder Problem**

Create a function named make username() that accepts two strings: first name and last name. The
function must:
1. Convert all letters to lowercase;
2. Remove all spaces from the first name;
3. Remove all spaces from the last name; and
4. Join the processed first and last names using one period (.).

The function **make_username(first_name, last_name)** is defined with two parameters that accept first and last names. It uses **.lower()** to convert all characters to lowercase and **.replace(" ","")** to remove all spaces. Two new variables store these results in **new_first** and **new_last**. Again, the **+** operator is used to concatenate the strings together with a **"."** string added in between to return the **complete_username** in the proper format.

**The Function Defined:**
```python
def make_username(first_name, last_name): #defines name and function of variables
  new_first = first_name.lower().replace(" ","")
  new_last = last_name.lower().replace(" ","")
  complete_username = new_first + "." + new_last
  return complete_username
```

# **C: Bookend Swap Problem**

Create a function named swap bookends() that accepts a list containing at least two elements. Unpack
the list into three variables:
• First – the first element;
• Middle – a list containing everything between the first and last elements; and
• Last – the last element.
Using these variables, return a new list in which the first and last elements have exchanged positions.
The elements in the middle must remain in their original order. Do not modify the input list.

The function swap_bookends(items) is defined with the parameter **items** to accept an input list. Extended sequence unpacking is used to define items as "first, *middle, last = items" to unpack the elements into three variables. **first** is the initial item, **last** is the final item, and the starred "*middle" is used to store all elements in between them in a sublist. **[last]**, **middle**, and **[first]** are then concatenated together using the **+** operator to return the new formatted list.

**The Function Defined:**
```python
def swap_bookends(items): #defines name and function of variables
  first, *middle, last = items
  return [last] + middle + [first]
```
