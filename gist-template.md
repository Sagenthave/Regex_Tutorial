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
<!-- - [Character Classes](#character-classes) -->
<!-- - [Flags](#flags) -->
<!-- - [Grouping and Capturing](#grouping-and-capturing) -->
- [Bracket Expressions](#bracket-expressions)
- [Greedy and Lazy Match](#greedy-and-lazy-match)
- [Boundaries](#boundaries)
- [Back-references](#back-references)
- [Email Examples](#email-examples)
<!-- - [Look-ahead and Look-behind](#look-ahead-and-look-behind) -->

## Regex Components
- Regex means it follows a literal pattern and to signify this the entire encryped message is wrapped inbetween slash characters (/). This signifies that the pattern does not change. For example is abc is written at the beginning, end, or middle of the encryped expression, it does not change what is stands for. 
- You can see below that the example email expression is wrapped in slashes. 
## /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

### Anchors
- Anchors are not meant to be viewed as charactars. Instead you can view them as signals that place characters before, after, or inbetween. 
- Anchors in the example are the following: ^ $
- Please not that not all the possible anchors will be viewed in this tutorial. For a full list please search the Web. 
- ^ signals that the following character is that start of the character string for the expression. 
- $ signals that the string expression has come to a end with the character listed before it. 
## /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/
- In the example provided we can see the expression is wrapped in slashes. Starts after ^ and ends with the symbol before $. So we will be looking at ([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6}) for our hidden email.

### Quantifiers
- Quantifiers are similar to anchors and are not meant to be viewed as characters. Instead you can view than as signals that show you how often a sequence can be repeated.
- Quantifiers in the example are the following: + 
- Please not that not all the possible quantifiers will be viewed in this tutorial. For a full list please search the Web. 
- The + quantifier looks inside the ([ ]) for the set of characters it is addressing and matched the pattern one or more times. 
## /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/
- In our example we can see in the plus symbols in two places. ([a-z0-9_\.-]+ and )@([\da-z\.-]+)
- a-z0-9_\.- and \da-z\.- can be repeated one or more times in the sequence.  
- This means these two sections can be repeated. For the sake of simplicity I will only multiply it once to generate an email with the encrypted expression. 

### OR Operator
- The OR Opterator (|) takes into consideration that within the bracket expression, it is not necassary for all the requiraments to been met. 
- For example: 123 can be written as 1|2|3
- In a more complex example (kyx)@(123). Possible examples of what would match are: "kyx@123", "yx@23", "x@3". 
- However, "123@kyx" would NOT be a match. 

<!-- ### Character Classes
- Not used in code -->

<!-- ### Flags
- not used in code -->

<!-- ### Grouping and Capturing
- not used in code -->

### Bracket Expressions
- Anything with [] means there are chararacters are the ones we want to include and match up. 
## /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/
- As you have probably noticed, there is a hypen between the letters and numbers. a-z and 0-9. This means that the expression can have any letters between a to z and any number from 0 to 9. Furthermore the _- in the expression within the bracket indicates the email can contain a hypen or an underscore.
- The following examples below are possible examples that can be generated from the example section: [a-z0-9_\.-]
- protect_nature-123
- books-are-the-best_12345
- 1234-12378
- _-_-_-_-

### Greedy and Lazy Match
- Greedy matches are: (*), (+), (?), and {}. 
- The symbols listed above are considered to be greedy because they want to match with as many character possibilites as possible. 
- The pattern is matched with each symbol:
- (*) zero or more times used
- (+) one or more times
- (?) zero or one time
- {} the curly brackets are what we can see in the example provided. 
   * {x} must match the pattern x times
   * {x,} must match the pattern minimun of x times
   * {x, y} must match pattern minimum x time, and maximun y times
- In out example we can see {2,6} at the end of the expression. This means it is looking for a string of charactars that is minimum of 2 characters long and maximum of 6 characters. Examples of possible strings for \.([a-z\.]{2,6}) are: 
   * .com
   * .ca 
   * .org

- In contrast to greedy matches which want to make as many matches as possible, lazy matches want to take the shortest route possible. A regular quantifier is made lazy by adding a (?) to it. You can think of it as someone who is questioning what work they can forget about to clock out of work early without getting caught. 

### Boundaries
- Boundries mark the beginning and end of the line. 
- (^) marks the beginning
- ($) marks the end 

### Back-references
- Back-referances refer back to the previous matched pattern expression. They are indicated with a (\1). Though this method is not used in our example, it can be understood as ([a-z.o.a-z\1])
- Examples that can fill this and be repeated are
   * mom
   * bob
   * dog

<!-- ### Look-ahead and Look-behind -->

## Email Examples
## /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/
- Now with all the information you have learned from the tutorial try to make up an email using the expression above. A few examples have been listed below

- save_the_planet-123@gmail.com
- rio_autumn@hotmail.ca
- sintha1991@yahoo.com


## Author
- About the Author: I am a new front/back- end developer studyign at the University of Toronto.
- GitHub Profile: https://github.com/Sagenthave 
<!-- A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile) -->
## References 
- https://www.ibm.com/docs/en/netcoolomnibus/8.1?topic=library-minimal-non-greedy-quantifiers 
- https://www.rexegg.com/regex-quantifiers.html
- https://www.gnu.org/software/sed/manual/html_node/Back_002dreferences-and-Subexpressions.html#:~:text=back%2Dreferences%20are%20regular%20expression,and%20is%20designated%20with%20parentheses.  
