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
  * <kbd>ls -ltr seinfeld</kbd>

### **7.)** Create 2 new files in seinfeld directory, eliane and newman
  * <kbd>touch eliane newman</kbd>

### **8.)** Change file permission of newman to add write permissions to only group
  * <kbd>chmod 764 newman</kbd> **:** Assigns rwx to user, rw to group, r to other
  * <kbd>chmod a-w newman</kbd> **:** Removes w for all users
  * <kbd>chmod g+w</kbd> **:** Adds w to group

### **9.)** Become root and cd into your home directory. Then create 2 new files superman and zad in superman directory
  * <kbd>su -</kbd>
  * Enter password for root user
  * <kbd>cd /home/user_name/superman</kbd>
  * <kbd>touch superman zad</kbd>

### **10.)** Change ownership of zad file from root to your username
  * <kbd>chown user_name zad</kbd>

### **11.)** Change group ownership of zad from root to your username
  * <kbd>chgrp user_name zad</kbd>

### **12.)** Move superman file to /temp directory
  * <kbd>mv superman /tmp</kbd>

### **13.)** Remove superman file to /temp directory
  * <kbd>pwd</kbd>
  * <kbd>cd /tmp</kbd>
  * <kbd>rm superman</kbd>

### **14.)** Exit out of root account
  * <kbd>exit</kbd>
  
### **15.)** Go back to superman directory in your home directory and add this line to zad file "zad is a bad character in superman movie"
  * <kbd>cd superman</kbd>
  * <kbd>echo "zad is a bad character in superman movie" > zad</kbd>

### **16.)** Go to seinfeld directory and create a new file seinfeld
  * <kbd>cd ../seinfeld</kbd>
  * <kbd>touch seinfeld</kbd>

### **17.)** Add 5 seinfeld characters names in seinfeld file: Jerry Seinfeld, George Costanza, Eliane Benis, Cosmo Kramer, and David Puddy
  * <kbd>vi seinfeld</kbd> **:** Opens VIM text editor
  * <kdb>i</kdb> **:** Insert command to insert data
  * Type in data
  * <kdb>esc</kdb>
  * <kbd>:wq!</kbd> **:** Writes to file, quits VIM, saves file

### **18.)** Become root user again
  * <kbd>su -</kbd>
  * Enter password for root user

### **19.)** Do cat/var/log/messages and output to a file called mesg-new in your home directory
  * <kbd>cat /var/log/messages > /home/user_name/mesg-new</kbd>

### **20.)** Read the mesg-new file with cat, more, less commands and practice
  * <kbd>cd /home/user_name/</kbd>
  * <kbd>cat mesg-new</kbd>
  * <kbd>more mesg-new</kbd> **:** Displays one page at a time, hit space to turn page, q to exit
  * <kbd>less mesg-new</kbd> **:** Displays one page at a time, hit space to turn page, j and up arrow scroll up, k and down arrow scrol down one line at a time, q to exit

### **21.)** View the first 10 lines of mesg-new file and output to a file name mesg-h10
  * <kbd>head mesg-new > mesg-h10</kbd>

### **22.)** View the last 20 lines of mesg-new file and output to a file name mesg-t20
  * <kbd>tail -n20 mesg-new > mesg-t20</kbd>

### **23.)** Exit out of root user
  * <kbd>exit</kbd>

### **24.)** Go to seinfeld directory in your home directory and create a new file "seinfeld-characters"
  * <kbd>cd seinfeld</kbd>
  * <kbd>touch seinfeld-characters</kbd>

### **25.)** Add text to seinfeld-character file using echo command. Each character should be in one line, "Jerry Seinfeld, Cosmo Kramer, Eliane Benes, George Costanza, Newman Mailman, Frank Costanza, Estelle Costanza, Morty Seinfeld, Helen Seinfeld, Babes Kramer, Alton Benes, J Peterman, George Steinbrenner, Uncle Leo, David Puddy, Justin Pit, and Kenny Bania"
  * <kbd>echo "Jerry Seinfeld" > seinfeld-character</kbd>
  * <kbd>echo "Cosmo Kramer" >> seinfeld-character</kbd>
  * <kbd>echo "Eliane Benes" >> seinfeld-character</kbd>
  * <kbd>echo "George Costanza" >> seinfeld-character</kbd>
  * <kbd>echo "Newman Mailman" >> seinfeld-character</kbd>
  * <kbd>echo "Frank Costanza" >> seinfeld-character</kbd>
  * <kbd>echo "Estelle Costanza" >> seinfeld-character</kbd>
  * <kbd>echo "Morty Seinfeld" >> seinfeld-character</kbd>
  * <kbd>echo "Helen Seinfeld" >> seinfeld-character</kbd>
  * <kbd>echo "Babes Kramer" >> seinfeld-character</kbd>
  * <kbd>echo "Alton Benes" >> seinfeld-character</kbd>
  * <kbd>echo "J Peterman" >> seinfeld-character</kbd>
  * <kbd>echo "George Steinbrenner" >> seinfeld-character</kbd>
  * <kbd>echo "Uncle Leo" >> seinfeld-character</kbd>
  * <kbd>echo "David Puddy" >> seinfeld-character</kbd>
  * <kbd>echo "Justin Pit" >> seinfeld-character</kbd>
  * <kbd>echo "Kenny Bania" >> seinfeld-character</kbd>
  * Note: this could also be accomplished by <kbd>echo -e "name\nname\n...etc" >> seinfeld-character</kbd>

### **26.)** Use cut command to cut the first 4 letters of each line from seinfeld-characters file and output to a different file name (name=filters-files)
  * <kbd>cut -c1-4 seinfeld-characters > seinfeld-cut</kbd> **:** Cuts characters in a range of 1-4

### **27.)** Use awk command to get only the 2nd column of seinfeld-characters and output to the filters-files without removing any other text from it
  * <kbd>awk '{print $2}' seinfeld-characters > filters-files</kbd>

### **28.)** Use grep command to only grep seinfeld and output to a new file called seinfeld-family
  * <kbd>grep -i seinfeld seinfeld-characters > seinfeld-family</kbd> **:** Ignores case

### **29.)** Use sort command, uniq and wc command to practice whichever way you like by creating new files or workign with existing files
  * <kbd>sort -u seinfeld-characters</kbd> **:** Sorts only unique lines
  * <kbd>sort seinfeld-characters | uniq -D</kbd> **:** Prints only duplicate lines
  * <kbd>cat seinfeld-characters | wc -lL</kbd> **:** Prints number of lines, Longest line