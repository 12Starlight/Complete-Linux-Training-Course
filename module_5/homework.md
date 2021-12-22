# **Module 5 Homework**

### **Note:** 

<p>

Finally after using many online resources including [StackExchange](https://superuser.com/questions/1313692/how-to-setup-a-bridge-connection-for-enp0s3-centos7-on-oracle-virtualbox) and rewriting the <kbd>ifcfg-enp0s3</kbd> and <kbd>ifcfg-enp0s8</kbd> files for Bridged Network I resolved the problem. Using [Technology/Notes](https://sites.google.com/site/technologyslashnotes/home/linux/configure-networks-centos7-on-virtualbox),  I was able to find out that Virtualbox `DOES NOT` support WIFI connections using Bridge Adapter. 

This link explains it all. [Virtualbox Complaint Ticket](https://www.virtualbox.org/ticket/10019). I did learn a lot about /etc/sysconfig/network-scripts.

</p> 

<p>

After deducing that Virtualbox was not going to offer a solution, I went ahead and downloaded a free user key for VMWare Fusion and was able to ssh into my mac terminal! Success 🔥😎

</p>


&nbsp;

### **Changing Username**
  * Login as root
  * Run <kbd>groupadd new_username</kbd>
  * Run <kbd>ps aux | grep old_username</kbd>
  * Find all `PIDs` for that user
  * Run <kbd>kill -KILL PID</kbd>
    * Do that for all processes being ran
  * Run <kbd>usermod -d /home/new_username -m -g new_username -l new_username old_username</kbd>
  * Close terminal and restart VM

&nbsp;

### **Changing Hostname**
  * Login as root
  * Run <kbd>hostnamectl set-hostname new_hostname</kbd>
  * Run <kbd>hostname</kbd>

&nbsp;

# **Questions**

### **1.)** Go to home directory and then go to superman directory.
  * <kbd>cd /home/</kbd>
  * <kbd>su - root</kbd>
    * Type in password for root user
  * <kbd>useradd superman</kbd> **:** Creates superman user
    * <kbd>cd /home/superman</kbd>

### **2.)** Create a new file called "first4movies" using vi command.
  * <kbd>vim first4movies</kbd> **:** Insert placeholder text, used VIM

### **3.)** Write anything you know about all first 4 movies of superman. If you never watched superman then you can enter at least 20 names of your family members. This file should have 20 lines and each line should have 5-6 words. 
  * <kbd>vim first4movies</kbd>
    * <kbd>dd</kbd> **:** Deletes placeholder text
    * <kbd>i</kbd> **:** Insert text
    * <kbd>esc</kbd> **:** Escapes out of insert
    * <kbd>:wq!</kbd> **:** Writes to the file, quits, then saves

### **4.)** Practice vi command by navigating the file content and remove some lines, edit or undo.
  * <kbd>r + character_replaced</kbd> **:** Replaces a character
  * <kbd>dd</kbd> **:** Deletes a line
  * <kbd>/search_term/</kbd> **:** Searches for all characters or strings within the forward slashes
  * <kbd>i</kbd> **:** Inserts text
  * <kbd>a</kbd> **:** Moves forward a space
  * <kbd>h, j, k, l</kbd> **:** Left, Down, Up, Right

### **5.)** Create a new group superheros (if you do not aleady have one).
  * <kbd>su -</kbd> **:** Login to root first
  * <kbd>groupadd superheros</kbd> **:* Create superheros group

### **6.)** Create a new user hulk and make sure its group should be superheros and its userid should be 2000.  
  * <kbd>su -</kbd> **:** Login to root first
  * <kbd>useradd hulk</kbd> **:** Creates new user hulk
  * <kbd>usermod -aG superheros hulk</kbd> **:** Appends hulk to superheros group
  * <kbd>grep hulk /etc/group</kbd> **:** Checks to see, if hulk was added to the superheros group
  * <kbd>chgrp -R superheros hulk</kbd> **:** Changes hulk's main group to superheros, Casades the change through the directories
  * <kbd>cat /etc/shadow</kbd> **:** Gives a high level snapshot of how the password is set up
  * <kbd>usermod --help</kbd> **:** Look up different options to use to change id
  * <kbd>usermod -u 2000 hulk</kbd>

### **7.)** Once the user hulk is created, change the password for hulk and then login as hulk.
  * <kbd>passwd hulk</kbd>
    * Type in new password
  * <kbd>su - hulk</kbd> **:** Type in password

### **8.)** Under hulk home directory create a file Skaar.
  * <kbd>touch Skaar</kbd>

### **9.)** Change group ownership of Skaar from superheros to root.
  * <kbd>su -</kbd> **:** Changes to root user
  * <kbd>usermod -aG wheel hulk</kbd> **:** Gives hulk access to sudo privledges
  * <kbd>grep wheel /etc/group</kbd> **:** Checks to make sure hulk is added to the group wheel
    * Exit terminal and restart session
  * <kbd>sudo chgrp -R root Skaar</kbd> **:** Changes group of Skaar to root, Cascades the change through the directories

### **10.)** Then create a new group continents.
  * <kbd>sudo groupadd continents</kbd> **:** Adds continents group
  * <kbd>cat /etc/group</kbd> **:** Checks to make sure group was added

### **11.)** Create new users namerica, samerica, asia, europe, australia, africa, and antartica.
  * <kbd>su -</kbd>
  * <kbd>useradd -g continents -s /bin/bash -c "North America" -m -d /home/namerica namerica</kbd> **:** Creates user, Puts user in continents group, Specifies the shell, Depicts description, Puts the user in the home directory, names user namerica 
  * <kbd>useradd -g continents -s /bin/bash -c "South America" -m -d /home/samerica samerica</kbd> **:** Creates user, Puts user in continents group, Specifies the shell, Depicts description, Puts the user in the home directory, names user samerica
  * <kbd>useradd -g continents -s /bin/bash -c "Asia" -m -d /home/asia asia</kbd> **:** Creates user, Puts user in continents group, Specifies the shell, Depicts description, Puts the user in the home directory, names user asia
  * <kbd>useradd -g continents -s /bin/bash -c "Europe" -m -d /home/europe europe</kbd> **:** Creates user, Puts user in continents group, Specifies the shell, Depicts description, Puts the user in the home directory, names user europe
  * <kbd>useradd -g continents -s /bin/bash -c "Australia" -m -d /home/australia australia</kbd> **:** Creates user, Puts user in continents group, Specifies the shell, Depicts description, Puts the user in the home directory, names user australia
  * <kbd>useradd -g continents -s /bin/bash -c "Africa" -m -d /home/africa africa</kbd> **:** Creates user, Puts user in continents group, Specifies the shell, Depicts description, Puts the user in the home directory, names user africa
  
### **12.)** Make sure all these users belong to the group continents
  * <kbd>usermod -aG continents user_name</kbd> **:** Solved in previous question in a chained command
 
### **13.)** Change password for every user, then switch into each user one by one using su - username command and create one file in each user account (e.g. england file in europe, usa in namerica, jpan in asia and so on).
  * <kbd>sudo passwd namerica</kbd> **:** Create password
  * <kbd>su - namerica</kbd> 
  * <kbd>touch usa</kbd>

### **14.)** Also add user namerica to wheel group to allow it to run root commands as root and then test it.

### **15.)** Run last command and find out the number of users logged in. (Do not count duplicate users)

### **16.)** Run id command on africa and austrailia users to verify their user id.

### **17.)** Change the date of your system to Aug 22 1998 at 1pm and verify.

### **18.)** Check system uptime.

### **19.)** List 1999 calender.

### **20.)** List everything with uname command and find out where the system architecture information is located.

### **21.)** Become yourself "Your username" and run df -h command. Output the df -h command to another file and name it systemdiskinfo.

### **22.)** vi Systemdiskinfo file and remove the first and second line and save the file.

### **23.)** Run dmesg command and output to dm-file.

### **24.)** vi dm-file and remove the last 5-7 lines.

### **25.)** Add text in the end of the file dm-file using vi. Text = This is the end of the file. Then save the file.

### **26.)** Reboot the system using init command.


