# Regex Tutorial

In this tutorial, I will explain the concept of Regex in relation to Email addresses. I will be breaking down each part of this Regex expression and describing what it does and how it is relevant. 

## Summary

What is Regex? Regex, also know as Regular Expressions, is a sequence of character that are used to define a search pattern for text. Historically, regex comes from a mathematical expression called regular sets, but for our purposes, they are used to define a search pattern in a body of text. For this tutorial, I will be explaining the Regex of an email address. Below is a look at the regex for email addresses. 

```
/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/
```

So why use regex? Regex allows coders to verify that a string (like email) matches basic validation characters. Regex is universal and can be used in any search to define the characters of a string. 

## Table of Contents

- [Regex Components](#regex-components)
- [Anchors](#anchors)
- [Bracket Expressions](#bracket-expressions)
- [Quantifiers](#quantifiers)
- [Character Classes](#character-classes)
- [Character Escapes](#character-escapes)
- [Conclusion](#conclusion)

## Regex Components

Let's look back at our email Regex and break it down by component. 

```
/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/
```

To start, a regex must be wrapped between the character `/` because it is considered a literal (a notion for representing a fixed value in source code). For the email regex, we can break it down by letters, numbers, and characters. 
after `/^` we see the first part of the regex 

```
([a-z0-9_\.-])
```
This is stating that the first part of you email address can contain the following:
 - letters a through z
 - Numbers 0 through 9
 - characters `_`, `\`, `.`, `-`

The `+` separates like any coded string and the `@` indicates `@` symbol of an email. 

The final piece of the email:

```
([a-z\.]{2,6})
```
Similar to the first part states the following:
 - letters a-z
 - character limit between 2 and 6

In the following sections, I will break these pieces of the regex down in detail.



### Anchors

In this (and any) regex expression, you will see anchor characters. Anchors are used to specify where the string begins. The symbols `^` and `$` are anchors and you can see these at the very start and end of our express:

```
/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/
```
`^` signifies the start of the string and `$` represents the end. In our email express, we know that our full sequence must fulfill the requirements of containing the following characters because they are within the anchors of the expression:

```
[a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]
```

### Bracket Expressions

Now that we know where our string starts, let's talk about what is in between the brackets. We briefly went over this in the contents section, but we will dive into more details. 

Our first section of brackets contains the qualifying characters for the part of an email address before the `@`.

```
[a-z0-9_\.-]
```

 1. We can use lower case letters between a and z. upper case cannot be used because they are not specified.
 2. We can use numbers between 0 and 9
 3. We can use the following special characters, `_`, `\`, `.`, `-`

Our second set of brackets lets up know what we can have in the part of our email after the `@`.

```
[\da-z\.-]
```
 1. We can have any digit to start our string, as indicated by the `\d`
 2. We can use any lower case letters between a and z
 3. We can use the following special characters, `_`, `.`, `-`

Our final set of brackets let you know what you can have in the final part of the email address after the `.`

```
[a-z\.]
```
 1. We can use any lower case letters between a and z
 2. we can use a `.` as our special character 


### Quantifiers

Quantifiers are exactly how they sound. These are limits that can be set for your string. They can be set for the string as a whole or for sections of the string. For our email regex, the quantifier is set for the last character of the string. 

```
([a-z\.]{2,6})
```

You will note that the first part of our email is not limited by our quantifier. However, we are only allowing emails to have between 2 and 6 characters in their final part of the email address. 


### Character Classes

Character classes are defined as a set of characters that can occur within a string to fulfill a match. For example, our email expression contains several character classes: 

```
/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/
```
 1. `.` matches any character except for the character to set a new line `\n`
 2. `\d` is another way of stating the `0-9` numeric qualifier


### Character Escapes

Our expression uses a character escape in several parts:
```
[\da-z\.-]
```
and

```
[a-z\.]
```

The `\` is a character escape. In regex, this means it is a character that is not interpreted literally. In the two cases above, this escape character is noting that we should look for the `.` or `-` in the first expression or the `.` in the second expression. 

### Conclusion

In conclusion, regular expressions are an important part of coding for patterns and can be helpful in validation for different strings.

## Author

About Me:

I am a Software Release Manager interested in full stack development. I am interested in learning about technologies and concepts like the one described above. For inquiries, please contact analise.giobbi@gc.com or visit my github, linked below.
![Github](https://github.com/analisegiobbi3)
