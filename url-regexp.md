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
 (`/`), (`.`), (`-`) that can be matched at a certain position within the url. E.g `(https://github.com/Reynoldscode/regex-Regular...)` the hyphen after the regex is a clear example of character class. So this pattern is expecting that the url inputed should have at least one of these charcters.
 
 
 ### Flags
In Regular expressions, flags can be used to indicate options like case insensitivity, global matching, or multiline matching etc our regex pattern has no flags that should often denote a letter or combination of letters.


### Grouping and Capturing
There are four groupings in the URL regex pattern. We are going to break it down to unsderstand what each sets of group does.

### First Group
`(https?:\/\/)?` - This is the first capturing group. It captures the optional protocol part of the URL, which can be either http:// or https://. The ? quantifier makes the entire protocol part (http:// or https://) optional.

https? The https pattern matches the protocol part of the URL, which can be either http or https. The protocol" in a URL refers to the scheme or protocol used to access the resource identified by the URL. It specifies the rules and conventions for communication between clients and servers over the internet. 

The `?` quantifier makes the entire capturing group optional. This means that the protocol part of the URL may occur zero or one time in the URL string.

 `\/\/` This is used to match a double forward slash (`//`). The forward slash character `/`is a special character in regex and is used to delimit the start and end of the regex pattern.

 ### Second Group
 (`/^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/`)

 `[\da-z\.-]+`- The second capture is used to captures the domain name part of the URL. It matches one or more alphanumeric characters, digits, dots, or hyphens.

 `[ ]` This explains a character class, that matches any single character contained within the square brackets.

`\d` This is the shorthand character class that matches any digit from `0` to `9`.

`a-z` This matches any lowercase letter from `a` to `z` typing a capital leter will error out.

`\.`This matches a literal dot (`.`). The backslash `\` is used to escape the dot because in regex, the dot has a special meaning (it matches any single character except newline).

`-`` This matches a hyphen -.

`+` This quantifier matches one or more occurrences of the preceding character class or group.

### Third Group
(`/^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/`)

`[a-z\.]{2,6}` - This is the third capturing group. It captures the top-level domain part of the URL, then followed by a quantifier `2` to `6` lowercase letters or dots.

`[ ]` - This denotes a character class, which means it matches any single character contained within the square brackets.

`a-z` - This range matches any lowercase letter from 'a' to `z`.

`\.` - This matches a literal dot (`.`). The backslash `\` is used to escape the dot because in regex, the dot has a special meaning (it matches any single character except newline).

`{2,6}` - This quantifier matches the preceding character class or group between `2` and `6` times. In other words, it requires the matched characters to occur at least `2` times and at most `6` times.

### Fourth Group
(`/^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/`)
`([\/\w \.-]*)*` - This is the fourth capturing group. It captures the optional path segment of the URL. It matches zero or more occurrences of word characters, whitespace characters, slashes, dots, or hyphens.

`( and )` - These parentheses denote a capturing group. It allows us to group multiple characters together and apply a quantifier to the entire group.

`[\/\w \.-]*`- Inside the capturing group, we have a character class followed by a quantifier.

`[\/\w \.-]` - This character class matches any word character (\w), which includes alphanumeric characters and underscores, as well as slashes (\/), dots (.), spaces ( ), and hyphens (-). The backslash \ is used to escape the forward slash / and the dot . because they have special meanings in regex.

`*` This quantifier matches zero or more occurrences of the preceding character class. It allows the pattern to match sequences of any length containing the characters specified in the character class.

`*` Outside the capturing group, we have another quantifier.

`*` This quantifier applies to the entire capturing group ( ). It allows the capturing group to repeat zero or more times. This means that the entire sequence of characters matched by the capturing group, including the character class and any repetitions, can occur zero or more times.

### Bracket Expressions
(`/^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/`)
In the  parttern, there are two instances of bracket expressions, which are denoted by square brackets []. Bracket expressions define a set of characters that can be matched at a specific position within the regex pattern.


### Greedy and Lazy Match
 Greedy and lazy matching applies to quantifiers in regular expressions.

The `*` quantifier after `([\/\w \.-]*)` is greedy, meaning it will match as much as possible while still allowing the entire regex to match. This means it will match zero or more occurrences of characters like `/`, word characters`(\w)`, spaces, dots, and dashes.

If you want to make this quantifier lazy, meaning it will match as few characters as possible, you can use `*?` instead of `*`. So, the modified part of your regex would be `([\/\w \.-]*?)`.

### Boundaries
`^` character at the beginning of the regex denotes the start of the line boundary. It ensures that the match starts at the beginning of a line.
The $ character at the end of the regex denotes the end of the line boundary. It ensures that the match ends at the end of a line.

Beginning of line - `(^)` this  matches the position at the beginning of a line. It ensures that the pattern following it occurs at the start of the string or immediately after a line break.

End of line `($)`- this matches the position at the end of a line. It ensures that the pattern preceding it occurs at the end of the string or immediately before a line break.

Word boundary `(\b)` - this a position where a word character (\w) is not followed or preceded by another word character. It's useful for matching whole words.

Non-word boundary `(\B)` -  this is a position where a word character is followed or preceded by another word character.


In summary , putting all this component together will help structure

### Back-references
https://coding-boot-camp.github.io/full-stack/computer-science/regex-tutorial
https://regex101.com/

### Look-ahead and Look-behind

## Author
By: Reynolds Addy

**GitHub-Gist Link:**
[Deployed GitHub-Gist Link: Click Here]https://gist.github.com/Reynoldscode/94fa28501da39eef79fb3225508baa4f

© 2023 [Reynolds Addy]https://github.com/Reynoldscode.

**GitHub Repository:**
[GitHub Repository: Click Here]https://github.com/Reynoldscode/regex-Regular-Expression


screenshot

![alt text](<Screenshot (2049).png>)

![alt text](<Screenshot (2050).png>)

![alt text](<Screenshot (2051).png>)
![alt text](<Screenshot (2052).png>)
