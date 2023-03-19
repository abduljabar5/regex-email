# Email regex

Email regex, short for email regular expression, is a powerful tool used to validate and extract email addresses from text. 
## Summary

An email regex is a regular expression pattern used to validate email addresses by matching them against a specific set of rules. It checks the format and structure of an email address to ensure it follows common standards. An example of a email regex pattern is:

/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

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
The following email regex component checks for the domain part of an email address: /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/
This pattern ensures the email address contains an '@' symbol, followed by a domain name with alphanumeric characters including dots and hyphens.
### Anchors
A regex is a literal, so the pattern must be wrapped in slash characters (/). In the example above, you'll see that the regex begins with a (^) and ends with a ($). The (^) anchor represents the start of the string. By placing this anchor at the beginning of the regex pattern, it ensures that the pattern matching starts from the very beginning of the text. And by placing the dollar sign anchor at the end, it insures that the pattern matching goes on till the end.
### Quantifiers
In the following example you'll see that there are 2 Quantifiers in the expression: /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/
The (+) quantifier is used to ensure that the '@' symbol, and the domain name have at least one character, while the ({2,6}) quantifier limits the length of the TLD (top-level domain).
### Grouping Constructs
In the following expression: /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/, there are three grouping constructs, seperated by parentheses.

([a-z0-9_\.-]+): This grouping construct captures the local part of the email address (the part before the '@' symbol). It matches one or more lowercase letters, digits, underscores, dots, or hyphens.

([\da-z\.-]+): This grouping construct captures the domain name part of the email address (the part after the '@' symbol and before the last dot). It matches one or more digits, lowercase letters, dots, or hyphens.

([a-z\.]{2,6}): This grouping construct captures the top-level domain (TLD) part of the email address (the part after the last dot). It matches at least 2 and at most 6 occurrences of lowercase letters or dots.
### Bracket Expressions
In the expression: /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/, there are three bracket expressions. The first bracket expression ([a-z0-9_\.-]+) represents the local part (username) of the email address, allowing any combination of lowercase letters, digits, underscores, dots, or hyphens. The second bracket expression ([\da-z\.-]+) represents the domain name part of the email address, allowing any combination of digits, lowercase letters, dots, or hyphens. The third bracket expression ([a-z\.]{2,6}) represents the top-level domain (TLD) part of the email address, allowing a combination of lowercase letters and dots with a length between 2 and 6 characters.
### Character Classes
The regex expression has /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/ has two character classes: '\d','\'. '\d' is a shorter way of saying 0-9 and is used in the domain name part of the email address. '\' represents a literal dot (.) in the regex and is used in the domain name part of the email.
### The OR Operator
the regex: /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/ does not include the explicit OR operator '|', the bracket expressions create a similar effect by providing a choice between multiple characters in each set.
### Flags
The regex expression /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/ does not include any Flags. In JavaScript, regex have a total of 6 flags, each serving a different purpose.
### Character Escapes
The following expression has two character escapes:
/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/
'\.': The backslash \ followed by a dot . is used to escape the dot character. Because the dot represents any single character in regular expressions, it needs to be escaped with a backslash before it can be used.
'\d': The backslash \ followed by the letter 'd' represents a character class that matches any digit.
## Author

Github: https://github.com/abduljabar5
