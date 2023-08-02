# A Regex Tutorial; 

Regular Expression, or commonly known as Regex is a sequence of characters that make up a pattern. These patterns can be used in algorithms to locate and replace specific patterns in a string. 

## Summary

In this tutorial we will be breaking down the following URL regex pattern 

<code> ^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$</code> 

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

Anchors can be found at the start or end of a string. In our URL string the symbols <code>^</code> and <code>$</code> would be anchors


### Quantifiers

Quantifiers specify the quantity a character, group, or character class must be present in the input in order for a match to be found. There are 18 types: 

![Alt text](<Screenshot 2023-08-02 at 1.02.59 PM.png>)

The following quantifiers can be found in our URL string 
- <code>?</code> = matches https
- <code>+</code> = matches a single or multiple digits, group of letters (a-z), dots (.) or hyphens (-) 1 

### Character Classes

A character class is a given sequence in brackets also known as a group <code>[]</code>  and matches it to a larger set of characters 

Our URL string contains the following character classes: 

- <code>[a-z]</code> = matches lower case letters between a-z
- <code>\w</code> = matches a single word
- <code>\d</code> = matches matches a single digit between 0-9
- <code>.</code> = matches any character 

### Flags

Flags are used to modify the behavior of the regular expression. Some commonly used flags are: 
- <code>i</code> = case insensitive matching
- <code>g</code> = global matches (all occurrences not just the first one)
- <code>m</code> = multi line matching 

In this case tha flags are: 
- <code>^</code> = denotes start of the string
- <code>(https?:\/\/)</code> = matches optional http ot https
- <code>?</code> = makes the preceding group optional 

### Grouping and Capturing

Grouping uses parentheses <code>()</code> it allows for organization and easier to identify the characters of a group

In our URL you can find the following groups: 
- <code>(https?:\/\/)</code> = this group matches optional http or https 
- <code>([\da-z\.-]+)</code> = this group is the domain name, matches 1 or more numbers, letters, dots or hyphen
- <code>([a-z\.]{2,6})</code> = the + in the previous group connects this group, matching 2-6 copies of the sequences <code>[a-z\.]</code>
- <code>([\/\w \.-]*)</code> =

### Bracket Expressions

As simple as it sounds, expressions between <code>[]</code> brackets 

Here are some bracket expressions found in our URL: 
- <code>[\da-z\.-]</code>
- <code>[a-z\.]</code>
- <code>[\/\w \.-]</code>

### Greedy and Lazy Match

Greedy and Lazy match allow you to find the longest and the shortest match respectively 

In our regex there is a 'greedy' match
- <code>([\da-z\.-]+) </code> = the <code>+</code> plus operator allows infinite character matching 

### Boundaries

Boundaries are characters that define the edges or position within the text where a match can occur 

- <code>^</code> = this symbol ensures that matches start at the beginning of the string
- <code>$</code> = this symbol ensures that the match continues until the end of the  string

### Back-references

Back-reference allow you to refer to previously matched groups within the same pattern 

No back-reference are used in our example regex 

### Look-ahead and Look-behind

## Author

Stephanie Angelito is currently a student at northwestern University Full-flex Coding Boot-camp with a background in Biology. 

Contact: 
- Email: angelitostephanie@gmail.com
- GitHub: https://github.com/sangelito