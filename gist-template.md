# A Beginner's Guide to Regular Expressions (RegEx)

Welcome to this beginner-friendly tutorial on Regular Expressions (RegEx). If you're a computer science student or a software programming enthusiast, you've likely encountered situations where you need to manipulate and search for patterns in text. RegEx is a powerful tool that allows you to do just that! In this tutorial, we'll take a step-by-step journey through the fundamental concepts of RegEx.

## Summary

In this tutorial, we will explore the basics of Regular Expressions and how to use them effectively in your programming tasks. We'll cover various RegEx components such as anchors, quantifiers, character classes, grouping, and more. Here's a quick example of a RegEx that matches email addresses:

Matching an Email – /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/


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
Anchors are used to specify the position of a match within the text. The most common anchors are ^ (start of line) and $ (end of line). For example, the pattern ^Hello will match any line that starts with "Hello". Similarly, the pattern world$ will match any line that ends with "world".

### Quantifiers
Quantifiers define how many times a character or a group of characters should appear. Examples include * (zero or more times), + (one or more times), and ? (zero or one time). For instance, the pattern a+ matches one or more consecutive 'a' characters. The pattern [0-9]{2,4} matches a sequence of digits that is at least 2 characters long and at most 4 characters long.

### OR Operator
The OR operator (|) allows you to match either one pattern or another. For example, the pattern apple|orange will match either "apple" or "orange". So, if you search for this pattern in a text, it will find occurrences of both "apple" and "orange".

### Character Classes
Character classes let you define a set of characters to match at a specific position. For instance, the pattern [aeiou] will match any vowel character. You can also use character ranges like [a-z] to match any lowercase letter.

### Flags
Flags are optional modifiers that affect how a RegEx is interpreted. They can control case sensitivity, multiline matching, and more. For example, the i flag is used for case-insensitive matching. So, with the pattern example, the i flag will make it match "example", "Example", "EXAMPLE", and so on.

### Grouping and Capturing
Parentheses ( ) are used for grouping characters or subexpressions. They also capture the matched text, which can be referred to later. For instance, the pattern (abc) will match "abc" and capture it for later use. This captured group can be referenced as \1 or $1 in some programming languages.

### Bracket Expressions
Bracket expressions allow you to specify a range of characters. For example, the pattern [0-9] will match any digit. You can also combine multiple ranges and characters in a single bracket expression like [a-zA-Z0-9] to match alphanumeric characters.

### Greedy and Lazy Match
Quantifiers are greedy by default, meaning they match as much text as possible. Adding ? after a quantifier makes it lazy, matching as little text as possible. For instance, .*? matches the shortest possible sequence of characters. Consider the pattern <.*> applied to the text <a> <b>. The greedy match will result in <a> <b> being matched together, while the lazy match will result in <a> being matched separately from <b>.

### Boundaries
Word boundaries (\b) help you match patterns at the beginning or end of words. For example, the pattern \bword\b will match the whole word "word". So, it will match "word" in the text "This is a word." but won't match "wordpress" because it's not a whole word.

### Back-references
Back-references (\1, \2, etc.) allow you to match the same text that was previously matched by a capturing group. For example, the pattern (abc)\1 will match "abcabc". This is particularly useful when you want to ensure that a certain pattern repeats consecutively.

### Look-ahead and Look-behind
Look-ahead and look-behind assertions allow you to check if a certain pattern is ahead or behind the current position, without including it in the match. (?=...) is a positive look-ahead, and (?<=...) is a positive look-behind. For instance, the pattern (?<=@)\w+ will match one or more word characters that come after the "@" symbol, effectively extracting usernames from email addresses.

## Author

This tutorial was written by Eric Fogerson. Feel free to check out my other programming-related projects on [GitHub](https://github.com/efogerson1). If you have any questions or suggestions regarding this tutorial, please don't hesitate to reach out! Happy coding!
