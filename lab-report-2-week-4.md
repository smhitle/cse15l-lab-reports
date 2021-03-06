[Back to Home](https://smhitle.github.io/cse15l-lab-reports/)

# Lab 2

### When working with the MarkdownParse program there were several bugs that emerged as a result of testing it with different test cases. The bugs that were encountered, the symptoms that were shown and the changes to fix them can be seen below.

# Bug #1 

![Codediff1](Images/codediff2.PNG)

The first bug that I had encountered was having trouble with was checking the parentheses and brackets. An example of a test case :

Test file that caused the bug : [TestFile1](https://github.com/smhitle/markdown-parser/blob/main/file2.md?plain=1)

Screenshot of output
![Fail1](Images/fail1.PNG)

As we can see, in the test file there are multiple valid links among a series of separated brackets and parentheses. However the last link is invalid and produces the following fail output.

If we do not check and correctly take into account that there will be brackets and parentheses, where one of them might be missing, chances are high that we will encounter an infinite loop. This is because the original program had relied on using the index of the brackets/parentheses to break out of the while loop. If we check that there is indeed at least one of each, we will not experience this error.

# Bug #2

![Codediff2](Images/codediff1.PNG)
* During this process, a lot of infinite loops were encountered 😭

This next bug was related to having the "link" tags on two separate lines. For example this is the test file 

Test file that caused the bug : [TestFile2](https://github.com/smhitle/markdown-parser/blob/main/file3.md?plain=1)

Screenshot of output
![Fail2](Images/fail2.PNG)

The important thing to note in this test file is the separation of `[Link2]` and `(chickens.com)`.

The second link is outputted, even though it should not be considered a valid link due to the separation between the tags, and now there is an invalid link among a valid link. To fix this, we have to check line by line for the brackets and parentheses. We can do this via splitting each line of the file into an array and do the check.


# Bug #3
![Codediff3](Images/codedifff3.PNG)

The last bug I encountered was having spaces in between the link tags. There was also another issue with spaces, where there would be spaces in between links, but fortunately this was solved in the last code change.

Test file that caused the bug :
[TestFile3](https://github.com/smhitle/markdown-parser/blob/main/file4.md?plain=1)

Screenshot of output
![Fail3](Images/fail3.PNG)

This test contains spaces in each line, what would deem the link to be invalid is spaces between the brackets and parentheses or in themselves. The failing output resulted in the addition of a blank space.

Spaces inbetween either the brackets or parentheses should not be a valid link. If we did not take this into account, the results of the fail output of the test file is what would happen. Among the links collected when using the program, there would be multiple invalid links among valid links.

