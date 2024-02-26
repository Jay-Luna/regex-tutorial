# Validating a Phone Number

/^\d{3}-\d{3}-\d{4}$/

## Summary

A phone number regex, also known as a regular expression, is a pattern used to validate and match phone numbers in a specific format. It ensures that phone numbers adhere to the expected structure and formatting. Applying the regex pattern to a given phone number helps determine if it is valid or not. This helps maintain data accuracy, improves user experience, and enables reliable handling of phone number inputs in applications. In this example, we will be focusing on a basic format for North American phone numbers.

The regex we will be discussing is meant to match phone numbers in the following formats:

XXX-XXX-XXXX

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Character Classes](#character-classes)
- [Flags](#flags)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)
- [Greedy and Lazy Match](#greedy-and-lazy-match)
- [Boundaries](#boundaries)
- [Back-references](#back-references)
- [Look-ahead and Look-behind](#look-ahead-and-look-behind)

## Regex Components

In the regular expression /^\d{3}-\d{3}-\d{4}$/, we will describe each of the components:

/ - The forward slash / at the beginning and end of the regular expression pattern signals that it is a regular expression literal. 

    **note** :In JavaScript, regular expressions can be defined with or without the forward slashes (/).
If you are using the regular expression in a RegExp object, you would use the forward slashes as delimiter. However, if you are using the regular expression as a method parameter or within string methods, then it's not needed.

^ - The caret symbol indicates the start of the string. It ensures that the entire string matches the following pattern.

\d{3} - This specifies exactly three digits. \d represents any digit from 0 to 9.

- - This matches a hyphen character.

\d{3} - This again specifies another three digits.

- - This matches another hyphen character.

\d{4} - This specifies four digits.

$ - The dollar sign represents the end of the string. It ensures that nothing comes after the specified pattern.

Therefore, the regular expression `/^\d{3}-\d{3}-\d{4}$/ matches phone numbers in the format "XXX-XXX-XXXX" exactly, where X represents any digit from 0 to 9.

### Anchors

Anchors are special characters used to specify the position of a match within a string. In this regex example, there are 2 anchors being used.

^ - The caret symbol (^) represents the start of the string anchor. It ensures that the pattern match must occur at the very beginning of the string.

$ - The dollar sign represents the end of the string anchor. It ensures that the pattern match must occur at the very end of the string.

By using these anchors, the regex enforces that the entire string must match the specified pattern from start to end, without allowing any additional characters or spaces before or after the phone number.
