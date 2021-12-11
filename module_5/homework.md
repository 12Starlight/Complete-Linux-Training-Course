# **Module 5 Homework**

### **Note:** 

<p>

So finally after using many online resources includeing [StackExchange](https://superuser.com/questions/1313692/how-to-setup-a-bridge-connection-for-enp0s3-centos7-on-oracle-virtualbox) and rewriting the ifcfg-enp0s3 and ifcfg-enp0s8 files for Bridged Network I resolved the problem. Using [Technology/Notes](https://sites.google.com/site/technologyslashnotes/home/linux/configure-networks-centos7-on-virtualbox),  I was able to find out that Virtualbox `DOES NOT` support WIFI connections using Bridge Adapter. 

This link explains it all. [Virtualbox Complaint Ticket](https://www.virtualbox.org/ticket/10019). I did learn a lot about /etc/sysconfig/network-scripts.

</p> 

