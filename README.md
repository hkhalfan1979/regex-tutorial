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

Regular expressions are generally broken up into sections using parentheses () and is a way to treat multiple characters as one unit.

Look at the entire expression within the parentheses.

```
/^([a-z0-9_.-]+)@([\da-z.-]+).([a-z.]{2,6})$/
```

Between /^ and $/, there are three distinct character groups, ```([a-z0-9_.-]+), ([\da-z.-]+)```, and ```([a-z.]{2,6})```.

### Bracket Expressions

A bracket expression is anything found within brackets ([]) that creates a range of characters that tell us what we want to match within the text. In our example, we can find three bracket expressions: ```[0-9], [a-z], and [_\.-].```

[0-9] denotes any number between ```0 and 9. [a-z]``` denotes any lowercase leter from a to z. Lastly, ```[_\.-]``` denotes the special characters that can be used: underscore ```(_)```, backwards slash ```(/)```, period ```(.)```, and dash ```(-)```.

### Character Classes

A character class can define a set of characters that can occur in input strings to fullfill a match. The bracket expressions mentioned previously are examples of this. There are two more examples that can be found in our email example.

The \d character class in the above code is looking for any digits, whereas a \D looks for non-digits, \s searches for space symbols, tab and newlines, \S looks for all but \s, \. any characters with the regex 's' flag, while the included \w character is looking for an alphanumeric character.


### The OR Operator

The purpose of an OR operator is to match the characters on the left or right of the operator, essentially serving as an or, as in and/or. Using the | as in m|M would match either m or an M from the string. If we had used ```https?:\/\/(www\.)?[\d-a|A``` it would search or a OR A.

### Flags

Flags are used at the end of a regex, after a closing slash. They are tokens that will modify parameters of a search. Multiple flags can be set by writing one after another with NO spaces. Flags must be written in lowercase. This URL does not contain any flags.

```
https?:\/\/(www\.)?[\d-a-zA-Z0-9@:%._\+~#=]{1,256}\.[a-zA-Z0-9()]{1,6}\b([-a-zA-Z0-9()@:%_\+.~#?&//=]*)g
```

### Character Escapes

A character escape uses a backslash to force a regex to look at the character following the backslash instead of using it in a literal. In our example above, you can find one example, (\.). This denotes that we want the expressiion to look directly for a period (.) instead of the character class using the same symbol.

## Author

Hasnain Khalfan is currently enrolled in a full stack developer bootcamp course with UPENN Unversity.
* [Hasnain's Github](https://github.com/hkhalfan1979/)  