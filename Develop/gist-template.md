# Title (replace with your title)

Regular Expressions, or regex, are a sequence of characters that can define a specific search pattern. They are extremely usefull for extracting information from any text by searching for matches of the search pattern. Regex can be used for several different purposes, one being text validation, such as verifying that an email address is in the correct format. Other purposes can include finding and replaicng strings, or translating data to other formats.

## Summary

The regex that will be described in the following tutorial is one that would match up with an email. Here is what the expression looks like: 
`/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`  In the tutorial, I will be going over what each compenents mean and how they could be used in other regular expressions. 

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

Ancors are components that exist at the beginning or end of a regex. `^` is used for matching strings at the beginning. For example, `^The` means that the string must start with `The`. From the email regex, notice the anchor at the beginning which reuires the email to start with a letter or a number. `$` is used for matching strings at the end. For example, `end$` means that the sring must end with `end`. Notice how this is used at the end of the email regex.

### Quantifiers

A quantifier is used to determine the amount of characters in a string. There are more variations of quantifiers than whhat will be discussed here, so be sure to research them. The main quantifier used in the email regex, `{}` indicates the range of characters that are allowed in the string. For example, `abc{2,5}` means that this must match a string that has ab followed by 2 up to 5 c. In the case of the email example, there is a `{2,6}` at the end of the regex, indicating that the length of the letters must be 2 to 6 characters long, ensuring that email endings such as .com or .net are accepted.

### Grouping and Capturing

`()` is the symbol used for grouping and capturing. This can be used in many cases, as seen in the email example, which is surrounded by parentheses on all three email components, one being `([\da-z\.-]+)`. The `()` implies which characters must be contained in the string.

### Bracket Expressions

Bracket expressions must match a string that has a range of characters within. For example, `[abc]` would match a string that containes either an a, a b, or a c. `[a-c]` would also match this. Toward the end of the email regex, notice the `[a-z\.]` This indicates that the string must contain any letter from a to z, also including the \ and . characters.

## Author

Kale Evans, [GitHub](github.com/kaletevans)
