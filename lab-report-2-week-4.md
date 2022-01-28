# Lab Report 2:

## Debugging 1:

The Problem:

![Output of test-file 4](https://raw.githubusercontent.com/lvuluong/cse15l-lab-reports/main/PicsForLab2/t4.JPG)

[This is the test file that causes the problem](https://github.com/lvuluong/markdown-parse/blob/main/test-file4.md)

The Changes to fix the problem:

![Code Changes 1](https://raw.githubusercontent.com/lvuluong/cse15l-lab-reports/main/PicsForLab2/l1.JPG)

So the failure-inducing input in this case is `test-file4.md` which tried to create a link but instead of putting `[Link] (URL here)` , it use `(Link) (URL here)`. And so because of that, the code before the change tried to find for the stuff inside the `()` but in this case, there is 2 `()`, therefore confusing the code since it was expecting a `[]` follow by a `()` which holds the link, but instead it got 2 `()` so it eventually causes an infinite loops. Which is why by adding the `if` statement, it make sure that it has found a `[` inside the file, since otherwise, it would be as a `-1` and that would cause the while loop to break, and stopping the code overall.

---

## Debugging 2:

The Problem:

![Output of test-file 3](https://raw.githubusercontent.com/lvuluong/cse15l-lab-reports/main/PicsForLab2/t3.JPG)

![Output of test-file 4]()

[This is the test file that causes the problem](https://github.com/lvuluong/markdown-parse/blob/main/test-file4.md)

The Changes to fix the problem:

![Code Changes 2](https://raw.githubusercontent.com/lvuluong/cse15l-lab-reports/main/PicsForLab2/l2.JPG)






