# Lab Report 5:

## Explaination on how I found test with different results:

I found the test with different results by using the command `diff` which allow me to see all the test cause where the result is different.
And then I use the line that it provided me, then I enter the `results.txt` file which contains all the results that I use to compare the
different when using `diff`. And then I enter `vim` to then use the command `set: number` to get the lines inside the `results.txt` file,
then I just find the specific lines to find out what test cases it is.

## Test Case 1:

### Result:

![Result](https://raw.githubusercontent.com/lvuluong/cse15l-lab-reports/main/PicsForLab5/Differen1.JPG)

*the markdown-parse by Joe return `/url` while my markdown-parse return nothing.*

### Expectation of what should be return:
`[]`

### My Personal MarkdownParse:

![My personal MarkdownParse](https://raw.githubusercontent.com/lvuluong/cse15l-lab-reports/main/PicsForLab5/mycode.JPG)

So in this case, both implementation is incorrect since my code is returning nothing because one of the variable became invalid during the 2nd while loop, causing it to break and return nothing. The bug that is happening in my personal Markdown-parse is that my code is not taking into account what happen when there is a image link within the `[]` of a link. Specifically, it is that there is a set of `()` within my `[]` so my code is returning the index of the `nextOpenBracket` as `-1` during its second loop which causes the loop to break and return nothing. To fix this, I would have to change the `if` statement from line 18 to line 21, so that it sure to check for any nested link within the `[]` and then based on that, do something about it. 

## Test Case 2:

### Result:

![Result 2](https://raw.githubusercontent.com/lvuluong/cse15l-lab-reports/main/PicsForLab5/diff2.JPG)

*the markdown-parse by Joe return `<url>` while my markdown-parse return nothing.*

### Expectation of what should be return:
`[]`

### Joe's MarkdownParse:

![Joe's MarkdownParse](https://raw.githubusercontent.com/lvuluong/cse15l-lab-reports/main/PicsForLab5/joe's%20code.JPG)

So in this case, Joe's implementation was incorrect and my implemtation return
the correct output as the expected output. So the bug that is happening in Joe's code is that the code returning the thing inside the `()` even though it shouldn't since it is for an image. And in test case 580, it is a image: `![foo](<url>)`. So to fix this bug, I would add new code after line 57 to make sure that it checks that the character before that `[` isn't a `!` since if it is, then it would be an image format and we don't want to return the things inside the `()` since it is not a url.