[Back to Home](https://smhitle.github.io/cse15l-lab-reports/)

# Lab 2

### When working with the MarkdownParse program there were several bugs that emerged as a result of testing it with different test cases. The bugs that were encountered, the symptoms that were shown and the changes to fix them can be seen below.

# Bug #1 

![Codediff1]()

The first bug that I had encountered was having trouble with the parentheses and brackets.

[TestFile1](https://smhitle.github.io/cse15l-lab-reports/Files/file2.md)

# Bug #2

![Codediff2](images/codediff1.PNG)
* During this process, a lot of infinite loops were encountered 😭

This next bug was related to having the "link" tags on two separate lines. For example this is the test file 

[TestFile2]()

This test shows () and these are the changes I made to my code in order to fix it.


# Bug #3
![Codediff3](images/codediff3.PNG)

The last bug I encountered was having spaces in between the link tags. There was also another issue with spaces, where there would be spaces in between links, but fortunately this was solved in the last code change.

[TestFile3]()

The failing output resulted in ()

![Fail3]()

Spaces inbetween either the brackets or parentheses should not be a valid link.

