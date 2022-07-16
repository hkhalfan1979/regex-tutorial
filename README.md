# Regex Tutorial

A regular or rational expression defined as characters in a pattern or a sequence that replace or find string operations which may be useful locating a string in a URL.

## Summary

In this tutorial, I'm going to introduce one of the more commonly used Regular Expressions and, by describing how it works, explain some important regex concepts. A regex is a set of characters that defines a search pattern within a text. This can be used to find such items as usernames, emails, hex values, URLs, or HTML tags. For the purposes of this article, we are going to look at a specific example used to match emails, break it up into its various components, and explain what each component does. You can find our example below.

```
Matching an Email: /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/
```

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

The two anchors in regex are ^ and $.

Succeeding the first forward slash, you will find the circumflex (^) and a dollar sign ($) proceeding the final forward slash. Theses symbols are both considered anchors, which denote the beginning and end of the expression. The circumflex (^) denotes the start of a string. The dollar sign ($), on the other hand, denotes the end of the string.

### Quantifiers

Quantifiers will measure and set the limit on the the number of characters that we are wanting to match in our Regex, we used `+` to communicate there is another sequence to be matched as a quantifier. We also use `{2,6}` as another quantifer to specify the input should be a minimum of 2 characrtors to a maximum of 6 characters.

### Grouping Constructs


### Bracket Expressions

### Character Classes

A character class can define a set of characters that can occur in input strings to fullfill a match. The bracket expressions mentioned previously are examples of this. There are two more examples that can be found in our email example.

The \d character class in the above code is looking for any digits, whereas a \D looks for non-digits, \s searches for space symbols, tab and newlines, \S looks for all but \s, \. any characters with the regex 's' flag, while the included \w character is looking for an alphanumeric character.


### The OR Operator

### Flags

### Character Escapes

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)