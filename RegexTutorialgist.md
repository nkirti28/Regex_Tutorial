# Regular Expressions Tutorial

Regular Expression, a Regex is a string of text that allows you to create patterns that help match, locate, and manage text.
This tutorial that explains how a specific regular expression, or regex, functions by breaking down each part of the expression and describing what it does.
A Regex is a sequence of characters that defines a specific search pattern. When included in code or search algorithms, regular expressions can be used to find certain patterns of characters within a string, or to find and replace a character or sequence of characters within a string.
They are also used frequently to validate input data.

## Summary

Thi Tutorial is covering and breaking down the components of the regular expression patterns used in the following example below to match hex values within a string to validate input data. This pattern is designed for color using the hexadecimal code format for color. In the web applications we can use hex triplets or RGB triplets to represent the colors on the web page. For the hex color code, there are two formats, a standard hex triplet and shorthand hex format, both formats start with a leading number sign #.

1.1 Hex Triplet Format
The hex triplet or standard hex color code uses six (hexadecimal)-digit form to represent color. For examples:

        #000000
        #FFFFFF
        #808080
        #8A2BE2

1.2 Shorthand Hex Format
The Shorthand hex uses three (hexadecimal)-digit form to represents a color. The idea is merely doubling each digit to become the above hex triplet format. For examples:

        #000
        #FFF
        #09C

/^#?([a-f0-9]{6}|[a-f0-9]{3})$/

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

- Anchor: ^
  Code Snipet: `/^#`

Description:

Anchors by themselves don't match any regular expression. Rather they assert something about the string (e.g. beginning, end) based on expressions/matching pattern next to the anchor.

- Anchor: $

Code Snipet: `$/`

Description: Matches the end of the string. Similar to the ^ anchor, $ is used to check if a string fully matches a pattern. However, $ asserts the pattern to the end of the string, not the beginning.

### Quantifiers

- Quantifier: ?

Code Snipet: `/^#?`

Description:
? implies a boolean value, 0 or 1. Typically, this makes the preceding symbol/character optional.

- Quantifier: {}

Code Snipet: `[a-f0-9]{6}`
Code Snipet: `[a-f0-9]{3}`

Description:

Quantifier indicates how many time the preceding pattern matches. Normally, the quantifiers are greedy, causing the regex to match as many occurrences of a particular pattern as possible. However, if ? was appended, the quantifier would become lazy-- causing the regex to match as few occurrences as possible. In our case, the quantifier is greedy.

### OR Operator

- OR Operator: |

Code Snipet: `[a-f0-9]{6}|[a-f0-9]{3}`

Description: The | indicator (i.e. OR indicator) is a boolean that matches either the expression before or after.

### Character Classes

Code Snipet: `a-f0-9`
Description: Character classes only matches one out of several characters defined in the character set. A hyphen can be used inside a character class to define a range of characters More than one range can be used -- as is the case in our code snipet.

### Flags

### Grouping and Capturing

### Bracket Expressions

Bracket Expression: []

Code Snipet: `[a-f0-9]`

Description: Bracket expression is a regex that will match a specific pattern of characters (alphabetic, numeric, special characters, symbols etc..) defined within the brackets. Typically a hyphen is used to describe a set or range of characters e.g. `[a-z]`. It's possible to use the ^ metacharacter to negate what is in between the brackets.

### Greedy and Lazy Match

Code Snipet: `[a-f0-9]{6}`
Code Snipet: `[a-f0-9]{3}`

Quantifier: {}

Description: Greedy means match the longest possible string. Lazy means match the shortest possible string.

### Boundaries

### Back-references

### Look-ahead and Look-behind

## Author

Hello, my name is Kirti Shelar. My main goal is to explore Javascript, Node.js, Sequelize, MySQL, CSS, HTML and other web technologies as full stack developer. My GitHub page has many projects while learning and exploring web technologies. Creating this gist is another way to describe and explore another important technology - regex.

You will continue to see new projects in the future.

GitHub: https://github.com/nkirti28
