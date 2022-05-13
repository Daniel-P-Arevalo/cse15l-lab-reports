# Lab Report - Week 6

## Streamlining ssh Configuration

You can create a new config file in your local .ssh folder with this text in it:
![ssh_config](ssh_config.png)

With this config file created you're able to log into your course account with an alias instead typing cs15lsp22zzz@ieng6.ucsd.edu every time.
![alias_login](alias_login.png)

This new alias can be used in place of cs15lsp22zzz@ieng6.ucsd.edu for anything, such as with the command `scp`.
![alias_scp](alias_scp.png)

## Setup Github Access from ieng6

In GitHub the public key is stored in its own place under settings for ssh keys.
![github_key_storage](github_key_storage.png)

On your user account the public and private key are both located in the account's .ssh folder.
![key_storage](key_storage.png)

By putting the key on GitHub you're able to commit and push your changes to the repository on GitHub through the command line.
![git_commit](git_commit.png)
![git_push](git_push.png)

[This](https://github.com/Daniel-P-Arevalo/good-markdown-parser/commit/b8163dce27e3a8b55614507a54c7d8a9e882d609) is the resulting commit from the above commit and push.

## Copy Whole Directories with `scp -r`

With the command `scp -r` you're able to copy entire directories over to your user account and from there you can run it on your account.
![copy_directory](copy_directory.png)
![copy_directory_run](copy_directory_run.png)

You can also optimize the above commands into only two lines with the use of a semicolon as seen below.
![copy_optimized_1](copy_optimized_1.png)
![copy_optimized_2](copy_optimized_2.png)
![copy_optimized_3](copy_optimized_3.png)
