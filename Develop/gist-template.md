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

### Groups and Ranges

__( )__ &nbsp;&nbsp;&nbsp; Used to match everything that us in the bracket.
<br>
Example: A(ll) matches the string: 'All'.

__{ }__ &nbsp;&nbsp;&nbsp; Used to match a particular number of occurrences that are in the curly brackets going to the left of the string. 
<br>
Example: All{3,2} would match the string 'Alllllll'.

__[ ]__ &nbsp;&nbsp;&nbsp; Used to match any character from the range og characters that are in the string inside of the square brackets.
<br>
Example: Al[cef]n can match the following strings: 'Alcn', 'Alen', and 'Alfn.

__[sol]__ &nbsp;&nbsp;&nbsp; Matches individual characters. 
<br>
Example: the [sol] would let you match with 's', 'o', and 'l'.

__[sol][ce]__ &nbsp;&nbsp;&nbsp; matches a single character from the first bracket and then following it would match with either c or e to its left. 
<br>
Example: It could match to the following strings: 'sc', 'oc', 'lc', 'se', 'oe' and 'le'. 

__(?: ...)__ &nbsp;&nbsp;&nbsp; Used to match a non-capturing group. 
<br>
Example: A(?:nt|pple) could match a string like 'Apple'.

__[^.....]__ &nbsp;&nbsp;&nbsp; Matches a character that is not defined in the square bracket. 
<br>
Example: If you have Al[^sol] could be matched to a string like: 'Al'.

__[a-z]__ &nbsp;&nbsp;&nbsp; Matches the range of letters in lowercase to a string. 
<br>
Example: Could match 'rainbow', 'zebra' or 'cookies'

__[A-Z]__ &nbsp;&nbsp;&nbsp; does the same thing as the above but in uppercase.
<br>
Example: Could match 'RAINBOW', 'ZEBRA' OR 'COOKIES'.

__^[a-zA-z]__ &nbsp;&nbsp;&nbsp; When you have a range of letters side by side it could match either lowercase or uppercase
<br>
Example: It could match 'NewYork' or 'greenDay'.

__[0-5] &nbsp;&nbsp;&nbsp; Matches a character within the range of the numbers indicated in the square brackets.
<br>
Example: Could match '12432' or '54234' 

__[aeiou]__ &nbsp;&nbsp;&nbsp; This specific bracket only matches the lower case vowels. 

__[AEIOU]__ &nbsp;&nbsp;&nbsp; This does the opposite from above and matches the uppercase vowels.

__al[^1-5]__ &nbsp;&nbsp;&nbsp; Matches the numbers or characters that aren't in the square bracket.
<br>
Example: Cannot match strings that contain 2, 3, and 4.

### Escape Characters or Character Classes

__\s__ &nbsp;&nbsp;&nbsp; Used to match one white space character. 

__\S__ &nbsp;&nbsp;&nbsp; Used to match one non-white space character.

__\0__ &nbsp;&nbsp;&nbsp; Used to match a NULL character. 

__\a__ &nbsp;&nbsp;&nbsp; Used to match an alarm or bell.

__\d__ &nbsp;&nbsp;&nbsp; Used to match one decimal digit, which means from 0 to 9.

__\D__ &nbsp;&nbsp;&nbsp; Used to match a non-decimal digit. 

__\n__ &nbsp;&nbsp;&nbsp; Used to match a new line

__\w__ &nbsp;&nbsp;&nbsp; Used to match the alphanumeric characters, [0-9a-zA-Z]. 

__\W__ &nbsp;&nbsp;&nbsp; Used to match the non-word character.

__\b__ &nbsp;&nbsp;&nbsp; Used to match a word boundary. 

## Regular Expression Languages 

Regular Expressions are used in Java, PHP, Python and JavaScript. Today we will explain how it can be incorporated in JavaScript code. 

### Regex in Javascript

It is very easy to use regular expressions in JavaScript code, the following two string methods provide a huge help:

1. __search():__ This searches the regex in the string inside the brackets and returns the position where the match was found.
<br>
Example: Using the search() method: var string = 'apples', pattern = 'technical',
var res = string.search(pattern), Returns the position of the string as well.

2. __Replace():__ This method is used to return the string after the replacement of a matched character in a string. 
<br>
Example: Using the repalce() method: var string = 'Allison', var pattern = /Yes/;, var replace = 'No';, var res = string.replace(/Yes/,replace);. This replaces the original word with the string related to replace. It will give you the output of 'Do you like coffee? No'.


