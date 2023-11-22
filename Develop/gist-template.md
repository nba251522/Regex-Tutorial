# # Understanding Email Validation Using Regex(Regular Expressions)

This tutorial was created to explain how regular expressions (regex) can be used to validate email addresses. Regular expressions provide a powerful way to match patterns in strings, and in this case, ensure that email addresses are in a valid format.

## Summary

In this tutorial, we will break down the following regex, which is used to validate email addresses:

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
- `^`: This anchor asserts the start of a line.
- `$`: This anchor asserts the end of a line.
### Quantifiers
- `([a-z0-9_\.-]+)`: This part captures the user name in an email address.
- `[a-z0-9_\.-]`: This character set includes lowercase alphabetic characters, digits, underscores, dots, and hyphens.
- `+`: This indicates that the preceding character set ([a-z0-9_\.-]) must appear at least once but can be repeated multiple times. This means the user name part of the email can contain any combination and number of these characters, as long as it has at least one.
### OR Operator
While the OR operator, represented by the pipe symbol `|`, is a crucial component in many regular expressions, it is not directly used in our specific regex for email validation (`/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`). The OR operator allows for the matching of one out of several possible characters or sequences and is commonly employed in more complex regex patterns to cater to various formats or conditions. However, in the simpler form of regex for email validation we are discussing, this operator does not play a role.
### Character Classes
Character classes in regex are denoted by square brackets `[]` and allow the matching of any one character from a specified set. In our email regex, `[a-z0-9_\.-]` is a character class that matches lowercase letters, digits, underscores, periods, and hyphens.
### Flags
Flags are special tokens that modify the behavior of the regex. Common flags include:
- `g` for global search (find all matches rather than stopping after the first match),
- `i` for case-insensitive search,
- `m` for multiline search.
However, this email regex does not use any flags.
### Grouping and Capturing
Grouping is done using parentheses `()`, which not only groups parts of a regex together but also captures them for reference. In our email regex, there are three groups: `([a-z0-9_\.-]+)`, `([\da-z\.-]+)`, and `([a-z\.]{2,6})`, each capturing different parts of an email address.
### Bracket Expressions
Bracket expressions are similar to character classes. They match any one character from a set defined within square brackets `[]`. Our regex uses these in `[a-z0-9_\.-]` and `[\da-z\.-]`.
### Greedy and Lazy Match
Our email regex uses greedy quantifiers (like `+`), which match as many occurrences of the pattern as possible. Lazy quantifiers (like `+?`), on the other hand, match as few occurrences as possible, but they aren't used in this regex.
### Boundaries
Word boundaries (`\b`) are not used in our email regex. Boundaries are useful in regex to indicate positions between characters, like the start or end of a word.
### Back-references
Back-references, which refer to previously captured groups, are not used in our email regex. They are usually represented by `\1`, `\2`, etc., in regex.
### Look-ahead and Look-behind
Look-ahead and look-behind are types of zero-width assertions that check for patterns before or after certain points in the text. They are not part of our email regex pattern.
## Author Info
**Thomas Er**
- [LinkedIn](https://www.linkedin.com/in/thomas-er-9b77321b9)
- [Github](https://github.com/nba251522)
- [Portfolio](https://nba251522.github.io/thomas-er-porfolio/)
