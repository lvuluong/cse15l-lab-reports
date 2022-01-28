# Lab Report 2:

## Debugging 1:

The Problem:

![Output of test-file 4](https://raw.githubusercontent.com/lvuluong/cse15l-lab-reports/main/PicsForLab2/t4.JPG)

[This is the test file that causes the problem (test-file4.md)](https://github.com/lvuluong/markdown-parse/blob/main/test-file4.md)

The Changes to fix the problem:

![Code Changes 1](https://raw.githubusercontent.com/lvuluong/cse15l-lab-reports/main/PicsForLab2/l1.JPG)

So the **failure-inducing input** in this case is `test-file4.md` which tried to create a link but instead of putting `[Link] (URL here)` , it use `(Link) (URL here)`. And so because of that, the code before the change aka **the bug** tried to find for the stuff inside the `()` but in this case, there is 2 `()`, therefore confusing the code since it was expecting a `[]` follow by a `()` which holds the link, but instead it got 2 `()` so it eventually causes an infinite loops which is the **symptom** that is shown here.

---

## Debugging 2:

The Problem:

![Output of all 3 test-files](https://raw.githubusercontent.com/lvuluong/cse15l-lab-reports/main/PicsForLab2/t5.JPG)

[This is the test file that causes the problem (test-file3.md)](https://github.com/lvuluong/markdown-parse/blob/main/test-file3.md)

The Changes to fix the problem:

![Code Changes 2](https://raw.githubusercontent.com/lvuluong/cse15l-lab-reports/main/PicsForLab2/l2.JPG)

For `test-file 3` which is the new **failure-inducing input**, it has a `()` inside the `()` which is why the **symptom** print out `[https://somet(hi]` without actually printing out the full link. Therefore, the **bug** that causes this **symptom** is that the code doesn't taken into account what if the link inside the `()` have another `()` and that the **bug** only prints out whatever is in the first `()` that it found which is what the **symptom** is.

---

## Debugging 3:

The Problem:

![Output of test-file 2](https://raw.githubusercontent.com/lvuluong/cse15l-lab-reports/main/PicsForLab2/t2.JPG)

[This is the test file that causes the problem (test-file2.md)](https://github.com/lvuluong/markdown-parse/blob/main/test-file2.md)

The Changes to fix the problem:

![Code Changes 3](https://raw.githubusercontent.com/lvuluong/cse15l-lab-reports/main/PicsForLab2/l3.JPG)

The reason this **failure-inducing input** is causing this **symptom** of `StringIndexOutOfBoundsException` is because the test-file itself has no `()` within it which causes so that the code can't find the `()`. And so the **bug** in this case is that the code doesn't taken into account what if there is no `()` within the file which causes the **symptom** when a markdown file that has no `()` is run as the input.







