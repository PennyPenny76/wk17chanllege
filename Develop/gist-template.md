# A regex tutorial about a matching a URL 

```md
This is a regex tutorial of macthing a URL.

```

## Summary

Briefly summarize the regex you will be describing and what you will explain. Include a code snippet of the regex. Replace this text with your summary.

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Grouping Constructs](#grouping-constructs)
- [Bracket Expressions](#bracket-expressions)
- [Character Classes](#character-classes)
- [The OR Operator](#the-or-operator)
- [Flags](#flags)
- [Character Escapes](#character-escapes)

## Regex Components

`/^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/`

------ `(https?:\/\/)? ` ------

* `https`: mathes exactly `https`.
* `？` in `https?` mathes `s` zero or one time.
* `:`: mathes `:`.
* `\/\/`: mathes `//`.
* The second `？` in `(https?:\/\/)?` means `(https?:\/\/)` zero or one time.

------ `([\da-z\.-]+)\.` ------

* `\d`: mathes numbers `0-9`.
* `a-z`: mathes letters `a-z`.
* `\.`: mathes `.`.
* `-`: mathes `-`.
* The `+`the elements in  `[\da-z\.-]` one or more time.
* `([\da-z\.-]+)` is a grouping constructs.

------ `([a-z\.]{2,6})` ------

* `a-z`: mathes letters `a-z`.
* `\.`: mathes `.`.
* `{2,6}`: matches the elements in `[a-z\.]`from a minimum of 2 number of times to a maximum of 6 number of times.
* `([a-z\.]{2,6})` is a grouping constructs.

------ `([\/\w \.-]*)*` ------

* `\/`: mathes `/`.
* `\w`: mathes letters `a-z`, letters `A-Z`, special character `-`, numbers `0-9`.
* `-`: mathes `-`.
* The first `*` matches the elements in `[\/\w \.-]` zero or more time.
* The second `*` matches the whole pattern `[\/\w \.-]` to show zero or more time.

## `\/?` ---

* `\/`: mathes `/`.
* `？` mathes `/` zero or one time.

### Anchors


* `^` : The `^` anchor signifies a string that begins with `http`.


* `$` : The `$` anchor signifies a string that ends with `/`.


### Quantifiers

* `？` : The `？` matches the pattern zero or one time.

The first `？` in `(https?:\/\/)?` means `s`  zero or one time.

The second `？` in `(https?:\/\/)?` means the pattern `(https?:\/\/)` zero or one time.

* `*` : The `*` matches the pattern zero or more time.

The `*` in `[\/\w \.-]*` means the URL allows the elements in `[\/\w \.-]` to show zero or more time.

The second `*` in `([\/\w \.-]*)*` matches the whole pattern `[\/\w \.-]` to show zero or more time.

* `+` : The `+` matches the pattern one or more time.

The `+` in `[\da-z\.-]+` means the URL allows the elements in `[\da-z\.-]` to show one or more time.

* `{2,6}`: Matches the pattern `[a-z\.]`from a minimum of 2 number of times to a maximum of 6 number of times

### Grouping Constructs

The Regex has 4 grouping constructs, which are:

`(https?:\/\/)` 
`([\da-z\.-]+)`
`([a-z\.]{2,6})`
`([\/\w \.-]*)`

### Bracket Expressions

The Regex has 3 bracket expressions, which are:

`[\da-z\.-]`
`([a-z\.])`
`([\/\w \.-])`

### Character Classes

* `\d`: mathes numbers `0-9`.
* `\w`: mathes letters `a-z`, letters `A-Z`, special character `-`, numbers `0-9`.

### Character Escapes

* `\/\/`: mathes `//`.
* `\.`: mathes `.`.
* `\/`: mathes `/`.

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)
