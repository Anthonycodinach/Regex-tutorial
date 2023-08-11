# Regex Tutorial: Matching an Email

# Introduction to Regex

A regular expression, regex for short, is a sequence of characters that defines a search pattern for text. Regex utilizes "literal characters' in order to identify the exact character or pattern(s) you are searching for within a body of text.

In this tutorial, we will be focusing on a specific regular exrpession,`/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`, matching an Email.

# Summary

Regex: `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`

This regex pattern is intended to validate email addresses with a specific structure of username@domain.extension, where the username can contain letters, numbers, underscores, periods, and hyphens.

# Table of Contents

- [Explanation of the Regex](#explanation-of-the-regex)
- [Components Breakdown](#components)
- [Examples & Explanations](#examples)
- [About the Author](#author)

# Explanation of the Regex

The following regular expression can be used to verify that user input is a valid email address:

`/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`

Anchors will match at the start and end of the string. The capturing group for the username and domain part of the email consists of lowercase letters, numbers, underscores, periods, and hyphens. The + allows for one or more characters.

# Components

* `^`: Matches the begining of the string.

* `([a-z0-9_\.-]+)` Capturing group #1: Groups multiple tokens together and creates a capture group for extracting a substring or using a backreference.

* `[a-z0-9_\.-]` Character set: Match any characetr in the set between [].

* `a-z` Range: Matches a character in the range "a" to "z" (char code 97 to 122). Case sensitive.

* `0-9` Range: Matches a character in the range "O" to "9" (char code 48 to 57). Case sensitive.

* `_` Character: Matches a "_" character (char code 95).

* `\.` Escaped character: Matches a "" character (char code 46).

* `-` Character: Matches a " " character (char code 45).

* `+` Quantifier: Match 1 or more of the preceding token.

* `@` Character: Matches the "@" symbol.

* `([\da-z\.-]+)` Capturing group #2: Groups multiple tokens together and creates a capture group for extracting a substring or using a backreference.

* `[\da-z\.-]` Character set: Match any characetr in the set between [].

* `/d` Character: Matches any digit character (0-9).

* `a-z` Range: Matches a character in the range "a" to "z" (char code 97 to 122). Case sensitive.

* `\.` Escaped character: Matches a "" character (char code 46).

* `-` Character: Matches a " " character (char code 45).

* `+` Quantifier: Match 1 or more of the preceding token.

* `([a-z\.]{2,6})` Capturing group #3: Groups multiple tokens together and creates a capture group for extracting a substring or using a backreference.

* `[a-z\.]` Character set: Match any characetr in the set between [].

* `\.` Escaped character: Matches a "" character (char code 46).

* `{2,6}` Quantifier: Match between 2 and 6 of the preceding token.

* `$`: Anchors the match at the end of the string.

# Examples

Refer to the examples of how the matching email regex can be used with JavaScript to match or validate email addresses:

`const pattern = /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/;`

`// Valid Email Addresses`
`console.log(pattern.test("john.doe@example.com"));       // true`
`console.log(pattern.test("alice1234@email.co.uk"));      // true`
`console.log(pattern.test("support-info@company.net"));   // true`

`// Invalid Email Addresses`
`console.log(pattern.test(".user@domain.com"));           // false`
`console.log(pattern.test("user@domain.c"));              // false`
`console.log(pattern.test("user@domain.com-"));           // false`
`console.log(pattern.test("user@.domain.com"));           // false`

In this JavaScript code, the .test() method of the regex pattern is used to check if a given email address matches the pattern. It returns true if the email is valid according to the regex and false otherwise. 

# Author

I'm Anthony Codinach, a dynamic creative breaking into the ever expanding tech space. The intersection between technology & creativity has always intrigued me. Please enjoy my regex tutorial and I hope it serves you well in better understanding what goes on behind the curtain of JavaScript functions.

## Github Profile
https://github.com/Anthonycodinach
