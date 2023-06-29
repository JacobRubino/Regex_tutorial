# Regex_tutorial
A concise tutorial on regex. The regex example I will use is: test_email123@example.com which matches to: '/^([a-z0-9_\.]+)@([a-z\.]+)\.([a-z\.]{2,})$/'

# Table of contents
- [Anchors](#ANCHORS)
- [Quantifiers](#QUANTIFIERS)
- [Grouping Constructs](#GROUPING-CONSTRUCTS)
- [Bracket Expressions](#BRACKET-EXPRESSIONS)
- [Character Classes](#CHACRACTER-CLASSES)
- [The OR Operator](#OR-OPERATOR)
- [Flags](#FLAGS)
- [Character Escapes](#CHARACTER-ESCAPES)

## Regex Components

### ANCHORS
  >The most commonly used anchors in regex are the `^` symbol, which denotes the starting of a string, specifically signifying that the pattern right next to it should start the string, and the `$` symbol, which denotes the end of the string, ensuring that the email ends. 

### QUANTIFIERS
  >Quantifiers provide additional limitations to regular expressions, examples being `*` which specifies that there will be no more occurences of the pattern, `+` which indicates that there will be at least one more occurrence of the pattern, and `?` which indicates that there will be 0 or one more occurrence of the pattern. There are also other Quantifiers known as non greedy quantifiers.
  In the example regex above, the `+` is used on multiple occasions, putting together the multiple instances of patterns, such as before the @, and after the email domain, in this case "example"  

### GROUPING CONSTRUCTS
  >Grouping constructs are used in order to group up elements in a regular expression, typically in the form of `()`. They help to apply quantifiers and alternations in a regular expression.
  In the regex example above, `([a-z0-9_\.-]+)` it is grouping up the elements in the bracket expression, with the + quantifier to connect itself with the next pattern.

### BRACKET EXPRESSIONS
  >Bracket expressions are like fancy lists in regex. It uses brackets `[]` to wrap a range of characters. Its used to match characters to characters in a set.
  In the regex above the part of `[a-z0-9_\.-]`, is grouping up that the characters in use are letters a-z, digits 0-9, and matches the . and _ characters. The `[a-z\.-]` is matching any character that is a digit, letter, period or hyphen, in this case matching the letters with the period character.

### CHARACTER CLASSES
  >A way to match common charcter types, such as /d for digits and things like `[.-_]` to match the set of characters . - and _  
  the character class of `[a-z\.]{2,}` in the regex example matches lowercase characters that are between 1-z, or a period. the `{2,}` means that its happening on 2 or more instances.
### OR OPERATOR
  >The OR operator is represetned by the | character, and it allows the specification of multiple alternative patterns. It can match either the element on the left or right of it, giving alternative choices.

### FLAGS
  >flags are used to change the behavior of a regular expression, They can control things such as case sensitivity and global matching
  if we wanted to, we could change `{2,})$/` to `{2,})$/i` to add case insensitivity, which would give uppercase and lowercase letters the same value.
 
 ### CHARACTER ESCAPES
  >Character escapes ensure that special characters are treated as literals. they are denoted by a `\` and are very commonly used. 
  The regex above uses two character escapes, both for a period character. `\.` forces the regex to treat the period as a literal character. 

  ## Author
  Created by Jacob Rubino, UCONN bootcamp student. <br />
  Github: https://github.com/jacobrubino