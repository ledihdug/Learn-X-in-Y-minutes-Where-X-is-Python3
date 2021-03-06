# Learn X in Y minutes (Where X=python3)
**Source:** [Learn X in Y minutes (Where X=python3) — Louie Dinh](https://learnxinyminutes.com/docs/python3/)


Table of Contents
=================

- [Table of contents](#table-of-contents)
- [0. Comments](#0-comments)
    + [Single line comments](#single-line-comments)
    + [Multi-line comments](#multi-line-comments)
- [1. Primitive Datatypes and Operators](#1-primitive-datatypes-and-operators)
    + [You have numbers](#you-have-numbers)
    + [Math is what you would expect](#math-is-what-you-would-expect)
    + [Result of integer division truncated down both for positive and negative](#result-of-integer-division-truncated-down-both-for-positive-and-negative)
    + [The result of division is always a float](#the-result-of-division-is-always-a-float)
    + [Modulo operation](#modulo-operation)
    + [Exponentiation](#exponentiation)
    + [Enforce precedence with parentheses](#enforce-precedence-with-parentheses)
    + [Boolean values are primitives](#boolean-values-are-primitives)
    + [Negate with not](#negate-with-not)
    + [Boolean Operators](#boolean-operators)
    + [True and False are actually 1 and 0 but with different keywords](#true-and-false-are-actually-1-and-0-but-with-different-keywords)
    + [Comparison operators look at the numerical value of True and False](#comparison-operators-look-at-the-numerical-value-of-true-and-false)
    + [Using boolean logical operators on ints casts them to booleans for evaluation](#using-boolean-logical-operators-on-ints-casts-them-to-booleans-for-evaluation)
    + [Equality](#equality)
    + [Inequality is](#inequality-is)
    + [More comparisons](#more-comparisons)
    + [Seeing whether a value is in a range](#seeing-whether-a-value-is-in-a-range)
    + [Chaining makes this look nicer](#chaining-makes-this-look-nicer)
    + [two variables refer to the same object or to have the same values](#two-variables-refer-to-the-same-object-or-to-have-the-same-values)
    + [Strings are created](#strings-are-created)
    + [Strings can be added too](#strings-can-be-added-too)
    + [String literals can be concatenated](#string-literals-can-be-concatenated)
    + [A string can be treated like a list of characters](#a-string-can-be-treated-like-a-list-of-characters)
    + [You can find the length of a string](#you-can-find-the-length-of-a-string)
    + [format strings](#format-strings)
    + [You can repeat the formatting arguments to save some typing](#you-can-repeat-the-formatting-arguments-to-save-some-typing)
    + [You can use keywords if you do not want to count](#you-can-use-keywords-if-you-do-not-want-to-count)
    + [If your Python 3 code also needs to run on Python 2.5 and below](#if-your-python-3-code-also-needs-to-run-on-python-25-and-below)
    + [You can also format using f-strings or formatted string literals](#you-can-also-format-using-f-strings-or-formatted-string-literals)
    + [You can basically put any Python statement inside the braces and it will be output in the string](#you-can-basically-put-any-python-statement-inside-the-braces-and-it-will-be-output-in-the-string)
    + [None is an object](#none-is-an-object)
    + [Do not use the equality symbol to compare objects to None](#do-not-use-the-equality-symbol-to-compare-objects-to-none)
    + [None 0 and empty strings or lists or dicts or tuples all evaluate to False](#none-0-and-empty-strings-or-lists-or-dicts-or-tuples-all-evaluate-to-false)

<small><i><a href='http://ecotrust-canada.github.io/markdown-toc/'>Table of contents generated with markdown-toc</a></i></small>


## 0. Comments
#### Single line comments
```python
# Single line comments start with a number symbol.
```
#### Multi-line comments
```python
""" 
Multiline strings can be written
using three "s, and are often used
as documentation.
"""
```
## 1. Primitive Datatypes and Operators
#### You have numbers
```
3  # => 3
```
#### Math is what you would expect
```python
1 + 1   # => 2
8 - 1   # => 7
10 * 2  # => 20
35 / 5  # => 7.0
```
#### Result of integer division truncated down both for positive and negative
```python
5 // 3       # => 1
5.0 // 3.0   # => 1.0 # works on floats too
-5 // 3      # => -2
-5.0 // 3.0  # => -2.0
```
#### The result of division is always a float
```python
10.0 / 3  # => 3.3333333333333335
```
#### Modulo operation
```python
7 % 3  # => 1
```
#### Exponentiation 
**(x^y, x to the yth power)**
```python
2**3  # => 8
```
#### Enforce precedence with parentheses
```python
(1 + 3) * 2  # => 8
```
#### Boolean values are primitives 
**(Note: the capitalization)**
```python
True
False
```
#### Negate with not
```python
not True   # => False
not False  # => True
```
#### Boolean Operators
**Note "and" and "or" are case-sensitive**
```python
True and False  # => False
False or True   # => True
```
#### True and False are actually 1 and 0 but with different keywords
```python
True + True # => 2
True * 8    # => 8
False - 5   # => -5
```
#### Comparison operators look at the numerical value of True and False
```python
0 == False  # => True
1 == True   # => True
2 == True   # => False
-5 != False # => True
```
#### Using boolean logical operators on ints casts them to booleans for evaluation
**But their non-cast value is returned. Don't mix up with bool(ints) and bitwise and/or (&,|)**
```python
bool(0)     # => False
bool(4)     # => True
bool(-6)    # => True
0 and 2     # => 0
-5 or 0     # => -5
```
#### Equality 
**Equality is ==**
```python
1 == 1  # => True
2 == 1  # => False
```
#### Inequality is
**Inequality is !=
```python
1 != 1  # => False
2 != 1  # => True
```
#### More comparisons
```python
1 < 10  # => True
1 > 10  # => False
2 <= 2  # => True
2 >= 2  # => True
```
#### Seeing whether a value is in a range
```python
1 < 2 and 2 < 3  # => True
2 < 3 and 3 < 2  # => False
```
#### Chaining makes this look nicer
```python
1 < 2 < 3  # => True
2 < 3 < 2  # => False
```
#### two variables refer to the same object or to have the same values
**(is vs. ==) is checks if two variables refer to the same object,but == checks if the objects pointed to have the same values.**
```python
a = [1, 2, 3, 4]  # Point a at a new list, [1, 2, 3, 4]
b = a             # Point b at what a is pointing to
b is a            # => True, a and b refer to the same object
b == a            # => True, a's and b's objects are equal
b = [1, 2, 3, 4]  # Point b at a new list, [1, 2, 3, 4]
b is a            # => False, a and b do not refer to the same object
b == a            # => True, a's and b's objects are equal
```
#### Strings are created 
**String are created with " or '**
```python
"This is a string."
'This is also a string.'
```
#### Strings can be added too
**Strings can be added too! But try not to do this.**
```python
"Hello " + "world!"  # => "Hello world!"
```
#### String literals can be concatenated 
**String literals (but not variables) can be concatenated without using '+'**
```python
"Hello " "world!"    # => "Hello world!"
```
#### A string can be treated like a list of characters
```python
"This is a string"[0]  # => 'T'
```
#### You can find the length of a string
```python
len("This is a string")  # => 16
```
#### format strings
**.format can be used to format strings, like this:**
```python
"{} can be {}".format("Strings", "interpolated")  # => "Strings can be interpolated"
```
#### You can repeat the formatting arguments to save some typing
```python
"{0} be nimble, {0} be quick, {0} jump over the {1}".format("Jack", "candle stick")
    # => "Jack be nimble, Jack be quick, Jack jump over the candle stick"
```
#### You can use keywords if you do not want to count
```python
"{name} wants to eat {food}".format(name="Bob", food="lasagna")  # => "Bob wants to eat lasagna"
```
#### If your Python 3 code also needs to run on Python 2.5 and below
**you can also still use the old style of formatting:**
```python
"%s can be %s the %s way" % ("Strings", "interpolated", "old")  
# => "Strings can be interpolated the old way"
```
#### You can also format using f-strings or formatted string literals 
**(in Python 3.6+)**
```python
name = "Reiko"
f"She said her name is {name}." # => "She said her name is Reiko"
```
#### You can basically put any Python statement inside the braces and it will be output in the string
**(Python 3.6+)**
```python
f"{name} is {len(name)} characters long."
```
#### None is an object
```python
None  # => None
```
#### Do not use the equality symbol to compare objects to None
**Don't use the equality "==" symbol to compare objects to None. Use "is" instead. This checks for equality of object identity.**
```python
"etc" is None  # => False
None is None   # => True
```
#### None 0 and empty strings or lists or dicts or tuples all evaluate to False
**None, 0, and empty strings/lists/dicts/tuples all evaluate to False.**
**All other values are True**
```python
bool(0)   # => False
bool("")  # => False
bool([])  # => False
bool({})  # => False
bool(())  # => False
```

