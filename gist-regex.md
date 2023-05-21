# Regex Tutorial

This Regex (Regular Expression) tutorial is created to help the reader break down and define the sequence of Regex special characters used for matching an email. Regex can be used in code to find certain patterns of characters within a string, or to find and replace a character of sequence of characters within a string. It is also used to validate input data, like in this case. 

## Summary

In this tutorial I will be breaking down the components of a regular expression used to match an email. By using regex, we can make it so the user has to enter a valid email in order to make an accout, sign up for something, etc.

/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Grouping Constructs](#grouping-constructs)
- [Bracket Expressions](#bracket-expressions)
- [Character Classes](#character-classes)
- [The OR Operator](#the-or-operator)
- [Flags](#flags)
- [Character Escapes](#character-escapes)

## Regex Components

### Anchors

`/^`([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})`$/`

The first component that we will be looking at are the Anchors. Looking at the regex code listed above, the highlighted portions are the Anchors. Anchors are used at the start and end of a string or expression. In this case, `/^` would signify the beginning and `$/` would signify the end of our expression.

### Quantifiers

/^([a-z0-9_\.-]`+`)@([\da-z\.-]`+`)\.([a-z\.]`{2,6}`)$/

A Quantifier specifies how many instances of the previous element (which can be a character, a group, or a character class) must be present in the input string for a match to occur. Quantifiers also determine whether a regular expression will attempt to perform a Lazy match or a Greedy match.

In the code above, we have two different quantifiers that are highlighted: The "+" character and a range of {2,6}.

The two "+" Quantifiers tells our regular expression to attempt to match everything within the Capture Group "()" with a character between one and unlimited times, as many times as possible. This means the regex will keep matching until either there are no characters to match (a blank string value), the character set that follows the string appears ("@" symbol for Group 1, "." for Group 2), or a character that does not match the string paramaters appears. This is a Greedy match because the Qualifier will attempt to match the largest group of characters possible barring the 3 circumstances above.

The {2,6} Qualifier performs a similar function. The regex attempts to match everything within the Capture Group "()" with a character between 2 and 6 times, as many as possible. It sets the range of matches instead of leaving it unlimited like with the "+" Qualifier. This Qualifier is also Greedy because it will still attempt to match the largest group possible.

### Bracket Expressions

/^(`[a-z0-9_\.-]`+)@(`[\da-z\.-]`+)\.(`[a-z\.]` `{2,6}`)$/

Brackets indicate a set of characters to match. Any individual character between the brackets will match, and you can use a hyphen to define a set ([abcd], [a-d]).

Curly braces are used to specify an exact amount of things to match. In this case, the regular expression is showing to match between 2 and 6 times {2,6}.

### Character Classes

/^(`[a-z0-9_\.-]`+)`@`(`[\da-z\.-]`+)`\.`(`[a-z\.]`{2,6})$/

Character Classes match a character in the input string to any one character set within it. In our regex above, we have 3 bracket expressions that house multiple Character Classes. We also have 2 Character Classes that are matched literally at the correct position in the input string ("@" and ".").

- "a-z" is a lowercase character range
- "0-9" is a digit character range
- "\d" serves the same purpose as defining the previous digit range (0-9)
- "_" and "-" match their respective characters literally
- "\." matches a period literally
- "@" and the external "\." match their respective characters literally at specific positions in the input string

### Character Escapes

/^([a-z0-9_`\.`-]+)@([\da-z`\.`-]+)`\.`([a-z`\.`]{2,6})$/

To match a character having special meaning in regex, you need to use an escape sequence prefix with a backslash (\). Example:   \. matches ".",    \+ matches "+"

## Author

Peter Yockey

Peter Yockey is a Biology graduate who decided the path he wanted to take was coding. To further this dream, he is a coding student taking a bootcamp with the University of Minnesota to earn a certificate in full-stack development.

GitHub: [YockaFlocka](https://github.com/YockaFlocka)
