# Regex Tutorial

Regular expressions are patterns used to match character combinations in strings. In JavaScript, regular expressions are also objects. These patterns are used with the exec() and test() methods of RegExp, and with the match(), matchAll(), replace(), replaceAll(), search(), and split() methods of String. This chapter describes JavaScript regular expressions.

## Summary

In this tutorial we will be describing how the following Regex is used to match an email address:

```const rexEmail = /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/;```

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

### Anchors

- ```^The        matches any string that starts with The```
- ```end$        matches a string that ends with end```
- ```^The end$   exact string match (starts and ends with The end)```
- ```roar        matches any string that has the text roar in it```

### Quantifiers

- ```abc*        matches a string that has ab followed by zero or more c```
- ```abc+        matches a string that has ab followed by one or more c```
- ```abc?        matches a string that has ab followed by zero or one c```
- ```abc{2}      matches a string that has ab followed by 2 c```
- ```abc{2,}     matches a string that has ab followed by 2 or more c```
- ```abc{2,5}    matches a string that has ab followed by 2 up to 5 c```
- ```a(bc)*      matches a string that has a followed by zero or more copies of the sequence bc```
- ```a(bc){2,5}  matches a string that has a followed by 2 up to 5 copies of the sequence bc```

### OR Operator

- ```a(b|c)     matches a string that has a followed by b or c (and captures b or c)```
- ```a[bc]      same as previous, but without capturing b or c```

### Character Classes

- ```\d         matches a single character that is a digit```
-```\w         matches a word character (alphanumeric character plus underscore)```
-```\s         matches a whitespace character (includes tabs and line breaks)```
-````.          matches any character```

### Flags

<p>Regular expressions may have flags that affect the search.</p>

<p>There are only 6 of them in JavaScript:</p

-```i  With this flag the search is case-insensitive: no difference between A and a.```
-```g  With this flag the search looks for all matches, without it – only the first match is returned.```
-```m  Multiline mode.```
-```s  Enables “dotall” mode, that allows a dot . to match newline character \n.```
-```u  Enables full Unicode support. The flag enables correct processing of surrogate pairs.```
-```y  “Sticky” mode: searching at the exact position in the text.```

### Grouping and Capturing

<p>Capturing groups are a way to treat multiple characters as a single unit. They are created by placing the characters to be grouped inside a set of parentheses. For example, the regular expression (dog) creates a single group containing the letters "d" "o" and "g". The portion of the input string that matches the capturing group will be saved in memory for later recall via backreferences</p>

### Bracket Expressions

-```[ ] Brackets indicate a set of characters to match. Any individual character between the brackets will match, and you can also use a hyphen to define a set```
-```You can use the ^ metacharacter to negate what is between the brackets.```
-```{ } Curly braces are used to specify an exact amount of things to match.```
-```( ) Parentheses represent remembered matches. This is especially useful for find-and-replace operations or any time you need to do something with part of the match.```
-```Parentheses are also used in regex to group parts of the expression together into subgroups, like in /(\$|¥)([0-9]+)\.([0-9]{2})/.```

### Greedy and Lazy Match

### Boundaries

### Back-references

### Look-ahead and Look-behind

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)
