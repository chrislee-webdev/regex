# Email Regex

This is a simple tutorial that attempts to explain the regex that matches and finds an email address. The tutorial will include the regular expression, otherwise known as regex, and examples of email addresses that will match the regex criteria

## Summary

The regex that I will attempt to explain will be one that find an email address. I will breakdown and try to explain the various characters that go in to finding a simple email address and will provide examples of what it looks like. The regex that will be use is as follows:
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
- [Final Summary](#final-summary)

## Regex Components

### Anchors
    Anchors are characters that help us denote the beginning of the end of something like a word, sentence, or string. The characters ^ and $ tell us where something starts and ends respectively. In the regex that we are using, you can see that we have used the ^ to tell us when the it starts and $ to tell us when it is the end of the regex. Eveything inbetween will help search for the individual components that make up an email address.
### Quantifiers
    Quantifiers are use to find a number of instances of words, characters, classes, etc. For example, {n} looks for an exact match to whatever n is equal to. In addition, we can specifify a minimum and maximum with the following notation {min, max}. In the regex that we are examining, you will find that in the  of the regex, we are looking for characters between 2 and 6 long with the following {2, 6}. In addition, a + looks for one or more instances of the character that precedes it. While a ? look for none or one of the character that precedes it. 
### OR Operator
    In regex there exists OR operators, denoted by | or [], that helps us find matches that either/or, and/or fits our criteria. In the regex we are examining we use [] to help us filter for email addresses. 
### Character Classes
    Character classes are the characters inside [], they help us look for anything inside of them. In our example you can see that we are looking for any lowercase letters, numbers of certain symbols that our email address may contain with the following: [a-z0-9_\.-]+ You will also notice the quantifier + that was explained previously. This tells the regex to find one or more instances of the preceding character classes.
    In our example the character class \d is also used in the following: [\da-z\.-] The \d denotes digits, so in this instance we are looking for character sets that either/or have digits between 0-9, lowercase letters, the characters . and/or -
### Flags
    Flags signify that tell us that we are lookin for patterns that fit our criteria. In our regex our entire expression is between a set of forward-slashes "/". This begins and end our search criteria. There are other flags that exists that allow us to look for certain things in our search such as "i" and "g". The "i" makes the search ignore capitalization, while "g" return all matches.

### Grouping and Capturing
    Grouping and capturing references groups of a particular search criteria and is denoted by (). In our regex we group our search throughout looking for matches that fit what we are looking for. 
### Bracket Expressions
    We use bracket expressions, [], to tell us what we are looking for by entering our serach criteria inside of the brackets. In our email example, 
    `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`
    the the first sest of brackets states we are looking for a string that contains any lowercase letters, numbers, and various characters,.
### Final Summary
    Now that we have attempted to explain some of the elements of a regex, we can go back and take a look at the regex we are examining.
    
    /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

    As we can see we start with the following 
    ^([a-z0-9_\.-]+)
    Here we have:
    1. the ^ states that the email starts with...
    2: any grouping, denoted with ()
    3: things that we are looking for are contained with an either/and/or, denoted with [],
    4: any lower case letters, numbers, an underscore, period or hyphen
    5: The + sets the criteria to any length

    The @ symbols is the literal @ that is part of an email address

    Then we have 
    `([\da-z\.-]+)`
    1: Again we start with the parentheses stating that we are looking for a grouping
    2: Again the [] tells is for either/and/or
    3: \d means any digit between 0-9, any letters, a period, a hyphen that may be in the email address
    4: the + , again, tells us that the string can be any length.

    The period, ".", like @ is the literal . that is part of an email address

    Then finally we have
    `([a-z\.]{2,6})$`
    1: Parentheses are looking for groupings
    2: Bracket are looking for the contents within it.
    3: a-z denotes any lowercase letters
    4: A literal period used in an email address such as .com
    5: The {2,6} denotes that minimum and maximum length of the string must be 2 or 6 characters long, respectively
    6: $ states that it ends with the grouping the preceded it.

    The entire expression is between two forward-slashes that tells us that this is a regular expression or regex.

## Author

My name is Chris is and I am currently attending the University of Minnesota Coding Bootcamp. After many years, I have found that I am really passionate about coding and I hope that this will lead to a career in the industry. 
Please feel free to visit my GitHub page!
https://github.com/chrislee-webdev
