# Title (replace with your title)

Introductory paragraph (replace this with your text)

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
- [Boundaries](#boundaries)
- [Back-references](#back-references)
- [Look-ahead and Look-behind](#look-ahead-and-look-behind)

## Regex Components

### Anchors

Anchors are at the beginning and end of searches to check if a string fully matches a pattern, even though they themselves do not match characters. They strictly affirm a string matches a location. Anchors will create tje parameters.

    Use the anchor "^" to match the beginning of the text.
    Use the anchor "$" to match the end of the text.

### Quantifiers

Quantifiers will measure and set the limit on a number of characters you want to match in your regex. "+" searched the pattern one or more times, "?" will search zero or one time. "*" Will search the pattern zero or more times. "https?" for = example, and the "?" will make the item before optional.

### OR Operator

The purpose of an OR operator is to match the characters on the left or right of the operator. What this does is make it serve as an or, as in and/or. Using "|" in an "m|M" would allow them to match in a string. If we would have used "https?:\/\/(www\.)?[\d-a|A" it would search for "a" or "A".

### Character Classes

A character class is the set of characters that can occur in a string. The "\d" character class in the above colde is looking for any digits. Where as a "\D" would be looking for non-digits. "\s" would search for space symbols, newslines, and tabs. "\S" looks for all but "\s". But any character with a regex's flag is looking for an alphanumeric character.

### Flags

Flags will be used at the end of a regex, but after a closing slash. They act as tokens modifying the parameters of a search and multiple flags can be set by writing one after another with NO spaces. But remember, flags must be written in lowercase!! If an expression showed "Shows global expression, see below" then that would be an example of a flag. Here is an example of a URL with no flags.

"https?:\/\/(www\.)?[\d-a-zA-Z0-9@:%._\+~#=]{1,256}\.[a-zA-Z0-9()]{1,6}\b([-a-zA-Z0-9()@:%_\+.~#?&//=]*)g"

Here are some listed flag expressions:
    i: An i will ignore casing and makes expressions case-sensitive.

    s: This enables "dotall" mode with allows a "." to match newline chracter "\n"

    u: This expression means unicode. It assumes individual characters are code points and not code units. Which will match them with 32-bit characters.
    
    y: This expression is called sticky. And this means taht it will match only from the index indicated yb the "lastindex" property of this regular expression in the string. It will not attempt to match any other index.

    m:This means multiline and will give a "^" to the beginning of every line and a "$" to the end of every line.

    g: This means Global, makes an expression search for all occurences.

### Grouping and Capturing

This is a part of a pattern that can be enclosed in a "()", it is known as a capturing group. This expression has many groupings such as "https?:\/\/" which is looking for the http(s), "("www\.)?[\d-a-zA-Z0-9@:%._\+`#=] which looks for the initial domain, "[a-zA-Z0-9()]{1,6}\b([-a-zA-Z0-9()@:%_\+.~#?&//=] will look for a top level domain and "*)" file paths.

### Bracket Expressions

These are either a matching or non-matching list expression which consist of one or more expressions that are going to be in "[]", which represents a special character class and is a quantified rule providing a ranged construct. These will also adapt to a users or app's locale.

### Greedy and Lazy Match

Matching the names, a greedy match will try to find the longest possible string while the lazy match tries to find the shortest possible string.

Here are some greedy quantifiers:
    A bullet is one or more revised gist, or zero or more.
    {2,4} means two or four times as greedy as the lazy quantifier.
    ? This expression : (https?:\/\/)? uses the lazy match of ? and is looking http OR https, [a-zA-Z0-9()]{1,6} is looking for a-z, A-Z, 0-9; one to six times as greedy.


### Boundaries

Boundaries are like an anchor and uses the expression "\b" for word boundaries, but uses "\B" for non-word boundaries. They are a zero-length match that marks the beginning and end of an alphanumerical sequence and will make it easier to find whole words. The beginning of this expression \b([-a-zA-Z0-9()@:%_\+.~#?&//=]*) is searching for a whole word or digit.

### Back-references

Backreferences are filters used to match the same text previously matched by a capturing group. An example is if you wanted to search for a repeated word, the first match could use a pattern that extracts a signle word, the second would be a back reference that referes to the captured group. The above example does not include any backreferences.

### Look-ahead and Look-behind

These are zero-length assertions just like the start or end of a line, and also the start or end of a word. These are collectively called "lookaround". The difference is that lookaround actually matches characters but will give up the match when returning the result, whether there was a match or not. Hence being named assertions. They wont take up characters in the string, but only assert if a match can be made.

## Author
Name: Kevni Kica
Email: kovnin1997@gmail.com
Github: https://github.com/KevniKica
A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)
