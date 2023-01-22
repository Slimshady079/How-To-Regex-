# Tutorial to Regex expression

In this tutorial we will be going over some of the things that make up regex and what it can be used for! I made my own email finding regex.

## Summary

I have an email regex to display.
This is the code: `/[\w\+!$%#&-]+@[\w\+!$%#&-]+\.[\w]+/mg`

So part of this expression was joke between me and a friend of mine. Essentially we are using `/` to start the expression. The `[]` is a bracket expression to confine what we want to search. `\w` is equal to `^a-za-z0-9*` which we are trying to target in the email that is everything infront of the `+@` sign. The `!$%#&-` is part of the joke because although it will capture it, no one is going to have an email with these characters. Maybe the `!`. But including these in the bracket, means it will pick up all `^a-za-z0-9*` and the special characters infront of the `@`. After the `@` is the same expression. `+\.[\w]` This will capture everything after the . ex.(.com,.net.org) and the `/mg` is our flags! Thanks for reading!

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Grouping Constructs](#grouping-constructs)
- [Bracket Expressions](#bracket-expressions)
- [The OR Operator](#the-or-operator)
- [Flags](#flags)
- [Character Escapes](#character-escapes)

## Regex Components

Some of the regex components we will be going over are as follows down below:

### Anchors

Basically anchors just start the search engine at a specific location. This can range from the start of a match, `\G`, the start of a string, `^`, `\A`, and even ends of a string, `\Z`. `\Z` is different from, `$`, in the way that doesn't get disrupted by multiline mode! Neat!

### Quantifiers

Quantifiers help you add a numeric value as to how many of that character or characters that you'd like to find. For example, if you wanted to find only where there are six `b` you can do `b{6}`. `bbbbbb bb bbb bbbbbb`, only the first and the last segment will be highlighted. You can even add 20 b's and it'll hightlight the first 6 only!

### Grouping Constructs

Its easy to identify groupings with their parenthesis `()`. This is a great tool for specifying what exactly we want with multiple groupings! (find me this!). You can also leave comments so to speak with grouping. `(?#.. anything in here will be ignored!)`

### Bracket Expressions

These are used when you want to find exactly one character. Or even not to find it. For example. `[^tfs]` this will find any character that isn't `t` `f` or `s`! You can also try to find a range or characters using brackets. `[a-z]` this will find all lower cased alphabet letters! These are also known as character classes! Now there are some shorthands that we can do. Let's say I wanted to find all lowercase letters, uppercase letters, numbers and an underscore. I could write `[a-zA-z0-9_]` or I can just write `\w`.
Super easy!! These classes are great!

### The OR Operator

The `|` operator is silly in my eyes but there are some uses for it. You can search for things like `(cats|dogs)`. This will find what is before the `|` and what is after. You can also use it in a way to not capture a group. `(?:cats|dogs)` now you won't find cats or dogs!

### Flags

I like to think of these as tags! `/g` would be global. But you can add on a bunch like
`/gmis`. `g` = looks globally, `m` = is like `^` and `$` which is the start and end of a line, `i` = insensitive, refers to letters and does a case insensitive match and finally `s` = single line, this works together with the dot metacharacter to also match new lines!

### Character Escapes

This is our `\` we can use this to make functions very specific as well! How I showed above with our example on bracket expressions. Instead of writing `[a-zA-z0-9_]` you can use the character escape of `\w` which will include all of the previous expression. You can also do the opposite, instead of writing `[^a-za-z0-9_]` which will find everything that doesn't include the bracket expression, you can simply write \W the differce being a capital `w`.

## Author

I am Max and I like to code. Check out my code here:
Email: maximiliangibes@gmail.com
Github: https://github.com/Slimshady079
