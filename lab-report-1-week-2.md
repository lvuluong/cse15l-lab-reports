# Lab Report 1: 

## Step 1: Installing VS Code

Google for "Visual Studio Code" or "VS code" and it will be the first link, go to it and click the blue download at the top right corner to get to this page. Then download the VS Code based on what computer you use.
![VS code download page](https://raw.githubusercontent.com/lvuluong/cse15l-lab-reports/main/PicsForLab1/downloadvscode.JPG)
You should be able to see this page when you first open VS Code with no file.
![Opening VS code](https://raw.githubusercontent.com/lvuluong/cse15l-lab-reports/main/PicsForLab1/vs.JPG)

## Step 2: Remotely Connecting

To connect remotely, first install OpenSSH by going to the Settings, select Apps > Apps & Features, then select Optional Features. Search for SSH and make sure that you have both OpenSSH Client and OpenSSH Server, if not, you can download for it using the "Add a feature" button at the top. 
 ![OpenSSH Client/Server](https://raw.githubusercontent.com/lvuluong/cse15l-lab-reports/main/PicsForLab1/SSH.JPG)
 Then look for your CSE15L account [here](https://sdacs.ucsd.edu/~icc/index.php) and once you get the name of your account, open a new terminal in VS code (at the top left VS code, in the Terminal section, select New Terminal) and type in [ssh cs15lwi22zz@ieng6.ucsd.edu] where for the "zz" part will be your own account specific letters. Then type in your password for the account(the password will not show when you type, so it is like you are not typing anything but you are) and if it is your first time, they will ask to continue connecting, just type "yes" and you are done connecting remotely.

 ![Using SSH](https://raw.githubusercontent.com/lvuluong/cse15l-lab-reports/main/PicsForLab1/p4lab.JPG)

## Step 3: Trying Some Commands

Once you have successfully connect remotely to the UCSD server, try out some commands such as:
* cd ~
* cd
* ls -lat
* ls -a
* ls <directory> where <directory> is /home/linux/ieng6/cs15lwi22/cs15lwi22abc, where the abc is your username
* cp /home/linux/ieng6/cs15lwi22/public/hello.txt ~/
* cat /home/linux/ieng6/cs15lwi22/public/hello.txt

![Trying out Commands](https://raw.githubusercontent.com/lvuluong/cse15l-lab-reports/main/PicsForLab1/tryingoutcode.JPG)

You should be able to run these command while the last 2 you shouldn't be able to run since you do not have access to it so that is normal to happen.
## Step 4: Moving Files with scp

In order to move files from your computer to your server, you use the command scp. Specifically, in the context (scp [filename] cs15lwi22[your own 3 unique letter]@ieng6.ucsd.edu:~/). An example of this [scp WhereAmI.java cs15lwi22abc@ieng6.ucsd.edu:~/]. 

![Using SCP](https://raw.githubusercontent.com/lvuluong/cse15l-lab-reports/main/PicsForLab1/scp.JPG)

And as you can see in the picture, after I use the scp command, I then use the ssh command in order to connect remotely to the server and then I use ls in order to double check and make sure that I have made a copy of the java file and to make sure that I have move it properly into the server.

## Step 5: Setting an SSH Key

And to make an SSH key so that you don't have to put in the password everytime you connect remotely, you have to first create a key [ssh-keygen -t ed25519] which is for powershell/microsoft computer users, then have the key saved in the place it was automatically in, so just press enter, then you can enter your passphrase if you want and the key is made (Type y if you have already made a key and want to overwrite it with a new one). 

![Making SSH Key](https://raw.githubusercontent.com/lvuluong/cse15l-lab-reports/main/PicsForLab1/makingprivatekey.JPG)

Now you have to copy the public to the ssh directory of your server by first ssh into your server, type [mkdir .ssh], then [exit] which will log you out of the server and back to your computer. Then type [scp (/Users/joe/.ssh/id_rsa.pub) cs15lwi22@ieng6.ucsd.edu:~/.ssh/authorized_keys] with the directory being the public key directory that was shown when you make the SSH key and the rest stays the same.

![installing key to server](https://raw.githubusercontent.com/lvuluong/cse15l-lab-reports/main/PicsForLab1/instalingkey.JPG)

## Step 6: Optimizing Remote Running

And finally, in order to optimzing the running time while trying to change the code, update it to the server and running the program itself on the server, normally it would take some time, however, after making the SSH key, you don't have to enter the password everytime which save time. But to further optimize it, you can type all the command needed to make a copy of the newly updated file, move it to the server and then compile it and run it all on one line to save time. And by clicking the up arrow key, you can reuse that command line everytime without having to type it, making it very efficient.

![optimizing](https://raw.githubusercontent.com/lvuluong/cse15l-lab-reports/main/PicsForLab1/optimize.JPG)