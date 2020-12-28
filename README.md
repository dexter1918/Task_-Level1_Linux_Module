## Creating and Configuring the Custom Command : `internsctl`
### Section A
⚡ **Creating manual (man) page**
- *Step 1 :* 
  * Login as a root user by running the command `sudo -i` (If it asks for the administrative password, Enter it)
  * Now using `cd` command move into to the standrad location in filesystem : `/usr/share/man`, where manual pages are normally stored in nroff(1) format.
  * Then run `ls` command to list all the directories in that location.
   <img src = "/images/img_1.png">
  
  Here in this location, several directories (e.g., man1, man2, man3...) store manual pages for different categories of commands as executable file. See below -
  
   ```
   The standard sections of the manual include:

      man1  -  User Commands
      man2  -  System Calls
      man3  -  C Library Functions
      man4  -  Devices and Special Files
      man5  -  File Formats and Conventions
      man6  -  Games et. al
      man7  -  Miscellaneous
      man8  -  System Administration tools and Daemons
   ```
   Now since `internsctl` is a `User Command`, the manual page should be created and stored in `man1` directory.
   
- *Step 2 :* 
