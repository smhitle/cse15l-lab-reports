[Back to Home](https://smhitle.github.io/cse15l-lab-reports/)

# Installing VSCode

![VSCode Screenshot](Images/image22.png)

### Here lies a screenshot of VSCode when first opened. This step was pretty much just installing and setting up VSCode (which it may be already for some people). 

# Remotely Connecting

![Remote Connect Screenshot](Images/image21.png)

### 

# Trying Some Commands

![Trying Commands](Images/part4.PNG)

### The point of this step was to explore some useful commands in the terminal. The following are some listed commands that were tried, though some had failed. Some of these were useful in learning about remote access and copying files, and some were interesting to learn about.

cd ~ - changes directory to "~"

cd - changes the directory

ls - prints out the contents of a directory

ls -lat - combines the effects of -l, -a, and -t (long format, ".", and modification date)

ls -a - lists files including those starting with "." (these same files can be seen far left when the -lat command was run)

ls /home/linux/ieng6/cs15lsp22/cs15lsp22abc - should have theoretically listed the contents of another users directory, however, permission was denied

cp /home/linux/ieng6/cs15lsp22/public/hello.txt ~/ - permission denied

cat /home/linux/ieng6/cs15lsp22/public/hello.txt - permission denied

scp - securely copies a file(s) to the remote computer and is always run from the client

cp - does the same as scp, except for the fact that it does not utilize SSH

mkdir - makes a new directory

pwd - prints the working directory

# Moving Files with scp

![Moving Files Screenshot](Images/image9.png)

# Setting an SSH key

![Setting up SSH key](Images/part6.PNG)

# Optimizing Remote Running

There are some very convenient shortcuts that could be made when trying to work remotely. This example will focus on making a local edit on a file (WhereAmI.java) and copying it to the remote server and running it.

The first step is to make the local edit itself. () with the addition of (), which will serve as the local edit.

The second step is to copy it to the server, and conveniently, the SSH key we created in the last part helps a lot since no password is required. There is also the fact that we are allowed to make up several commands in one line, in which the command I will be using is scp WhereAmI.java cs15lsp22awq@ieng6.ucsd.edu:~/; javac WhereAmI.java; java WhereAmI



