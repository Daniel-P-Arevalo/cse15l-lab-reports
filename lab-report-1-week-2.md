# Lab Report - Week 2

## Downloading VScode

The first step to remote access is to download an IDE (Integrated Development Environment). The one that we will be using is [VScode](https://code.visualstudio.com/), so simply download it from the website and install it to your computer. When you open up VScode you show get an interface that looks like this:

_**Insert Picture**_

## Remotely Connecting

If you're on Windows you will need to install the program [OpenSSH](https://docs.microsoft.com/en-us/windows-server/administration/openssh/openssh_install_firstuse) before you can begin.

On Vscode open up a new terminal either by pressing Ctrl + ` or by selecting Terminal --> New Terminal in the menus.
Now in the terminal input the command:

$ ssh cs15lsp22zz@ieng6.ucsd.edu

The zz should be replaced with the letters in your course specific account and the $ shouldn't be included. After that is done simply input your password for your course specific account. If it's your first time connecting you may get a message asking if you want to continue connecting, just type yes and press enter. Now your terminal should look something like this:

_**Insert Picture**_

**Note:** When entering your password it won't show up while typing but it is being entered.

## Trying Some Commands

Now that you have connected try running some commands in the terminal. Try these commands both while connected and not connected to the remote computer.

Here is a list of commands to try:
* cd ~
* ls -lat
* pwd
* mkdir
* cp /home/linux/ieng6/cs15lsp22/public/hello.txt ~/
* cat /home/linux/ieng6/cs15lsp22/public/hello.txt

Here is an example of some commands run on the terminal:

_**Insert Picture**_

## Moving Files with scp
