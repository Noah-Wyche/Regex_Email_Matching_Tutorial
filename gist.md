# Matching an Email with Regex (Tutorial)

Obtaining reliable data from users who access websites can be quite a challenge. To err is human and it can be
all too easy to make a mistake when filling out online forms or submitting emails. One of the tools dvelopers have
at their disposal is verification. Using tools like Regular expressions allows us to automatically filter out some
mistakes and improve the user experience.

## Summary

I will be describing the function and purpose of a matching an email regex using the function: 

'/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/'

A regular expression is a specific line of code that defines a search pattern. In this case it is validating an email address to meet certain criteria

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [OR Operator](#or-operator)
- [Character Classes](#character-classes)
- [Flags](#flags)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)
- [Greedy and Lazy Match](#greedy-and-lazy-match)
- [Boundaries](#boundaries)
- [Back-references](#back-references)
- [Look-ahead and Look-behind](#look-ahead-and-look-behind)

## Regex Components
Regular expressions, though they look confusing are all made up of a certain set of components

/ ^ ( [ a-z 0-9 _\.- ] + ) @ ( [ \ da-z \.- ] + ) \.( [a-z\.] {2,6} ) $ /

Since it is considered a litteral it must be wrapped in '/' slash characters
Lets look at the rest of its components.

### Anchors
'^' and '$' are the anchors for this function and mark the beginning and end of the expression.
Between the two anchors we will find all the information needed to validate email addresses

### Quantifiers
A quantifier works by setting limits to the string. In our case '{2, 6}' is a quantifier.
We can see in this snippet: '([a-z\.]{2,6})' only this area will be effected by the quantifier since it is contained inside the ''''.
Quantifiers have several different methods to set up a limit,

{ n }—Matches the pattern exactly n number of times

{ n, }—Matches the pattern at least n number of times

{ n, x }—Matches the pattern from a minimum of n number of times to a maximum of x number of times

Since our quantifier, '{2, 6}', falls into the { n, x } method, it will require this section to be between 2 and 6 characters.

### Character Classes

### Flags

### Grouping and Capturing

### Bracket Expressions

### Greedy and Lazy Match

### Boundaries

### Back-references

### Look-ahead and Look-behind

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)