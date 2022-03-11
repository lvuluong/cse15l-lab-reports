# Lab Report 5:

## Explaination on how I found test with different results:

I found the test with different results by using the command `diff` which allow me to see all the test cause where the result is different.
And then I use the line that it provided me, then I enter the `results.txt` file which contains all the results that I use to compare the
different when using `diff`. And then I enter `vim` to then use the command `set: number` to get the lines inside the `results.txt` file,
then I just find the specific lines to find out what test cases it is.

## Test 194:

### Result of Test 194:

![Result of Test 194](https://raw.githubusercontent.com/lvuluong/cse15l-lab-reports/main/PicsForLab5/diff.JPG)

> **Test 194 is the one with the 212c212**. And in this case, the markdown-parse by Joe return `url` while my markdown-parse return nothing.


### Expectation of what Test 194 should be:
![Expectation of what Test 194 should be](https://raw.githubusercontent.com/lvuluong/cse15l-lab-reports/main/PicsForLab5/expect1.JPG)

