# Lab Report - Week 10

In order to find files with differences I manually searched through files for ones that I suspected might have difference between the provided implementation and my implementation.

These are two of the files with differences that I found:

[Test File 22](https://github.com/nidhidhamnani/markdown-parser/blob/main/test-files/22.md)

[Test File 194](https://github.com/nidhidhamnani/markdown-parser/blob/main/test-files/194.md)

## Test File 22

Neither implementations are correct

This is the output of my implementation:
![file22_my_output](file22_my_output)

This is the output of the provided implementation:
![file22_provided_output](file22_provided_output)

The expected output is [ti*tle]

This is the provided implementation's code:
![provided_implementation](provided_implementation)

The problem with this implementation is that in the last if statement it only adds the potential link if it doesn't have a space in it. The potential link in this case would be /bar\* "ti\*tle", and since there is a space in between the two parts it gets skipped and not added. So you would need to make changes to that if statement that allows for spaces that are still valid and find a way to extract only the part in the quotation marks.

## Test File 194

Neither implementations are correct

This is the output of my implementation:
![file194_my_output](file194_my_output)

This is the output of the provided implementation:
![file194_provided_output](file194_provided_output)

The expected output is [title (with parens)]

This is the provided implementation's code:
![provided_implementation](provided_implementation)

The problem with this implementation is that it only considers text to be potential links if it's within parenthesis that has brackets that come before it. Due to this the invalid line url is added despite the text between the brackets and parenthesis, but the actual link outside of the parenthesis, title (with parens), is ignored. In order to fix this issue you would need to modify the beginning of the while loop where the potential link is found in order to consider text outside of brackets and parenthesis, but also invalidate links where text goes between the brackets and parenthesis.
