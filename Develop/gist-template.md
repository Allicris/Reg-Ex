# Regex Tutorial with Javascript

Welcome to this tutorial! Today we will be covering Regex, Regex stands for regular expressions in short. They are a string of characters that are tied together and are used to search patterns and manipulate texts or strings.  They are very useful and are used in almost all programming languages. Today we will be going over the fundamentals of regex in Javascript and emails. I never knew how useful regex was until researching it more and didn’t realize I use it almost everyday! Whether I am searching for an email or URL, I am given results from the computer with links or email addresses that match with the characters I started to type in the search bar.

## Four Different Types of Characters of Regular Expression

1. Metacharacters

2. Quantifier

3. Groups and Ranges

4. Escape Characters or Character Classes

### Metacharacters
__^__ &nbsp;&nbsp;&nbsp; Matches an expression to the right at the start of a string. 
<br>  
Example: ^a is used to match a string like 'allison'.

__$__ &nbsp;&nbsp;&nbsp; Does the opposite and matches an expression to the left at the end of string.
<br>
Example: t$ would be used to match the 'cat' or 'matt'.

__.__ &nbsp;&nbsp;&nbsp; Used to match a single character in a string using either letters between it.
<br>
Example: t.x could me matched to 'tax', 'tox' or 'toy'.

__|__ &nbsp;&nbsp;&nbsp; Used to match a particular character or a group of characters 
<br>
Example: A|B could match Allison or Bernard.

\ &nbsp;&nbsp;&nbsp; Used to escape a special character after the sign in a string.
<br> 
Example: Allison! could be rendered as Allison.

__A__ &nbsp;&nbsp;&nbsp; Can match the charater 'A', specifically upper case. 
<br>   
Example: Can match 'About' or 'helloAllison'.

### Quantifiers

__+__ &nbsp;&nbsp;&nbsp; Specifies an expression to its left of one or more times. 
<br>
Example: a+ can give you the result of 'aa' or 'aaa' etc..

__?__ &nbsp;&nbsp;&nbsp; Specifies an expression to it's left zero or more times. 
<br> 
Example: aD? Can give you 'a' and 'ad' but not add.

__*__ &nbsp;&nbsp;&nbsp; Specifies an expression to its left for 0 or more times. 
<br>
Example: B* can give you 'B' or 'Ba' or 'Baa' etc..

__{x}__ &nbsp;&nbsp;&nbsp; Specifies an expression to its left for the number that you put inside the brackets. 
<br>
Example: A{6} can be used to give you a 'Allison' since there are 6 more characters to its left. 

__{x, }__ &nbsp;&nbsp;&nbsp; Specifies an expression to its left at least x times or more times. 
<br>
Example: Al{3, } could specify this expression Allll or Alllll etc..

__{x, y}__ &nbsp;&nbsp;&nbsp; Specifies an expression it its left at least x times but not more than y times. 
<br>
Example: Al{2, 2} could specify Allison or An{2,1}n could specify Annnn but not Annnnnn.