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


### **Homework**
  * Change Password:
    * <kbd>su -</kbd> **:** &nbsp; Switches to `Root User`
    * <kbd>passwd <user_name></kbd> **:** &nbsp; Changes User password
    * <kbd>Exit</kbd> **:** &nbsp; Switches back to `User`

  &nbsp;
  * Create Files: jerry, kramer, george, lex, clark, lois, homer, bart, lisa,
    marge
    * <kbd>touch <file_name> ... <infinity_names></kbd> **:** &nbsp; Creates files 

  &nbsp;
  * Create 3 Directories seinfeld, superman, simpsons
    * <kbd>mkdir <dir_name> ... <infinity_names></kbd> **:** &nbsp; Creates dir's

  &nbsp;
  * Create file jupiter and write to it "Jupiter is a planet". Then create a soft
    link in /temp directory
    * <kbd>echo "Jupiter is a planet" > jupiter</kbd>
    * <kbd>cd /tmp</kbd>
      * <kbd>ln -s /home/<user_name>/jupiter</kbd>
      * Check: <kbd>ls -ltri</kbd> **:** Displays inode (Linux pointer to file)
      * Check: <kbd>cat jupiter</kbd> **:** Reads file in command line
      * Note: link is broken when sourcefile is removed    

  &nbsp;
  * Create hard link
    * <kbd>echo "Jupiter is a planet" > jupiter</kbd>
    * <kbd>cd /tmp</kbd>
      * <kbd>ln /home/<user_name>/jupiter</kbd>
      * Check: <kbd>ls -ltri</kbd> **:** Displays inode (Linux pointer to file) 
      * Check: <kbd>cat jupiter</kbd> **:** Reads file in command line
      * Note: link remains when sourcefile is removed

