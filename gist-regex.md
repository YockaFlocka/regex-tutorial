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

`/^`#?([a-f0-9]{6}|[a-f0-9]{3})`$/`

The first component that we will be looking at are the Anchors. Looking at the regex code listed above, the highlighted portions are the Anchors. Anchors are used at the start and end of a string or expression. In this case, `/^` would signify the beginning and `$/` would signify the end of our expression.

### Quantifiers

### Grouping Constructs

### Bracket Expressions

### Character Classes

### The OR Operator

### Flags

### Character Escapes

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)
