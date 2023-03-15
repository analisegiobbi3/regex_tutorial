# Regex Tutorial

In this tutorial, I will explain the concept of Regex in relation to Email addresses. I will be breaking down each part of this Regex expression and describing what it does and how it is relevant. 

## Summary

What is Regex? Regex, also know as Regular Expressions, is a sequence of character that are used to define a search pattern for text. Historically, regex comes from a mathematical expression called regular sets, but for our purposes, they are used to define a search pattern in a body of text. For this tutorial, I will be explaining the Regex of an email address. Below is a look at the regex for email addresses. 

```
/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/
```

So why use regex? Regex allows coders to verify that a string (like email) matches basic validation characters. Regex is universal and can be used in any search to define the characters of a string. 

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

Let's look back at our email Regex and break it down by component. 

```
/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/
```

To start, a regex must be wrapped between the character `/` because it is considered a literal (a notion for representing a fixed value in source code). For the email regex, we can break it down by letters, numbers, and characters. 
after `/^` we see the first part of the regex 

```
([a-z0-9+\.-])
```
This is stating that the first part of you email address can contain the following:
 - letters a through z
 - Numbers 0 through 9
 - characters **

The `+` separates like any coded string and the `@` indicates `@` symbol of an email. 

** figure out what the symbols mean and explain the rest

The final piece of the email:

```
([a-z\.]{2,6})
```
Similar to the first part states the following:
 - letters a-z
 - character limit between 2 and 6



### Anchors

In this (and any) regex expression, you will see anchor characters. Anchors are used to specify where the string begins. The symbols `^` and `$` are anchors and you can see these at the very start and end of our express:

```
/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/
```
`^` signifies the start of the string and `$` represents the end. In our email express, we know that our full sequence must fulfill the requirements of containing the following characters because they are within the anchors of the expression:

```
[a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]
```


### Quantifiers

### OR Operator

### Character Classes

### Flags

### Grouping and Capturing

### Bracket Expressions

### Greedy and Lazy Match

### Boundaries

### Back-references

### Look-ahead and Look-behind

## Author

About Me:

I am a Software Release Manager interested in full stack development. I am interested in learning about technologies and concepts like the one described above. For inquiries, please contact analise.giobbi@gc.com or visit my github, linked below.
![Github](https://github.com/analisegiobbi3)
