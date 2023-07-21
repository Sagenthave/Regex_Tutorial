# Regex: Creating a Modern Rosetta Stone
<!-- Introductory paragraph (replace this with your text) -->
Regex, also known as Regular Expressions doesn't necassarily belong to any form of development. The simplist way I can begin to explain it to you is comparing it to one of the most famous discoveries in archoloigal history; the Rosetta Stone. Before the Rosetta Stone was discovered the ancient Egyptians language was lost in transation until they found a stone that had the ancient Egyptions language side by side another language we could already read. That is Regex. Regex can be thought of as another language that has been directly translated into an encrypted format with very specific rules. As long as we know the rules we can figure out what it is saying. 

## Summary
<!-- Briefly summarize the regex you will be describing and what you will explain. Include a code snippet of the regex. Replace this text with your summary. -->
The regex I will be describing is matching an encrypted email to a standard one. 

- Email: /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/
- Though it may not look like it. The utter nonsense you see above is in face an email. In this tutorial I will be breaking down the set of rules used to devise this line and how it can be made to make a sensible email you might see in your day-to-day life.

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
- Regex means it follows a literal pattern and to signify this the entire encryped message is wrapped inbetween slash characters (/). This signifies that the pattern does not change. For example is abc is written at the beginning, end, or middle of the encryped expression, it does not change what is stands for. 
- You can see below that the example email expression is wrapped in slashes. 
## /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/



### Anchors
- Anchors are not meant to be viewed as charactars. Instead you can view them as signals that place characters before, after, or inbetween. Please not that not all the possible anchors will be viewed in this tutorial. For a full list please search the Web. 
- Anchors in the example are the the following: 
- ^ $
- ^ signals that the following character is that start of the character string for the expression. 
- $ signals that the string expression has come to a end with the character listed before it. 
## /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/
- In the example provided we can see the expression is wrapped in slashes. Starts after ^ and ends with the symbol before $. So we will be looking at ([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6}) for our hidden email.


### Quantifiers

### OR Operator

### Character Classes

### Flags

### Grouping and Capturing

### Bracket Expressions

### Greedy and Lazy Match

### Boundaries

### Back-references

### Look-ahead and Look-behind

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)
