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

### **2.)** Create a new file called "first4movies" using vi command.

### **3.)** Write anything you know about all first 4 movies of superman. If you never watched superman then you can enter at least 20 names of your family members. This file should have 20 lines and each line should have 5-6 words. 

### **4.)** Practice vi command by navigating the file content and remove some lines, edit or undo.

### **5.)** Create a new group superheros (if you do not aleady have one).

### **6.)** Create a new user hulk and make sure its group should be superheros and its userid should be 2000.

### **7.)** Once the user hulk is created, change the password for hulk and then login as hulk.

### **8.)** Under hulk home directory create a file Skaar.

### **9.)** Change group ownership of Skaar from superheros to root.

### **10.)** Then create a new group continents.

### **11.)** Create new users namerica, samerica, asia, europe, australia, africa, and antartica.

### **12.)** Make sure all these users belong to the group continents

### **13.)**
### **13.)**
### **13.)**
### **13.)**
### **13.)**
### **13.)**
### **13.)**
### **13.)**
### **13.)**
### **13.)**
### **13.)**


