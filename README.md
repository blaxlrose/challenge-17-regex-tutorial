# Challenge 17: The Regex Tutorial

A Regular Expression, Regex for short, is a string of text that helps you search for specific text. This is achieved by combing special character operators. For example, when you press cmd + F on Mac, or ctrl + F in Windows, to search words or numbers to match in the VS Code text editor, you will find ".*" symbol. This button will allow you to search using regex. 



## Summary

For this tutorial, you will learn how to search for both five and nine digit zip codes in a text file. The regex for a 5 digit zip is `\b\d{5}\b`. The regex for a nine digit zip code with a hyphen in the middle is `\b\d{5}(?:-\d{4})\b`. Each regex is made up of a combination of components that provide a special purpose. The components used and their specicfic purpose for this search can be forund in the Table of Contents below.
 

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Character Classes](#character-classes)
- [Grouping Constructs](#grouping-constructs)
- [How to Use](#how-to-use)
- [Search Examples](#search-examples)

## Regex Components

### Anchors
`\b`: word boundary anchor. It is a zero-width assertion that matches the position between a word character.

### Character Classes
`\d`: Digit character class. It matches any single digit from 0 to 9.<br>
`-`: The Hypphen is a literal character that separates the first five digits from the last four digits in a nine digit zip code.

### Quantifiers
`{5}`: It specifies that the preceding `\d` should occur exactly 5 times.<br>
`{4}`: It specifies that the preceding `\d` should occur exactly 4 times.

### Grouping Constructs
`(?:)`:This is a non-capturing group. `(?:)` is used to group multiple elements together without creating a capturing group. It matches a hyphen `(-)` followed by four digits `(\d{4})`. 

### How to Use
1. Start by obtaining the text or data you want to search for zip codes. Use a programming environment or text editor   
   that supports regex search. You can use programming languages like Python, JavaScript, or tools like Notepad++ or RegexBuddy. For example, if you hit cmd + F on Mac, or ctrl + F in Windows, a search window with a regex search option '.*' will appear. You can type either regex in after hitting this button.

   For the regex \b\d{5}\b:

   \b represents a word boundary, ensuring that the regex matches whole words.
   \d{5} matches five consecutive digits, representing the entire zip code.
   \b represents another word boundary to complete the match.

   For the regex \b\d{5}(?:-\d{4})\b:

   \b represents a word boundary, ensuring that the regex matches whole words.
   \d{5} matches five digits consecutively, representing the main part of the zip code.
   (?:-\d{4}) is a non-capturing group that matches a hyphen followed by four digits. This part represents the optional extended part of the zip code.
   \b represents another word boundary to complete the match.

2. The regex will match any zip code in the format "12345" or "12345-6789" within the given text or data. It will 
   disregard partial matches or zip codes embedded within other text.


### Search Examples

1. Andy and Opie live at 322 Maple St.    
   Mayberry, NC 28382.<br>
2. The President lives at 1600 Pennsylvania 
   Avenue NW, Washington, DC 20500-0005.<br>
3. The Flintstones live at 301 Cobblestone  
   Way, Bedrock 70777.<br>
4. Jerry lives at Apartment 5A, 129 West 
   81st Street, New York, NY 10024-7207. <br>
   

## Author

Christopher Brown is a student currently enrolled in the EDX FullStack Bootcamp at the University of Richmond.<br>
Regex Gist:https://gist.github.com/blaxlrose/665a6bcdd4c56ec6425e226fb92c2f39<br>
Github: https://github.com/blaxlrose
