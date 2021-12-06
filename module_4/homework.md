# **Module 4 Homework**

### **1.)** Practice Linux command syntax with command, options and arguments
  * <kbd>whoami</kbd> **:** Gets username
  * <kbd>hostname</kbd> **:** Gets hostname
  * <kbd>pwd</kbd> **:** Prints working directory
  * <kbd>clear</kbd> **:** Clears screan
  * <kbd>ls -ltr</kbd> **:** List Line, Ordered by time, In reverse (newest first)
  * <kbd>cat seinfeld-characters</kbd> **:** Reads file
    * <kbd>grep -in cos seinfeld-characters</kbd> **:** Selects charaters in file, ignores case, Lists line number selections are found

### **2.)** List files in your home directory by the last time they were modified
  * <kbd>ls -ltr</kbd> **:** Lists by line, Last modified time, In reverse (newest first)

### **3.)** Move jerry, george, kramer, and puddy files into seinfeld directory
  * <kbd>mv jerry george kramer puddy seinfeld</kbd>
  
### **4.)** Move homer, bart, marge, lisa files in simpsons directory
  * <kbd>mv homer bart marge lisa simpsons</kbd>

### **5.)** Move clark, luther and lois files in superman directory
  * <kbd>mv clark lois luther superman</kbd>

### **6.)** List the content of seinfeld directory by the last time they were modified
### **7.)** Create 2 new files in seinfeld directory, eliane and newman
### **8.)** Change file permission of newman to add write permissions to only group
### **9.)** Become root and cd into your home directory. Then create 2 new files superman and zad in superman directory
### **10.)** Change ownership of zad file from root to your username
### **11.)** Change group ownership of zad from root to your username
### **12.)** Move superman file to /temp directory
### **13.)** Remove superman file to /temp directory
### **14.)** Exit out of root account
### **15.)** Go back to superman directory in your home directory and add this linke to zad file "zad is a bad character in superman movie"
### **16.)** Go to seinfeld directory and create a new file seinfeld
### **17.)** Add 5 seinfeld characters names in seinfeld file: Jerry Seinfeld, George Costanza, Eliane Benis, Cosmo Kramer, and David Puddy
### **18.)** Become root user again
### **19.)** Do cat/var/log/messages and output to a file called mesg-new in your home directory
### **20.)** Read the mesg-new file with cat, more, less commands and practice
### **21.)** View the first 10 lines of mesg-new file and output to a file name mesg-h10
### **22.)** View the last 20 lines of mesg-new file and output to a file name mesg-t20
### **23.)** Exit out of root user
### **24.)** Go to seinfeld directory in your home directory and create a new file "seinfeld-characters"
### **25.)** Add text to seinfeld-character file using echo command. Each character should be in one line, "Jerry Seinfeld, Cosmo Kramer, Eliane Benes, George Costanza, Newman Mailman, Frank Costanza, Estelle Costanza, Morty Seinfeld, Helen Seinfeld, Babes Kramer, Alton Benes, J Peterman, George Steinbrenner, Uncle Leo, David Puddy, Justin Pit, and Kenny Bania"
### **26.)** Use cut command to cut the first 4 letters of each line from seinfeld-characters file and output to a different file name (name=filters-files)
### **27.)** Use awk command to get only the 2nd column of seinfeld-characters and output to the filters-files without removing any other text from it
### **28.)** Use grep command to only grep seinfeld and output to a new file called seinfeld-family
### **29.)** Use sort command, uniq and wc command to practice whichever way you like by creating new files or workign with existing files