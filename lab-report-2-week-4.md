# Lab Report - Week 4

## Bug 1: Link Inside of Parenthesis

These are the code changes made in order to fix this bug:
![link in parentheses fix](link_in_parentheses_fix.png)

Using [this failure-inducing input](https://github.com/Daniel-P-Arevalo/markdown-parser/blob/main/test-file-1.md) that has a link in parentheses an out of memory error is produced as the symptom of this bug when given this input.
![link in parentheses error](link_in_parentheses_error.png)

This out of memory error symptom happens becuase there is text after the link, so MarkdownParse continues to look for another link in the file, which causes an infinite loop. This loop only ends when it runs out of memory resulting in the symptom we saw. Adding a check for if any of the variables are -1 tells the program to stop when there is no more links by breaking it out of the loop.

## Bug 2: Images

These are the code changes made in order to fix this bug:
![image fix](image_fix.png)

When we use [this failure-inducing input](https://github.com/Daniel-P-Arevalo/markdown-parser/blob/main/test-file-2.md) that has an image instead of a link an array containing the image name in the file is returned, which we don't want as it should only return links in the file meaning that this is a symptom of a bug.
![image error](image_error.png)

The reason behind this symptom is that with the failure-inducing input an image has almost exactly the same syntax as a link in a markdown file. Due to not having a check for that explanation mark the program adds the image to the array becuase it sees it as a link due to it being in a similar format. Adding a check for the explanation mark before the opening bracket prevents this from happening.

## Bug 3: No Brackets

These are the code changes made in order to fix this bug:
![no brackets fix](no_brackets_fix.png)

By using [this failure-inducing input](https://github.com/Daniel-P-Arevalo/markdown-parser/blob/main/test-file-3.md) of a link in parentheses and no brackets we get an empty array instead of the excepted array with the link, so this is a symptom of a bug.
![no brackets error](no_brackets_error.png)

The lack of brackets in the file causes the loop to break prematurely and not add anything. This results in it returning the empty array that we saw as a symptom of the bug. By adding an extra condition that checks for only the brackets being -1 before the loop break it ensures that the the link gets added to the array despite the lack of brackets.
