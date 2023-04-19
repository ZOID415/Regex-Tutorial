# Challenge 17 Regular Expressions Tutorial

In this tutorial we will be learning what Regex (Regular Expression) is and how to use it. Regex is used when trying to match a certain special character combination in a string. It is mostly used to validate and pull information from a block of code. In this tutorial we will be using an example code snippet that can be used to match an email.

## Summary

This code snippet will be used throughout the tutorial to give specific examples of how regex can be used to match emails. One use for this code is to validate and make sure that an email follows the correct format. 

Matching Email-

`/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`

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

The anchor is what starts and ends the regular expression. 
In the matching email code, 

`/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`, 

 `^` and, `$` are the anchors. This code says that we are looking for something that starts with 

`^([a-z0-9_\.-]+)` and ends with `.([a-z\.]{2,6})$`. If it does not start with or end in the mentioned character sequence it is not a match.



### Quantifiers

A quantifier is used to determine how many times a specific character or group of characters needs to be present in order to have a match. For example, if we used the code:`xyz+` then this will match the string `xy` followed by at least one `z`. So, if we look at our code for matching the email:`([a-z0-9_\.-]+)` it will match any string that contains `a-z`, `0-9`, `_`, `.`, or `-`. The quantifier `+` means that it has to contain at least one of these in order to match. 

### OR Operator

In order to talk about an OR operator we will be using a different snippet of code as it is not present in the email snippet. The following code will be used for matching a hex code:
 

`/^#?([a-f0-9]{6}|[a-f0-9]{3})$/`


The mentioned Regex will match wherever it starts with `#` and followed by one of the following:
`[a-f0-9]{6}` which will match a 6 character long string that contains a combination of `a-f` letters and `0-9` numbers. 

`|` OR Operator

`[a-f0-9]{3}` it will match a 3 character long string that contains a combination of `a-f` letters and `0-9` numbers.
So in this instance the or operator allows the regex to search for a match with `[a-f0-9]{6}` `|` OR `[a-f0-9]{3}`.

### Character Classes
`/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`

`\d` is present in the given matching email code and it will match a single letter character from `a` - `z`, after the `@` symbol in the email address making sure that a letter is matched after the `@` in the email and not a number or special character.  
### Flags
A flag is an optional parameter to a regex that modifies its behavior of searching. A flag will always follow the closing forward slash of an expression, and change how it is interpreted.

A flag changes the default searching behavior of a regular expression. It makes a regex search in a different way.

A flag is denoted using a single lowercase alphabetic character.

A regex flag is not used in the matching email code that is being used for this tutorial. A regular expression typically comes in the form:

`/regex/` 

Where the slashes denote where the regular expresssion starts and ends. A flag can be used after the slash to give more guidelines for our matching. The flags are:
* `i` - `Ignore Casing`	Makes the expression search case-insensitively.
* `g`	- `Global` Makes the expression search for all occurrences.
* `s` - `Dot All` Makes the wild character `.` match newlines as well.
* `m`- `Multiline` Makes the boundary characters `^` and `$` match the beginning and ending of every single line instead of the beginning and ending of the whole string.
* `y`- `Sticky`	Makes the expression start its searching from the index indicated in its lastIndex property.
* `u`- `Unicode` Makes the expression assume individual characters as code points, not code units, and thus match 32-bit characters as well.
 
### Grouping and Capturing

`/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`

Using the email code snippet above we will talk about grouping and capturing.

`([a-z0-9_\.-]+)` is the first group that appears in our regex.

`([\da-z\.-]+)` is the second group that appears in our regex. 

`([a-z\.]{2,6})` is the third group that appears in our regex. 

Each code snippet must be true before moving on to the next group in sequence.

 
### Bracket Expressions
`/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`

Using the email code snippet above we will talk about bracket expressions.


`[a-z0-9_\.-]`, `[\da-z\.-]`, `[a-z\.]` 

The guidelines for matching the group. 

For the first code snippet, it can contain letters `a-z`, numbers `0-9`, an `_`, `-` or `.`.

The `.` is an escaped character, so it required the backslash in order to be able to be matched. 

### Greedy and Lazy Match

By defult a quantifer will attempt to match as many characters as possible as it goes through the regex string making it greedy. A lazy quantifier will attempt to match as few characters as possible as it goes through the regex string. 

### Boundaries

The following three positions are qualified as word boundaries:

Before the first character in a string if the first character is a word character.
After the last character in a string if the last character is a word character.
Between two characters in a string if one is a word character and the other is not. 

### Back-references

Backreferences match the same text as previously matched by a capturing group. Suppose you want to match a pair of opening and closing HTML tags, and the text in between. By putting the opening tag into a backreference, we can reuse the name of the tag for the closing tag.

### Look-ahead and Look-behind

If using a look-ahead or look-behind, then it has to match in a certain order. Lookaheads and lookbehinds force the main expressions to be what you have defined it as exactly otherwise it willnot be accepted as a valid input. 

## Author

This tutorial was created by Michael Alfaro.

Contact:

[GitHub](https://github.com/zoid415)

[Email](michaelalfaro93@gmail.com)
