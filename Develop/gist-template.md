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

/^#?(`[a-f0-9]`{6}|`[a-f0-9]`{3})$/

In our regex we have one character class that is repeated twice: `[a-f0-9]`. A character class matches any character enclosed in brackets. For example: `[abc]` will match "a" or "b" or "c". `[-.]` will match "-" or ".". 

Inside our character class we have two ranges: `a-f` and `0-9`. This means that it maches any character "a" through "f" (lowercase, it won't match uppercase), and "0" through "9".  Other examples: `[m-p]` matches "m", "n", "o" or "p". `[3-5]` matches "3", "4" or "5".

### Flags

/`^`#?([a-f0-9{6}|[a-f0-9]{3})`$`/

Flags are for advanced searching with a regex, in the hex code value we can see that we have a multi-line flag by using a ^ and $ at the beginning and end of the string. This allows the expression to cross multi-lines of code without breaking it.

  - `^#?([a-f0-9]{6}|[a-f0-9]{3})$` is showing that the hex value could be wrapped onto multiple lines

### Bracket Expressions
/^#?`([a-f0-9]{6}|[a-f0-9]{3})`$/

Bracket expressions in our regular expression signify the beginning of a character class or quantifier statement. In our example we use parenthesis to define our bracket expressions.

### Greedy and Lazy Match
/^#`?`([a-f0-9]{6}|[a-f0-9]{3})$/

In this section we will discuss greedy and lazy matches. A greedy match tries to match an element as many times as possible. Whereas, a lazy match tries to match an element as few times as possible. In our example we have `?` which signifies lazy quantifier. This is referred to a lazy quantifier because it causes the regular expression engine to match as few occurances as possible. We can simply turn this lazy match into a greedy one by adding a `?`.


[Top of Page](#Matching-HEX-Values)
## Author

Written by: Jose Seto\
Github Portfolio [Jose Seto](https://github.com/JoseSeto)
