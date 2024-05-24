# Title:
URL REGEX AND UNDERSTANDING IT'S COMPONENT.

## Description:
Welcome to my tutorial on how to use regular expression also known as Regex which defines a search pattern. It is a powerful tool that helps match a pattern and text processing task.This tutorial will dive into how to understand the characterristics of a URL parttern and how this parttern help developers validate if a user have entered the right URL pattern.

## Summary:
You will learn the pattern of a URL regex pattern aligned to javescript language.  The tutorial have noting musch to do with coding but it is tailored to developers using the language stated. We get to understand what if a given URL is valid or not. 


## Table of Contents
- [TDecription](#description)
- [Sunnary](#summary)
- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Character Classes](#character-classes)
- [Flags](#flags)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)
- [Greedy and Lazy Match](#greedy-and-lazy-match)
- [Boundaries](#boundaries)
- [Back-references](#back-references)
- [Look-ahead and Look-behind](#look-ahead-and-look-behind)

## Regex Components
`/^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/`

### Anchors
- The Anchor of the URL pattern starts with `^` which asserts the position at which the string starts. 
- The  `$` symbol asserts the end of the string or before the line terminator right at the end of the string.


example: (http:// or https://) It ensures that the string must start with the specified pattern that follows it, which in this case includes an optional http:// or https:// protocol, if present, or directly with the domain name. It is crucial for validating and preventing unwanted outcome.

### Quantifiers
Quantifiers in Regular Expressions that indicates the number of occurance a character or a group of character match in an input text. It is equally useful for tasks such as matching repeated digits.
`
ref of Regex: (`/^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/`)
The `?` quantifier is used after `(https?:\/\/)` to indicate that the preceding element (the s in https) is optional. It matches zero or one occurrence of the preceding element, allowing the URL to start with either http:// or https://, or none at all.

 The `*` quantifier is used after `([\/\w \.-]*)` to match zero or more occurrences of the preceding element. This allows for the presence of an optional path segment after the domain name in the URL. The path segment can contain any combination of word characters`(\w)`, spaces, slashes, dots, or hyphens.


### Character Classes
The character classes are sets of characters such as
 (`/`), (`.`), (`-`) that can be matched at a certain position within the url. E.g (https://github.com/Reynoldscode/regex-Regular...) the hyphen after the regex is a clear example of character class. So this pattern is expecting that the url inputed should have at least one of these charcters.
 
 
 ### Flags

### Grouping and Capturing

### Bracket Expressions

### Greedy and Lazy Match

### Boundaries

### Back-references

### Look-ahead and Look-behind

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)
