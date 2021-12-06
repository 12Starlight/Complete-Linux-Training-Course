# SSH

### **Create SSH Connection**
  * Open Virtual Machine
  * Run &nbsp; <kbd>ip addr</kbd>
    * Look for `2: enp0s3`, then the ip address
    * Open a terminal in your Mac
      * Run &nbsp; <kbd>ssh -l <user_name> <vm_ip_address_above></kbd>
      * Run &nbsp; <kbd>whoami</kbd> to check new username
      * Run &nbsp; <kbd>hostname</kbd> to check new hostname

### **Locate**
  * As the root user run &nbsp; <kbd>updatedb</kbd>
  * Make sure mlocate package is installed
    * As the root user run &nbsp; <kbd>um install mlocate</kbd>


