# Regex Tutorial

In this tutorial, you will be able to get a breakdown of what Regex does, and how it fits in to computer science, and coding. In the example provided, you will see what each character means, and how it fits in to your code. 

## Summary

/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/
Regex (short for regular expression) is defined as a series of special characters that define a search pattern used by developers. Regex is read from left, to right. In the above code, these characters are allowed to be in a users’ email. 


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
^ and $ are anchors in Regex. ^ is to be put in the beginning, while $ is put at the end.
### Quantifiers
Quantifiers are a group of characters that serve to limit the length of email strings. In this case, the quantifiers + and would be used. A + indicates that the pattern can be matched once or more, depending on the user. There are various definitions for curly brackets depending on how many characters are present. Users will see 2,6 using this example. These numbers indicate that the email must have more than three and no more than six numbers.
### OR Operator
In order to discuss the OR Operator, we will look at the following code for matching a hex code since it is not present in the code for the given matching email code.

`/^#?

([a-f0-9]{6}|[a-f0-9]{3})

$/`

This regex employs the OR Operator to match hexadecimal codes.
This will match the starting point of the "#," which must come first and be followed by one of the following:

"[a-f0-9]6" will match a string of 6 characters long that consists of a mix of a-f letters and 0-9 numerals.

OR Operator '|'

'[a-f0-9]3' will match a 3 character string made up of a mix of the letters a through f and the digits 0 through 9.

### Character Classes

Character escapes and character classes are the two forms of character classes. The characters included in a square bracket are rendered invalid by a character escape using a backslash. It is applied in a literal sense. An escape can be thought of as a backslash in this instance. Any character found in the regex sequence is considered a member of a character class.

### Flags

The regex is enclosed by two ```/``` characters with no flags. Since multi-line is not enabled (by following the ending ```/``` with an ```m```), the anchors match a string instead of the start and end of a line. 

### Grouping and Capturing

The parenthesis "()" in this regex are used to capture a group. The username from the email address is captured in the first set of "'(),"' the domain name is captured in the second set, and the domain is captured in the last set. Disassembled: "'/([a-z0-9 .-]+)@([da-z.-]+). ([a-z\.] {2,6}) A literal "'@"' is followed by one or more characters of any digit "'0-9"', "'a-z"' (case insensitive), "'_"', "'."', or "'-"', followed by a literal "'."', followed by 2-6 characters of any digit "'a-z"' (case insensitive) or

### Bracket Expressions

Using brackets allows a regex to match specific characters in a range. So, `[a-z]` is not looking for a or - or z, but actually looking for any letters a through z. And in the brackets the "-" is not taken literally in the cases of a-z or 0-9. But after the \ to escape the period it is recognized as a literal "-".

### Greedy and Lazy Match
A greedy match will match as much as possible while the lazy match will try to match as little as possible. In matches in the email regex are greedy and will match as much as possible.

## Author

#### <a href="https://www.github.com/bannywalia">Banny Walia</a>
