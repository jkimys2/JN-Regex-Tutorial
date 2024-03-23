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

Quantifiers set the limits of the string that your regex matches. They specify how many instances of a character, group, or character class must be present in the input for a match to be found. They can either be greedy, meaning they can match as many occurrences of pattterns as possible, or lazy, meaning they will match as few occurences as possible. 

- `*` means that the pattern will matfh 0 or more times
- `+` means that the pattern will match 1 or more times
- `?` means that the pattern will match 0 or 1 time
- `{}` provide three different ways to set limits:
    * `{ n }` matches the pattern exactly n number of times
    * `{ n, }` matches the pattern at least n number of times
    * ` { n, x }` matches the pattern from a minimum of n number of times to maximum of x number of times
- Adding `?` after each of the quantifiers makes each of them lazy.

In the case of our email regex, `([a-z0-9_\.-]+)`, it contains the `+` quantifier. This means that the email that the user provides needs to contain at least one of the characts inside the brackets in order to match. 

The email regex also contains `([a-z\.]{2,6})`. The `{2,6}` quantifier requires that the pattern must match from a minimum of 2 to a maxmimum of 6 times. 

If any of these requirements are not met, then the email will not be accepted.


### Grouping Constructs

As the regex becomes more complex, you may need to break up the strings into different sections in order to fulfill different requirements. Those different sections are called grouping constructs. They are split into differnt grouping constructs by using parentheses. Each section within the parentheses is known as a subexpression.

`/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`

In our email regex above, we have 3 different subexpressions. This means that our regex is split into 3 grouping constructs, and we have 3 requirements that we want to fulfill. 


### Bracket Expressions

Bracket expressions represent a range of characters that we want to match. They outline the characters that we want to include. You can insert any characters you wish to include inside of brackets (`[ ]`) by following these guidelines:
- `[a—z]` — the string can contain any lowercase letters from a to z (will only look for lowercase letters)
- `[0—9]` — the string can contain any number from 0 to 9
- `[_-] — the string can contain an underscore or hyphen;
- You can also define any special characters that you wish to include in your regex

`/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`

So in the case of our email regex, we are looking for any lowercase letters from a to z, any numbers from 0 to 9, and for any special characters such as underscores, hyphens, backslashes, and periods.

This means that the input email can meet any of these requirements, but is not required to meet all of hte requirements. Even if it meets 1 of the requirements, it will still be accepted. 


### Character Classes



### The OR Operator



### Flags



### Character Escapes



## Author


A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)
