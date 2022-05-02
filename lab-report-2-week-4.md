[Back to Home](https://smhitle.github.io/cse15l-lab-reports/)

# Lab 2

### When working with the MarkdownParse program there were several bugs that emerged as a result of testing it with different test cases. The bugs that were encountered, the symptoms that were shown and the changes to fix them can be seen below.

# Bug #1 

![Codediff1](images/codediff1.PNG)

The first bug that I had encountered was having trouble with the parentheses and brackets.

[Testfile1]()

# Bug #2

![Codediff2]()

This next bug was related to having the "link" tags on two separate lines. For example this is the test file 

[Testfile2]()

This test shows () and these are the changes I made to my code in order to fix it.


# Bug #3
![Codediff3]()

With the problem with spaces in between lines being already solved in the last code change,the last bug I encountered was having spaces in between the link tags.

[Testfile3]()

Spaces inbetween either the brackets or parentheses should not be a valid link. The failing output resulted in ()