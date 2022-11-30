# Match an Email with a Regex Tutorial

Regular expressions are a sequence of characters we use to specify a search pattern. This tutorial breaks down the components of a regex used to match emails. The regex used to match an email is `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`. Matching an email can be useful for a variety of purposes when building applications. 

## Table of Contents

- [Match an Email Regex](#match-an-email-regex)
- [Regex Components](#regex-components)
- [Anchors](#anchors)
- [Grouping Constructs](#grouping-constructs)
- [Bracket Expression](#bracket-expression)
- [Character Class](#character-class)
- [Quantifiers](#quantifiers)

# Regex Components

## Anchors

First, every regex is surrounded by a slash `/`. Next, the `^` and `$` are the anchors. The `^` signifies the beginning of the string, and the `$` signifies the end. 

## Grouping Constructs

After the initial anchor, `^`, the email regex is broken into three section by parentheses `()`; the first section `([a-z0-9_\.-]+)` to find the user's email, the second section `([\da-z\.-]+)` for the email service, and the last section `([a-z\.]{2,6})` for ".com". The parentheses confine the search criteria to each of three sections.

## Bracket Expression

In each section, the square brackets `[]` are used to include a range of characters in the search. The square brackets mean that the string can include any of the characters in these ranges, but it doesn't have to include all. The match email regex includes letters a-z (`a-z`)(case sensitive), 0-9 (`0-9`), and a period and hyphen (`\.-`).

## Character Class

The second section includes a character class `/d` to search for any single digit from 0-9. Also, the forward slash in front of the period, `\.` is a character escape. This allows the range to include a search for a period rather than the period's other purpose in regular expressions (to match any character). 

## Quantifiers

The first two sections are followed by a `+` character. This is a quantifier that ensures the pattern will be matched one or more times. Also, the third section uses a quantifier to limit the number of characters from 2 to 6 with `{2, 6}`.

## Conclusion

In conclusion, the first section of the match an email regex checks for one or more matches for a range of characters a-z, 0-9, and a period or hyphen. Then, the string's next character must be the `@`. 

The second section searches for one or more matches for any single digit 0-9, any character a-z, and a period or hyphen. The string's next character must be a period.

Last, the third section searches for any characters a-z and a period between 2 and 6 characters long.

---

## Author

Erica Morabito
- Full-Stack Developer
- [Github](https://github.com/ericaemorabito)
- [Portfolio](https://ericaemorabito.github.io/Erica_Morabito_Portfolio/) 
- [LinkedIn](https://www.linkedin.com/in/erica-morabito-full-stack-dev)