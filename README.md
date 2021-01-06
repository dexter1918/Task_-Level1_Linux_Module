## Creating and Configuring the Custom Command : `internsctl`
### Section A
⚡ **1. Creating manual (man) page**
- *Step 1 :* 
  * Login as a root user by running the command `sudo -i` (If it asks for the administrative password, Enter it).
  * Now using `cd` command move into to the standrad location in filesystem : `/usr/share/man`, where manual pages of all the commands are normally stored in **nroff(1)** format.
  * Then run `ls` command to list all the directories in that location.\
  \
    <img src = "/images/img_1.png">
  
    Here in this location, each man page is categorized in a specific section (directory), different directories (e.g., man1, man2, man3...) store man pages for different category of commands. See below -
   
     ```
        man1  -  User Commands
        man2  -  System Calls
        man3  -  C Library Functions
        man4  -  Devices and Special Files
        man5  -  File Formats and Conventions
        man6  -  Games et. al
        man7  -  Miscellaneous
        man8  -  System Administration tools and Daemons
     ```
     Now since **internsctl** is a **user command**, we will create and store the manual page file in `/man1` directory.
   
- *Step 2 :*
  * From the current directory, navigate to `/man1` directory using `cd man1` command.
  * Create the source file of the man page using the command `touch` followed by `<File_Name>.<Section_Index>`.

    > File_Name : The command whose manual page to be created.\
    > Section_Index : For man1 - it'll be **1**, For man2 - it'll be **2**, and so on.
    >
    > In this case it will be : **touch internsctl.1**
    
    <img src = "/images/img_2.png">
- *Step 3 :*    
  * Now run `nano internsctl.1` to edit the source file in nano text editor. Copy and paste the following script into the source file or write it from yourself and save it.
    ```
    .\" Manual (man) page of internsctl
    .TH internsctl 1 "28 December 2020" "0.1.0" "Custom Command"
    .SH NAME
    internsctl
    .SH SYNOPSIS
    internsctl cpu getinfo |
    .brinternsctl memory getinfo |
    .brinternsctl user create <username> |
    internsctl user list |
    internsctl user list --sudo-only |
    internsctl file getinfo <file-name> |
    internsctl file getinfo [options] <file-name> 
    .SH DESCRIPTION
    Display cpu and memory information, create new user, list all users, list all users with sudo permissions, get file information, get specific  information of file.  
    .SH OPTIONS
    .TP
    .BR \-\-size ", " \-s			print " " file " " size
    .TP
    .BR \-\-permissions ", " \-p		print " " file " " permissions
    .TP
    .BR \-\-owner ", " \-o			print " " file " " owner
    .TP
    .BR \-\-last-modified ", " \-m		print " " last " " modified " " date " " and " " time " " of " " the " " file
    .SH BUGS
    No known bugs. (However reach at sksalmanhaider@outlook.com in case of any errors and typos.)
    .SH AUTHOR
    Sk Salman Haider
    ```
    ➡️ Refer to this link for man page syntax : https://unix.stackexchange.com/questions/90759/where-should-i-install-manual-pages-in-user-directory
    
- *Step 4 :*
  * Now it's done.
  * Run `man internsctl` from terminal to check the manual page of the `internsctl`. See below -
  \\
    <img src = "/images/img_3.png">
    
    
