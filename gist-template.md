# Regex Tutorial: Matching an Email

# Introduction to Regex

A regular expression, regex for short, is a sequence of characters that defines a search pattern for text. Regex utilizes "literal characters' in order to identify the exact character or pattern(s) you are searching for within a body of text.

In this tutorial, we will be focusing on a specific regular exrpession,`/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`, matching an Email.

# Summary

Regex: `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`

This regex pattern is intended to validate email addresses with a specific structure of username@domain.extension, where the username can contain letters, numbers, underscores, periods, and hyphens.

# Table of Contents

- [Explanation of the Regex](#anchors)
- [Breakdown of Components](#quantifiers)
- [Examples & Explanations](#or-operator)
- [About the Author](#author)

# Explanation of the Regex

The following regular expression can be used to verify that user input is a valid email address:

`/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`

Anchors will match at the start and end of the string. The capturing group for the username and domain part of the email consists of lowercase letters, numbers, underscores, periods, and hyphens. The + allows for one or more characters.

# Examples & Explanation

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
