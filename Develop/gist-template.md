# Regular Expression Tutorial For An Email Address

A regular expression is a sequence of characters that define a search pattern in text. This is a RegEx tutorial for checking that a string fulfills the requirements for an email address.  

## Summary

This regular expression is used to validate an email address format by checking for a local part, an @ symbol, a domain part, a dot separating the domain and top-level domain, and finally a valid top-level domain with 2 to 5 alphabetic characters.

The RegEx below is for validating an email address:

````
^([a-zA-Z0-9_\-\.]+)@([a-zA-Z0-9_\-\.]+)\.([a-zA-Z]{2,5})$
````

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

The characters ^ and $ are both considered to be anchors. The ^ anchor signifies a string that begins with the characters that follow it. The $ anchor signifies a string that ends with the characters that precede it. 

        ^   This symbol indicates the start of the string. It ensures that the email address starts from the beginning of the input string.

        $   This symbol indicates the end of the string. It ensures that the email address ends at this point in the input string.

### Quantifiers

Quantifiers set the limits of the string that your regex matches. Quantifiers can be made lazy by adding the ? symbol after it, meaning it will match as few occurrences as possible.

        +    This quantifier specifies that the preceding character class should match one or more times.

        {2,5}    This quantifier specifies that the preceding character class should match between 2 to 5 alphabetic characters.

### OR Operator

The logical OR operator ( || ) returns the boolean value true if either or both operands is true and returns false otherwise. In this RegEx example for an email address, there is no OR operator. 

### Character Classes

A character class matches any one of a set of characters. It is used to match the most basic element of a language like a letter, a digit, a space, a symbol, etc. 

        [a-zA-Z0-9_\-\.]+    This character class [...] matches any single character inside the brackets. In this case, it matches alphabetic characters (both uppercase and lowercase), numbers, underscore _, hyphen -, and dot ..

        @    This symbol matches the literal @ character in the email address.

        \.   This matches the literal dot . character that separates the domain name from the top-level domain. It is a character escape.

### Flags

Flags are placed at the end of a regex, after the second slash, and they define additional functionality or limits for the regex. There are six optional flags that can be used, either separately or together and in any order, but these are the three you're most likely to encounter: g-Global search, i-Case-insensitive search, m-Multi-line search.

### Grouping and Capturing

The primary way you group a section of a regex is by using parentheses (()). Each section within parentheses is known as a subexpression. Subexpressions look for an exact match. Grouping constructs have two primary categories: capturing and non-capturing. Capturing groups capture the matched character sequences for possible re-use (including a numbered backreference) while non-capturing groups do not. A grouping construct can be made non-capturing by adding the characters ?: at the beginning of an expression inside the parentheses.

        ([a-zA-Z0-9_\-\.]+)  This part matches the local part of the email address before the @ symbol. 

        ([a-zA-Z0-9_\-\.]+): This part matches the domain part of the email address after the @ symbol.

### Bracket Expressions

Anything inside a set of square brackets ([]) represents a range of characters that we want to match. 

        [a-zA-Z]     This character class matches alphabetic characters (both uppercase and lowercase) for the top-level domain.

### Greedy and Lazy Match

Greedy means your expression will match as large a group as possible, lazy means it will match the smallest group possible.

### Boundaries

Boundary markers such as ^ and $ allow you to anchor the regex pattern to the beginning and end of the string. This means that when you want to match a literal ^ or $ , you need to escape these special characters with a backslash.

### Back-references

A backreference refers to the submatch of a previous capturing group and matches the same text as that group.

### Look-ahead and Look-behind

A lookahead assertion "looks ahead": it attempts to match the subsequent input with the given pattern, but it does not consume any of the input — if the match is successful, the current position in the input stays the same. 

A lookbehind assertion "looks behind": it attempts to match the previous input with the given pattern, but it does not consume any of the input — if the match is successful, the current position in the input stays the same. It matches each atom in its pattern in the reverse order.

## Author

Robin Langton is a junior full-stack web developer. You can find more of her projects posted on her [Github page](https://github.com/rrlangton)!
