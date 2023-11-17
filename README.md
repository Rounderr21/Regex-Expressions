# Regular Expression Tutorial: Email Validation

Welcome to the Regular Expression Tutorial for Email Validation! In this tutorial, we'll explore a regular expression designed to validate email addresses. The ability to validate email addresses is crucial for ensuring data integrity in various applications. The regular expression we'll be dissecting is:

# Summary

I have created a tutorial for a simple regular expression that validates email addresses. The regular expression for this purpose is:

regex code: ^[\w\.-]+@[a-zA-Z\d\.-]+\.[a-zA-Z]{2,}$

In the following sections, we'll break down each component of this regex to understand its functionality. From anchors that define the string boundaries to quantifiers specifying the number of occurrences, we'll delve into the world of regex components. Additionally, we'll cover character classes, grouping constructs, the OR operator, flags, and character escapes. To solidify your understanding, we'll conclude with an example code snippet in JavaScript that demonstrates how to use this regular expression for email validation.

# Table of Contents

1. [Anchors](#Anchors)
2. [Quantifiers](#Quantifiers)
3. [Grouping Constructs](#Grouping-Constructs)
4. [Bracket Expressions](#Bracket-Expressions)
5. [Character Classes](#Character-Classes)
6. [The OR Operator](#The-OR-Operator)
7. [Flags](#Flags)
8. [Character Escapes](#Character-Escapes)
9. [Example code for Javascript](#Example-code)

## Regex Components

## Anchors
`^` : This anchor asserts the beginning of the string. It ensures that the match starts from the beginning of the input.

`$` : This anchor asserts the end of the string. It ensures that the match spans the entire input string.

## Quantifiers
`'+'` : The plus sign is a quantifier that matches one or more occurrences of the preceding character class or group. In this case, it applies to the character class [\w\.-] and [a-zA-Z\d\.-], allowing one or more word characters, dots, or hyphens.

`{2,}` : This curly brace quantifier matches two or more occurrences of the preceding character class. In this case, it applies to the character class [a-zA-Z], ensuring that the top-level domain (TLD) has at least two characters.

## Grouping Constructs
`()` : While not explicitly used in this regex, grouping constructs allow you to apply quantifiers to part of your regex. For example, (abc){2} would match "abcabc."

## Bracket Expressions
`[\w\.-]` : This bracket expression is a character class that matches any word character (\w), dot (.), or hyphen (-).

`[a-zA-Z\d\.-]` : Another character class that matches any uppercase or lowercase letter, digit, dot, or hyphen.

## Character Classes
`\w` : Represents any word character (alphanumeric + underscore).

`a-zA-Z` : Represents any uppercase or lowercase letter.

`\d` : Represents any digit.

## The OR Operator
`|` : The OR operator is not explicitly used in this regex. It allows you to match either the expression before or after it.

## Flags
In JavaScript, flags are used after the closing delimiter of the regular expression (e.g., /pattern/g). Common flags include:

`g` : Global search, meaning the pattern will match all occurrences in the input string.
`i` : Case-insensitive search, making the pattern match regardless of letter case.

## Character Escapes
`\.` : The backslash \ is an escape character. In this case, it escapes the dot (.) to match the literal dot character. Without the backslash, a dot in a regular expression would match any character.

## Example Code

 function validateEmail(email) {
  const pattern = /^[\w\.-]+@[a-zA-Z\d\.-]+\.[a-zA-Z]{2,}$/;
  return pattern.test(email);
}

const emailToTest = "user@example.com";`

if (validateEmail(emailToTest)) {
  console.log(`${emailToTest} is a valid email address.`);
} else {
  console.log(`${emailToTest} is not a valid email address.`);
}
In this JavaScript example:

The validateEmail function takes an email address as an argument.
The regular expression is stored in the pattern variable.
The test method of the regular expression is used to check if the provided email matches the pattern.
The result is then logged to the console.

## Author

Current Student that is learning how to code:

link to profile: https://github.com/Rounderr21

link to published gist file on github: https://gist.github.com/Rounderr21/03c63403590b3000f3575f25c52dbf14
