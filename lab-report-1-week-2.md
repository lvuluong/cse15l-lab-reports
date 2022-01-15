# Lab Report 1: 

## Step 1: Installing VS Code

Goggle for "Visual Studio Code" or "VS code" and it will be the first link, go to it and click the blue download at the top right corner to get to this page. Then download the VS Code based on what computer you use.
![Screenshot 1](https://raw.githubusercontent.com/lvuluong/cse15l-lab-reports/main/downloadvscode.JPG)
You should be able to see this page when you first open VS Code with no file.
![Screenshot 1](https://raw.githubusercontent.com/lvuluong/cse15l-lab-reports/main/vs.JPG)

## Step 2: Remotely Connecting

To connect remotely, first install OpenSSH by going to the Settings, select Apps > Apps & Features, then select Optional Features. Search for SSH and make sure that you have both OpenSSH Client and OpenSSH Server. 
 ![Screenshot 1](https://raw.githubusercontent.com/lvuluong/cse15l-lab-reports/main/SSH.JPG)
 Then look for your CSE15L account [here](https://sdacs.ucsd.edu/~icc/index.php) and once you get the name of your account, open a new terminal in VS code (at the top left VS code, in the Terminal section, select New Terminal) and type in [ssh cs15lwi22zz@ieng6.ucsd.edu] where for the "zz" part will be your own account specific letters. Then type in your password for the account(the password will not show when you type, so it is like you are not typing anything but you are) and if it is your first time, they will ask to continue connecting, just type "yes" and you are done connecting remotely.
 ![Screenshot 1](https://raw.githubusercontent.com/lvuluong/cse15l-lab-reports/main/p4lab.JPG)

## Step 3: Trying Some Commands

Once you have successfully connect remotely to the UCSD server, try out some commands such as:
* cd ~
* cd
* ls -lat
* ls -a
* ls <directory> where <directory> is /home/linux/ieng6/cs15lwi22/cs15lwi22abc, where the abc is your username
* cp /home/linux/ieng6/cs15lwi22/public/hello.txt ~/
* cat /home/linux/ieng6/cs15lwi22/public/hello.txt

![Screenshot 1]()

You should be able to run these command while the last 2 you shouldn't be able to run since you do not have access to it so that is normal to happen.
## Step 4: Moving Files with scp

In order to move files from your computer to your server, you use the command scp. Specifically, in the context [scp <filename> cs15lwi22<your own 3 unique letter>@ieng6.ucsd.edu:~/]. An example of this [scp WhereAmI.java cs15lwi22adk@ieng6.ucsd.edu:~/] 