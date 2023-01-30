## SafePass
**NOTE: This is not to be used seriously, its just a demo. If you wish to use it seriously then I advise you to edit the code and move the important files (*.aes) to a better location.**
### Requirements
[Cryptopp](https://github.com/weidai11/cryptopp)
### Run
To run this program simply clone the repo, cd into it and run make
 ```
 git clone https://github.com/emoney17/safepass.git
 cd safepass
 make
 ```
### Usage
This password manager is my interpretation of [pass](https://www.passwordstore.org/).
It will generate a directory for you to store all of your passwords and seperate them by subject. Each subject will be a directory and the file is the name of the actual website/program you are using. The password will be stored in the file after going through AES-128 encryption. To view any password you will used the "-v/--view" and enter the subject and entry. This will print out a decrypted password for you to copy.
### Commands
```
$ ./safepass -h
A CLI password manager!
Usage: ./safepass [OPTIONS]

Options:
  -h,--help                   Print this help message and exit
  -i,--init                   First time users generate necessary files
  -v,--view TEXT              View all entries with 'all' or a specific entry with 'Subject/Entry'
  -g,--generate INT           Generate a password when adding an entry and pick the length
  -s,--nosymbols              Generate a password without special characters
  -a,--add TEXT               Add a new entry with the format 'Subject/Entry' and enter a password
  -r,--remove TEXT            Remove a 'Subject/' or a 'Subject/Entry'
```
