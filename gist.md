# Matching an Email with Regex (Tutorial)

Obtaining reliable data from users who access websites can be quite a challenge. To err is human and it can be all too easy to make a mistake when filling out 
online forms or submitting emails. One of the tools dvelopers haveat their disposal is verification. Using tools like Regular expressions allows us to automatically 
filter out some mistakes and improve the user experience.

## Summary

I will be describing the function and purpose of a matching an email regex using the function: 

'/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/'

A regular expression is a specific line of code that defines a search pattern. In this case it is validating an email address to meet certain criteria.

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Character Classes](#character-classes)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)
- [Greedy and Lazy Match](#greedy-and-lazy-match)

## Regex Components
Regular expressions, though they look confusing are all made up of a certain set of components.

/ ^ ( [ a-z 0-9 _ \ . - ] + ) @ ( [ \d a-z \ . - ] + ) \ .( [ a-z \ .] {2,6} ) $ /

Since it is considered a litteral it must be wrapped in '/' slash characters.
Lets look at the rest of its components.

### Anchors
'^' and '$' are the anchors for this function and mark the beginning and end of the expression.
Between the two anchors we will find all the information needed to validate email addresses.

### Quantifiers
A quantifier works by setting limits to the string. In our case '{2, 6}' is a quantifier.
We can see in this snippet: '([a-z\.]{2,6})' only this area will be effected by the quantifier since it is contained inside the ''''.
Quantifiers have several different methods to set up a limit,

{ n }—Matches the pattern exactly n number of times

{ n, }—Matches the pattern at least n number of times

{ n, x }—Matches the pattern from a minimum of n number of times to a maximum of x number of times

Since our quantifier, '{2, 6}', falls into the { n, x } method, it will require this section to be between 2 and 6 characters.

### Character Classes
Character Classes define a set of characters in a regex, any one of which would pass validation inside the string.
'[a-z0-9_\.-]' is a character class that allows any lower case letter, any number between 0 and 9, and the special characters: "_", "\", ".", and "-".
'[\da-z\.-]' defines almost the same thing but uses \d to allow for any single digit, and leaves out the "_".
'[a-z\.]' allows only lowercase letters "a" through "z", "\", and ".".

### Grouping and Capturing
Looking back at our full expression we can see that there are 3 distinct subgroups or subexpressions.

'/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/'

Think of the expression like a math problem where the things inside the parenthesis need to be dealt with together.
'/^' - Oppening anchor of our expression
'([a-z0-9_\.-]+)' - First group, defines the section of the email before the '@'. The '+' allows for one or more of the proceeding characters. (at least something but as much as you want)
'@' - Requires an @ sign
'([\da-z\.-]+)' - Second group, defines the domain of the email
'\.' - Accepts only a '\' or a '.'
'([a-z\.]{2,6})' - Third group, difines the extension (.com, .org, etc...)
'$/' - Ending anchor tag of our expression

### Bracket Expressions
Bracket expressions are defined within the square brackets '{}' and include everything that we want to match from our expression.
Multiple character classes can be contained inside of a bracket expression such as here:
'[a-z0-9_\.-]'
This is only one bracket expression but it contains the character classes for lowercase a-z, 0-9, and _\.-.
All of these are options for this particular bracket expression.

### Greedy and Lazy Match
All quantifiers are greedy and will match the pattern as many times as they are able to.
The '+' quantifier matches the pattern one or more times, meaning it can be as long as you want so long as there is at least one.
The '{}' defines a specific limit to how long the string can be in our case.

## Author

Hi!

My name is Noah Fleetwood, I am 24 and I learned a lot about Regular Expressions while writing this tutorial. I hope you can find it useful and if you'd like to see my other work, check out my Github page here: https://github.com/Noah-Wyche

Thanks a ton!