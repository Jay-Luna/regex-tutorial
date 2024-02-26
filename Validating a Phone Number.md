# Validating a Phone Number

`/^\d{3}-\d{3}-\d{4}$/`

## Summary

A phone number regex, also known as a regular expression, is a pattern used to validate and match phone numbers in a specific format. It ensures that phone numbers adhere to the expected structure and formatting. Applying the regex pattern to a given phone number helps determine if it is valid or not. This helps maintain data accuracy, improves user experience, and enables reliable handling of phone number inputs in applications. In this example, we will be focusing on a basic format for North American phone numbers.

The regex we will be discussing is meant to match phone numbers in the following formats:

XXX-XXX-XXXX

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Character Classes](#character-classes)
- [Grouping and Capturing](#grouping-and-capturing)
- [References](#references)


## Regex Components

In the regular expression `/^\d{3}-\d{3}-\d{4}$/`, we will describe each of the components:

`/` - The forward slash / at the beginning and end of the regular expression pattern signals that it is a regular expression literal. 

   <strong>note</strong>: In JavaScript, regular expressions can be defined with or without the forward slashes (/).
If you are using the regular expression in a RegExp object, you would use the forward slashes as delimiter. However, if you are using the regular expression as a method parameter or within string methods, then it's not needed.

`^` - The caret symbol indicates the start of the string. It ensures that the entire string matches the following pattern.

`\d{3}` - This specifies exactly three digits. \d represents any digit from 0 to 9.

`-` - This matches a hyphen character.

`\d{3}` - This again specifies another three digits.

`-` - This matches another hyphen character.

`\d{4}` - This specifies four digits.

`$` - The dollar sign represents the end of the string. It ensures that nothing comes after the specified pattern.

Therefore, the regular expression `/^\d{3}-\d{3}-\d{4}$/ matches phone numbers in the format "XXX-XXX-XXXX" exactly, where X represents any digit from 0 to 9.

### Anchors

Anchors are special characters used to specify the position of a match within a string. In this regex example, there are 2 anchors being used.

`^` - The caret symbol (^) represents the start of the string anchor. It ensures that the pattern match must occur at the very beginning of the string.

`$` - The dollar sign represents the end of the string anchor. It ensures that the pattern match must occur at the very end of the string.

By using these anchors, the regex enforces that the entire string must match the specified pattern from start to end, without allowing any additional characters or spaces before or after the phone number.

### Quantifiers

`{}` - these are quantifiers that define the exact number of occurrences for the digits to match the expected phone number pattern  

`{3}` - This quantifier specifies that the preceding element, `\d` (which represents a digit), should occur exactly 3 times. So, `\d{3}` matches exactly three digits in a row.

example: \d{3} is the same as \d\d\d

`-`- This matches a hyphen character literally.

`{4}` - This quantifier specifies that the preceding element, \d (a digit), & should occur exactly 4 times. So, `\d{4}` matches exactly four digits in a row.

example: \d{4} is the same as \d\d\d\d

The quantifiers `{3}` and `{4}` are used to define the specific number of occurrences of digits in the regex pattern. In this case, it enforces the pattern of three digits from 0-9, followed by a hyphen, followed by another three digits from 0-9, and finally, another hyphen and four more digits from 0-9. 

example: 911-699-9966

Because it's requiring digits, alphabets or any other characters cannot be accepted.

not accepted: 5@1-09A-BBC!


### Character Classes

`\d` - Matches any digit from 0 to 9. <br>
`-` - Matches a hyphen (-)

### Grouping and Capturing

This specific regex example is using the pattern repetition syntax {} to specify the number of occurrences for each part of the pattern. The \d{3} matches exactly three digits, followed by a hyphen (-), and then another \d{3} matches three more digits, followed by another hyphen (-), and lastly, \d{4} matches four digits.


### References

- [Regex Youtube Tutorial](https://www.youtube.com/watch?v=7DG3kCDx53c)


## Author
https://github.com/Jay-Luna
Jeah is a student at the University of California San Diego studying how to become a full stack developer.
