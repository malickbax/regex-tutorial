# REGEX TUTORIAL
This this a tutorial to explain how Regular Expressions, commonly known as Regex, work. In this tutorial, I use a regex to match an email address.

## Summary
Regex are used to declare a sequence of characters that define a search pattern of a text. As such, we can use regex to find any type of user input on a webpage. Regex allows programmers to specificifally target characters in a text and narrow down a type of input such as email addresses, telephone numbers, usernames... In this tutorial, I will be using email addresses as the text type to demonstrate how Regex work. 

## Table of Contents
- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Character Classes](#character-classes)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)
- [Greedy Match](#greedy-match)

## Regex Components for an Email Address Input
For an email address pattern, we will use the following regex components:
`/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`

Each section below describes a component explaining what it does. A code snippet of each component and some examples that meet the requirements of that component are included below.

### Anchors
Anchors allow us to define the begining and end of our search string. In our email address pattern search example above, the anchors are identified by the sympbols `^` and `$`. 
- `^` marks the begining of the email address pattern search string 
- `$` marks the end of the email address pattern search string 
- Every thing contained in between the two symbols `^` and `$` represents the string values that we are searching for. In this specific email address example, everything between the two signs `^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})`represents the search characters that allows us to narrow down our pattern to that of an email address. 

### Quantifiers
In our email address regex example, we have `+` and a `{2,6}`.
- `+` indicates the string connection between the username and email (e.g. user `+` email `+` .ext) 
- `{2,6} indicates a range of characters between 2 and 6 in the `[a-zA-Z]` set.

### Character Classes
Character classes are used to search for a specific type of character such as a digit. The backslash is used to differentiate the digit class from a regular d letter. In our example, we used `\d` which indicates we are looking for matches of any signle digit character. 

### Grouping and Capturing 
In our example, grouping is expressed through ( ) signs. Characters contained in ( ) represent a sigle unit.  
- In our email address pattern example we have three groups: (user)@(email).(ext). These correspond to `([a-z0-9_\.-]+)` @ `([\da-z\.-]+)` . `([a-z\.]{2,6})`

### Bracket Expressions
Bracket expressions indicate single characters. The characters are identified within the bracket signs. In our email address patttern example we have the following bracket components: 
- `[a-z0-9_.-]`, `[\da-z.-]`, and `[a-z.]`
- `[a-z0-9_.-]` means searching for any characters in the alphabet (a through z), or any numbers (0-9), or a period (.), or any dash (-)

### Greedy Match
The regex for our email address pattern example contains greedy operators `+` and `{}` which allow our matches to expand as far as possible through the provided text.

## Author
**Malick Ba**

If you have any questions, please feel free to post them as a comment or visit my [GitHub page](https://github.com/malickbax)  for more projects.