# Lab Report - Week 8

The two versions of MarkdownParse used:
[My implementation](https://github.com/Daniel-P-Arevalo/markdown-parser)
[The reviewed implementation](https://github.com/UDXS/markdown-parser)

Snippet 1 should produce [`google.com]

Snippet 2 should produce [a.com, a.com(())]

Snippet 3 should produce [https://sites.google.com/eng.ucsd.edu/cse-15l-spring-2022/schedule]

This is how I implemented the tests in my implementation of MarkdownParse:
![my_snippet_test](my_snippet_test.png)

This is how I implemented the tests in the reviewed implementation of MarkdownParse:
![review_snippet_test](review_snippet_test.png)

For my implementation of MarkdownParse it failed for all three snippets
![my_snippet_failure](my_snippet_failure.png)

For the reviewed implementation of MarkdownParse it failed for all three snippets
![review_snippet_failure_1](review_snippet_failure_1.png)
![review_snippet_failure_2](review_snippet_failure_2.png)
