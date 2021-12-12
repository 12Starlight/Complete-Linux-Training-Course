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
  * Run <kbd>ps aux | grep user_name_to_change</kbd>
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