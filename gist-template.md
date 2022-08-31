# RegEx Tutorial - Matching a Hex Value

A regular expression (regex) is a sequence of characters that specifies a search pattern in text. Regex can be used to check if a string contains the specified search pattern.

Hex color codes (also referred to as hexadecimal color or hex) are a type of HTML color code. Hex color codes begin with a hashtag (#) and are followed by six letters and / or numbers. As an example, some common colors are:

- Red = #FF0000
- Gren = #008000
- Blue = #0000FF

A valid hex color code must satisfy the following conditions:

- Start with the hastag symbol (#)
- The hashtag should be followed by letters (a-f) or (A-F) and / or the digits 0-9
- The length of the hex color code should be either 3 or 6, excluding the hashtage

The regex to match a hex color code can be written as: /^#?([a-f0-9]{6}|[a-f0-9]{3})$/

## Summary

The regex code to validate a hex code is: /^#?([a-f0-9]{6}|[a-f0-9]{3})$/

- '^' represents the start of the string
- '#' represents that the hex color code must begin with the (#) symbol in order to be valid
- '(' represents the start of the group
- '[a-f0-9]{6}' represents the letters from a-f, or digits from 0-9, with a length of six
- '|' represents OR
- '[a-f0-9]{3}' represents the letters from a-f, or digits from 0-9, with a length of three
- ')' represents the end of the group
- '$' represents the end of the string

This tutorial will review the elements of the hex code described above

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [OR Operator](#or-operator)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)

## Regex Components

### Anchors

Anchors are regex tokens that do not match any character, but provide information about the string or matching process. Anchors indicate that the engine's current position in the string matches a specific location, e.g., the beginning or end of a string.

In the example: ^#?([a-f0-9]{6}|[a-f0-9]{3})$

- the caret (^) represents the beginning of the string
- the dollar sign ($) represents the end of the string

### Quantifiers

Quantifiers match a number of instances of a character, group, or character class in a string.

- {n} a number in curly braces appended to a character or character class specifies how many characters / character classes you want to match
- {n,m} represents a range. The range matches a character or character class from n to m times
- ? represents zero or one. As an example, /colou?r/ will match both color and colour

In the example: ^#?([a-f0-9]{6}|[a-f0-9]{3})$ quantifiers are:

- {6} in [a-f0-9]{6} indicating 6 instances of the criteria within the brackets
- {3} in [a-f0-9]{3} indicating 3 instances of the criteria within the brackets

### OR Operator

The | operator (logical OR) can be used to match characters or expressions on either the left or right of the | operator. As an example the (a|A) will match either a or A from the input string.

In the example: ^#?([a-f0-9]{6}|[a-f0-9]{3})$, the hex color code is valid if either of the following expressions is matched:

- [a-f0-9]{6} OR
- [a-f0-9]{3}

### Grouping and Capturing

A group in regex is part of a regex pattern enclosed in parentheses (). A group is created by placing the regex pattern inside the parentheses, e.g., the regular expression (dog) creates a single group containing the letters 'd', 'o', and 'g'.

In the example: ^#?([a-f0-9]{6}|[a-f0-9]{3})$ the group is composed of:

- [a-f0-9]{6}|[a-f0-9]{3}

### Bracket Expressions

A bracket expression is a list of characters enclosed by '[' and ']'. It matches any single character in that list. If the first character of the list is a caret '^', then it matches any character not in the list.

In the example: ^#?([a-f0-9]{6}|[a-f0-9]{3})$ the bracket expressions is:

- '[a-f0-9]' one character that is within the range of a-f OR 0-9

## Author

Reena is a wealth management specialist, financial literacy advocate, and delighted to be learning coding! GitHub - https://github.com/RHunjan
