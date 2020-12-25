# Creating and Configuring the Custom Command - `internsctl`
## Section A
⚡ **Create man page**
- *Step 1 :* Go to the standrad location `/usr/share/man` in filesystem, where manual (man) pages of all the commands are stored and run `ls` command to list all the directories in that location.

  <img src = "/images/Setting_Up_Man_Page_step-1.png">
  
  Here in this location, several directories (e.g., man1, man2, man3...) store manual pages of several categories of commands. See below -
  
   ```
   The standard sections of the manual include:

      man1  -  User Commands
      man2  -  System Calls
      man3  -  C Library Functions
      man4  -  Devices and Special Files
      man5  -  File Formats and Conventions
      man6  -  Games et. al
      man7  -  Miscellanea
      man8  -  System Administration tools and Daemons
   ```
   Now since `internsctl` is a `User Command`, the manual page should be created and stored in `man1` directory.
   
- *Step 2 :* 
