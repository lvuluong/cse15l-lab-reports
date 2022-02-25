# Lab Report 4:

## Links to MarkDown-Parse Repositories:

[My Own Repository](https://github.com/lvuluong/markdown-parse)

[The Repository I Reviewed](https://github.com/QijunHuMary/markdown-parse)

## What all 3 Snippets SHOULD produce:

### Snippet 1:

![Snippet 1](https://raw.githubusercontent.com/lvuluong/cse15l-lab-reports/main/PicsForLab4/snippet1.JPG)

### Snippet 2:

![Snippet 2](https://raw.githubusercontent.com/lvuluong/cse15l-lab-reports/main/PicsForLab4/snippet2.JPG)

### Snippet 3:

![Snippet 3](https://raw.githubusercontent.com/lvuluong/cse15l-lab-reports/main/PicsForLab4/snippet3.JPG)

## My Repository:

![My Own jUnit Tests](https://raw.githubusercontent.com/lvuluong/cse15l-lab-reports/main/PicsForLab4/TestForReport4.JPG)

![Result of Running jUnit Tests](https://raw.githubusercontent.com/lvuluong/cse15l-lab-reports/main/PicsForLab4/commandLineFailure.JPG)

The circles in red is the lines that causes the jUnit Tests to fail, which is shown on the command line where it expected one
thing but was outputed something else which causes the jUnit Test to fail.

### Questions:

Question 1: No, I believed that not possible for a small code changes to 
make my program works with snippet 1 and all cases of inline codes with backticks because as shown in snippet 1, there is many different behaviors of what should be outputed based on where the 2 backticks are in. Like if one of the ticks is outside the `[]` then it would inline the whole thing that is inside the ticks but that didn't work when there was one tick outside the `()`. Meaning that if we want it to behave specifically based on where the backticks are placed, it will be much more complex to be able to be done in less than 10 lines.

Question 2: No, I believed that its not possible for a small code change to make
my program work with snippet 2 and all cases of nest parentheses, brackets, and escaped brackets because in order to deal with the first part of snippet 2, I would need to make a recursion to always check if there is another set of `[]` and `()` inside the `[]` so that if there is, I have to run the code to find the links within the `()`. Plus, to deal with the second line of snippet 2, I would then have to deal with a `()` within a `()` which required even more complex if statements to double check which would definitely required more than 10 lines of codes added.

Question 3: No, I believed that its not possible for a small code change to make my program work with snippet 3 and all cases that have newlines in brackets and parentheses because somewhere in my code, it returned null meaning that I would have to removed all my if statement that return null. And I would have to then write many if statements and changes to my code in order to take in the cases where they might be newlines within the brackets/parentheses, making it impossible to make my program be able to work with snippet 3 with less than 10 line of code change. 

## The Repository I Reviewed:

![The jUnit Tests I wrote](https://raw.githubusercontent.com/lvuluong/cse15l-lab-reports/main/PicsForLab4/Test2ForReport.JPG)

![Result of Running jUnit Tests on the Repository I reviewed](https://raw.githubusercontent.com/lvuluong/cse15l-lab-reports/main/PicsForLab4/commandLineFailure2.JPG)

The circles in red is the lines that causes the jUnit to fail since it was expected one thing but the output from the program gave a different output, meaning that they were not equal, thus causing the jUnit to fail.

### Questions:

Question 1: No, because in order to deal with snippet 1 and all cases of inline codes with backticks would required many if statements so that it can factor in all cases based on where the backticks are located, whether one of them is inside a `()` or a `[]`, and based on that, the output of the markdown would have to be different. And what if one backtick is inside a `()` which the other backtick is inside the `[]`, then what should the output be, therefore it would not be possible to make a small change and allow this program to pass all cases with inline codes with backticks.

Question 2: No, because it would required more complex changes to the code, specifically, the changes would have to check if there is any nested parentheses and if there is, what it should input. As well as whether there is any extra brackets or escaped brackets within the link, and then would have to output the right behavior for it based on where it is located, making it impossible to solve within 10 lines of code changes.

Question 3: No, because it would have to somehow deal with the newlines with in the `[]` and `()` and then being able to outputed the proper links for it. Not only that but in snippet 3, it also have an example where there is a `)` missing which mean that the could would also have to deal with that in order to work with snippet 3, therefore making impossible solve with 10 line of codes changes.  
