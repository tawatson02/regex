# Regex Tutorial for Phone Numbers

The goal of this challenge is to become acquainted with the syntax and structure of Regex code, and to learn how and when to use them effectively.

## Summary

^(?:\d{3}|\(\d{3}\))([-/.])\d{3}\1\d{4}$

The above is the example we are going to go over and hopefully digest to get a better understanding of how Regex works and how to effectively use it. 
Below is a breakdown in order of the example from above. 

    `^`: Starts the beginning of the string.

    `(?:\d{3}|\(\d{3}\))`: This is a non-capturing group that matches either:

        `\d{3}`: Exactly three digits.

        `\(\d{3}\)`: Three digits surrounded by parentheses.

    `([-/.])`: This captures a single character that can be a hyphen (`-`), forward slash (`/`), or a dot (`.`).

    `\d{3}`: Exactly three digits.

    `\1`: This is a backreference to the first captured group. Example: `([-/.])` 

    `\d{4}`: Matches exactly four digits.

    `$`: This is found at the end of the string.

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
Anchors are used to assert the postion within a string. 
    Common anchors are:

    `^`: Starts the beginning of the string.

    `$`: This is found at the end of the string.

### Quantifiers
Quantifiers specify the number of times an element should be matched.
    Common quantifiers include: 

        `*`: 0 or more times.

        `+`: 1 or more times.
        
        `?`: 0 or 1 time.

        `{n}`: Exactly 'n' times.

        `{n,}`: 'n' or more times.

        `{n,m}`: Between 'n' and 'm' times.

In this example code we used these two different quantifiers:

    `\d{3}`: Matches exactly three digits.

    `\d{4}`: Matches exactly four digits.

### Grouping Constructs
Grouping Constructs are used to create subexpressions within a regex pattern.
 They allow for applying quantifiers to the group, capturing for backreferences, or grouping for alternation.

    `(?:\d{3}|\(\d{3}\))`: This is a non-capturing group that matches either:

        `\d{3}`: Exactly three digits.

        `\(\d{3}\)`: Three digits surrounded by parentheses.
    
    `\1`: This is a backreference to the first captured group. Example: `([-/.])` 

### Bracket Expressions
Bracket Expressions, or character classes, are used to match any one of a set of characters.

    `([-/.])`: This captures a single character that can be a hyphen (`-`), forward slash (`/`), or a dot (`.`).

    Another example:
        `[abc]`: Matches any one of `a`, `b`, or `c`.

### Character Classes
Character Classes match predefined sets of characters.

    `\d`: Matches any digit (0-9).

### The OR Operator
The OR Operator is used to match one pattern or another.

    `|`: This acts as an OR operator within the non-capturing group to match either `\d{3}` or `\(\d{3}\)` in this example. 

### Flags
Flags are not used in this regex pattern, but a flag is an optional parameter that modifies the behavior of the regex pattern.
    
     Example: `/abc/i`
        `i` (Ignore Case): Makes the regex pattern case-insensitive.

### Character Escapes
Character Escapes allow special characters to be treated literally or to use special sequences.
    Examples from this code:
        `\(`: Match the literal `(` character.

        `\)`: Match the literal `)` character.

        `\.`: Match the literal `.` character.

    Other examples include: 

        `\n`: Matches a newline character.

        `\t`: Matches a tab character.

        `\b`: Matches a word boundary.
## Author
My name is Timothy Watson. I'm currently in a full-stack software development class and working full time in the pursuit of bettering my career for myself and my family.
Github link: https://github.com/tawatson02
