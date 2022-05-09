[Back to Home](https://smhitle.github.io/cse15l-lab-reports/)

# Lab Report 3

## Streamlining ssh Configuration

Initially I had to create a config file under the .ssh directory. Once it was created I opened a new window in VSCode in order to edit it (since it was uneditable unless I had a proper way to open it). 

![OpenConfig](Images/openconfig.PNG)

Having it opened, I changed the name of the alias to ucsd instead. In order to access the ieng6 server, all I had to do was use ssh ucsd (very conveinent)

![LoggingIn](Images/login.PNG)

The next to do was copy a file using this new method. The command that I used to do this was `scp <filename> ucsd:~/<filename>`

![CopiedFile](Images/copiedfile.PNG)

## Setup Github Access from ieng6 