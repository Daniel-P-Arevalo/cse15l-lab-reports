# Lab Report - Week 2

## Downloading VScode

The first step to remote access is to download an IDE (Integrated Development Environment). The one that we will be using is [VScode](https://code.visualstudio.com/), so simply download it from the website and install it to your computer. When you open up VScode you show get an interface that looks like this:

_**Insert Picture**_

## Remotely Connecting

If you're on Windows you will need to install the program [OpenSSH](https://docs.microsoft.com/en-us/windows-server/administration/openssh/openssh_install_firstuse) before you can begin.

On Vscode open up a new terminal either by pressing Ctrl + ` or by selecting Terminal --> New Terminal in the menus.
Now in the terminal input the command:

>$ ssh cs15lsp22zz@ieng6.ucsd.edu

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

With remote connecting we are able to copy files to and from the remote computer. To do this we use the command scp on the client, so first log out of the remote server by pressing Ctrl + D or running the command exit. After that input this command:

>scp <File Name> cs15lsp22zz@ieng6.ucsd.edu:~/

Now if you log back in you and type the command ls you should be able to see the file there.
  
_**Insert Picture**_
  
## Setting an SSH Key
  
One problem with remote connecting and scp is that everytime we do either of these we need to reinput our password, which can get annoying and combersome very quickly. In order to solve this problem we can create and use ssh keys.
  
On your client input the command:
  
>$ ssh-keygen
  
You will then be prompted to enter the file where you want the key to be saved and to enter a passphrase. If you're using Windows you will need to follow some [extra steps](https://docs.microsoft.com/en-us/windows-server/administration/openssh/openssh_keymanagement#user-key-generation).
  
_**Insert Picture**_  
  
Now that the keys have been created we need to copy the public key to the server. Start by logging into the remote server and inputing the command:
  
>$ mkdir .ssh
  
Now log out of the remote server and on your client input the command:
  
>$ scp <Key Path Name> cs15lsp22zz@ieng6.ucsd.edu:~/.ssh/authorized_keys
  
After doing this you should be able to log into the remote server without having to type in your password.
  
## Optimizing Remote Running
  
There are many ways in which you can make doing tasks quicker and easier to perform. At the end of an ssh command you can add a command in quotes to run the command on the remote server and exit afterwards. Using semicolons will let you perform multiple commands on the same line. You can use the up-arrow to automatically input the last command that was run. Here is an example of these techniques in practice:
  
_**Insert Picture**_
