# REGEX TUTORIAL

A regex, or regular expression, is a sequence of characters that defines a specific search pattern. It is quite useful when used in code or search algorithms. They can be used to find certain patterns of characters or to replace characters within a string. They are also used to validate input data. This tutoril will break down each part of the regex and what it does!


## Summary

This tutorial will discuss how the components of a regex can be used to verify that the user provided a valid email address: 

`/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`

Each component of this regex has its own unique responsibility to ensure that what the user passed in is indeed a valid email addresss, and each part is essential in making sure that the expression works correctly. 


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

The characters `^` and `$` are considered anchors. The `^` anchor is used to signify the characters that follow the string. The `$` anchor signifies a string that ends with the charactors that precede it.

So when we look at our email regex `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`, we are saying that we saying that the email pattern must start with `([a-z0-9_\.-]+)`, and it must end with `([a-z\.]{2,6})`. 

If it does not start or end with those given parameters, it will not be considered an email, and will not be accepted. 

### Quantifiers



### Grouping Constructs



### Bracket Expressions



### Character Classes



### The OR Operator



### Flags



### Character Escapes



## Author


A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)
