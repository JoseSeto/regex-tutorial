# Matching HEX values

The following tutorial will go over how to match a regular expression, or regex, for HEX values. Each section will cover a specific part of the regex and explain that section of the regex.

## Summary

Briefly summarize the regex you will be describing and what you will explain. Include a code snippet of the regex. Replace this text with your summary.

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [OR Operator](#or-operator)
- [Character Classes](#character-classes)
- [Flags](#flags)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)
- [Greedy and Lazy Match](#greedy-and-lazy-match)
## Regex Components

### Anchors

`/^`#?([a-f0-9]{6}|[a-f0-9]{3})`$/`

The first component that we will break down are the anchors. As shown in the highlighted portion of the regular expression, the components that are highlighted are called anchors. Anchors are used at the start and end of a string or expression. In this case `/^` and `$/` signify the beginning or end of our expression.

### Quantifiers

/^#`?`([a-f0-9]`{6}`|[a-f0-9]`{3}`)$/

Next up, quantifiers. Quantifiers are used to communicate how many characters are expected. Quantifiers specify how many instances of a character, group, or character class must be present in the input for a match to be found. By default, quantifiers are greedy, which we will go over in more detail later in the tutorial, and will match as many characters as possible. If the "*,+,?,{}"* characters are found within regular expressions, they are considered quantifiers. The `?` indicates the expression to match 0 or 1 time. As mentioned in the summary above because there are 2 types of formats we'll use the or operator to distinguish which format we are using. In our Hex Value regular expression we have `{6}` (Hex Triplet Format) and `{3}` (Shorthand Hex Format), this indicates that the length of the component preceding these quantifiers should be 6 for `{6}` and 3 for `{3}`. 

Hex Triplet Formats Include:
#000000, #FFFFFFF, #0099CC

### OR Operator

/^#?([a-f0-9]{6}`|`[a-f0-9]{3})$/

The next component we will be discussing is the "or" operator. The "or" operator within a regular expression is defined using the `|` element. The or operator indicates that it could either of the components that we are separating with the `|`. For our hex value regular expression we have ([a-f0-9]{6}`|`[a-f0-9]{3}). Note the or operator separating these 2 components. This means that our hex value could either be 6 characters `[a-f0-9]{6}` or 3 characters `[a-f0-9]{3}`.

### Character Classes

### Flags

### Grouping and Capturing

### Bracket Expressions

### Greedy and Lazy Match

## Author

Written by: Jose Seto\
Github Portfolio [Jose Seto](https://github.com/JoseSeto)
