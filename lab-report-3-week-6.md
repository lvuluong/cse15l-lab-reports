# Lab Report 3: Streamlining ssh Configuration

## ssh/config File:
![Config File](https://raw.githubusercontent.com/lvuluong/cse15l-lab-reports/main/PicsForLab3/configpic.JPG)

Here is the config file after I enter `~/.ssh/config` into VS Code so everything such as the `HostName` and the `User` was automatically there for me already. The only change that I made was to the alias, after the `Host`, and I changed it from `ieng6.ucsd.edu` to just `ucsd` so it is shorter to type and very simple for me to understand where I am `ssh` into.

## SSH using new alias:
![SSH into ucsd server](https://raw.githubusercontent.com/lvuluong/cse15l-lab-reports/main/PicsForLab3/sshucsd.JPG)

As shown here, I am trying to `ssh` into the remote server using the alias that I have set in my `config` file which is `ucsd`. And it was able to work on my first try which is what is shown in the picture. And at the end, I `exit` out of the server back to my local computer.

## SCP file to the remote server using the alias:
![SCP File to ucsd server](https://raw.githubusercontent.com/lvuluong/cse15l-lab-reports/main/PicsForLab3/scpucsd.JPG)

Here I am using `scp` to copy a new `md` file that I have created called `Week6.md` and I am trying to `scp` it into my remote server by using the new alias that I have created. And so I changed the whole part of `cs15lwi22adk@ieng6.ucsd.edu` to just `ucsd` while keeping the `:~/` at the end of it.