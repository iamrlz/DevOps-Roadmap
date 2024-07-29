# Basic Commands in Linux

- Present Working Directory: `pwd`
  
- List Content: `ls`
   - To Show Hidden files: `ls -a`
   - To Show files in-order of creation: `ls -lt`
   - To Show files in the reverse order of creation: `ls -ltr`

- Make Directory
  - Make a New Directory: `mkdir <file or directory name>`
  - Make a Multiple Directory: `mkdir <file1> <file2> <file3>`
  - Make a Directory without going inside the directory: `mkdir <filename>/<newfile>`
  - Create a child directory with simultaneously creating a parent directory: `mkdir -p <newfile1>/<newfile2>`
  - Create a file under each directory by the name `capital.tx` without going inside the directory: `touch /home/username/countries/{USA,UK}/capital.txt`
  - Add the capital cities name in the file Using `echo` command: `echo "Washington, D.C" > /home/username/countries/USA/capital.txt && echo "London" > /home/username/countries/UK/capital.txt`

 
- Change Directory
   - Changes the current directory to the user's home directory: `cd`
   - Changes the current directory to the parent directory of the current working directory: `cd ..`
   - Absolute Path: Full path from root, starts with `/`, like: `cd /home/username`
   - Relative Path: Path relative to current directory, doesn't start with `/`, like: `cd ../myfile`

- `pushd`: Adds a directory to the directory stack and changes the current directory.
- `popd`: Removes directories from the stack and changes the current directory to the previous directory in the stack.


## More Basic Commands 

- Move File or Directory: `mv /home/user/europe/pakistan   /home/user/asia` or `mv europe/pakistan asia/`

- Rename File or Directory: `mv Asia/Pkistn  /Asia/Pakistan`

- Copy File: `cp asia/pakistan/country.txt   asia/india`

- Remove Directory: `rmdir <filenanme>`

- Remove File: `rm asia/pakistan/country.txt`
  
- Copies directories and their contents recursively: `cp -r source_directory target_directory` like: `cp -r /home/user/working /home/user/backup`


## More More Basic Commands

- Working with Files & Directory: `Cat` Command
   - Display File Content: `cat <filename>`
   - Concatenate Multiple Files: `cat file1 file2 > combined_file`
   - Append to a File: `cat file1 >> file2`
   - Create a new file and add text: `cat > newfile.txt`
 
- Create a file using `touch` Command
    - Create a new empty file: `touch <filename>`
    - Create a new empty file without navigating into the directory: `touch /home/user/asia/test.txt>`

- To display a line of text or a string that is passed as an argument: `echo` Command
     - `echo [options] [argument]` like: `echo "Hello World"`
     - #### Common Options
       - `-n`: Do not output the trailing newline.
       - `-e`: Enable interpretation of backslash escapes.
       - `-E`: Disable interpretation of backslash escapes (default).

- Text Editor: `vi` & `nano` cammand
     * Open a file in Vim: `vi <file_name>`
        * Modes:
            * `i`: Insert mode
            * `Esc:` Normal mode
        * Navigation:
            * `h`, `j`, `k`, `l`: Move left, down, up, and right
            * `gg`: Go to the beginning of the file
            * `G`: Go to the end of the file
            * `w`: Move to the beginning of the next word
            * `b`: Move to the beginning of the previous word
        * Editing Text:
            * `i`: Insert before the cursor
            * `a`: Insert after the cursor
            * `o`: Open a new line below the cursor and enter Insert Mode
            * `dd`: Delete the current line
            * `yy`: Yank (copy) the current line
            * `p`: Paste the yanked or deleted content after the cursor
        * Save and Quit:
            * `:w`: Save
            * `:q`: Quit
            * `:wq`: Save and quit
            * `:q!`: Quit without saving


     * Open a file in nano: `nano <filename>`
        * Navigation:
            * `Ctrl + A`: Start of line
            * `Ctrl + E`: End of line
        * Editing:
            * `Ctrl + K`: Cut line
            * `Ctrl + U`: Paste
        * Save and Quit:
            * `Ctrl + O`: Save (Enter to confirm)
            * `Ctrl + X`: Exit
 
- Displaying File Content One Page at a Time: Pages
   - `more` command displays the content of a file one screen at a time: `more <file.txt>`
   - `less` command is more powerful than more and allows for backward movement in the file as well as forward movement: `less <file.text>`
     
   -  #### Navigation in `more`:
         - [Spacebar]: Move to the next screen.
         - [Enter]: Move one line down.
         - [b]: Move one screen back (if supported by the terminal).
    
         
   -  #### Navigation in `less`:
         - [Up Arrow (↑)]: Move one line up.
         - [Down Arrow (↓)]: Move one line down.
         - [/]: Search test.

# Bit Advanced commands

- Viewing a file or directory sizes (disk usage):
    -  Summarize total size and show size in kilobytes: `du -sk test.img`
    -  Summarize total size, show size in Megabytes and human-readable format: `du -sh test.img`
    -  Long format and human-readable format: `ls -lh test.img`
 
- Archiving Files:
   - Archiving more than one file: `tar -cf test.tar file1 file2`
   - Show long list content: `tar -tf test.tar`
   - Extract content: `tar -xf test.tar`
   - Compress the file: `tar -zcf test.tar file1 file2`
 
- Compressing Filess:
    - `bzip2`: High compression ratio, moderate speed.
    - `gzip`: Fast compression/decompression, lower compression ratio.
    - `xz`: Highest compression ratio,

 - Un-compressing:
     - `bunzip2 <filename>`
     - `gunzip <filename>`
     - `unxz <filename> `
   
 - How to read a compressed file without un-compressing:
      - `bzcat <filename>`
      - `zact <filename>`
      - `xzcat <filename>`
  
        
- Searching/Finding for a File or Directory names - `locate`:
     - For finding file names: `locate <filename>`
     - For Case-insensitive search: `locate -i <filename>`
     - For Limit number of results: `locate -n 10 <filename>`
     - For Update the database(if locate command doesn't work): `sudo updatedb`


- Searching/Finding text patterns within files - `grep`:
     * For finding patterns within files: `grep "pattern" <filename>`
     * For Search in multiple files: `grep "pattern" <file1> <file2>`
     * Case-insensitive search: `grep -i "pattern" <filename>`
     * Print a line using pattern: `grep "pattern" <file1.text>`
     * Display line numbers: `grep -n "pattern" <filename>`
     * Search for whole words: `grep -w "word" <filename>`
     * Invert match (show lines that do not match): `grep -v "pattern" <filename>`
     * Count matching lines: `grep -c "pattern" <filename>`
     * Using grep with other commands: `command | grep "pattern"`
     * Recursive search through directories(When you don't know the file content): `grep -r "pattern" directory/`
     * Invert match (show lines that do not match the pattern): `grep -v "pattern" <filename>`
     * Treat binary files as text (useful if you need to search binary files): `grep -a "pattern" <filename>`
     * Show byte offset of matching lines: `grep -b "pattern" <filename>`
     * Combining options: `grep -r -w -v "pattern" directory/`
     * To check vendor for the ethernet controller used in sys: `ispc: | grep Ethernet` OR `cd /sys/class/net/eth0/devices`


- Documentation and Get help Commands:
   - Command to describe how a command name is interpreted, identify whether a command is internal or external: `type grep`
   - Command for displaying a brief description of other commands" `whatis echo`
   - Manual command to view detailed documentation (man pages) for other commands: `man echo`
   - Command-line option to display a brief help message with usage information for a command: `echo --help`
   - Command for searching the manual page names and descriptions for a keyword: `apropos modpr`

- Piping:
     - `command1 | command2` , e.g. `ls -l | grep ".txt"`
- Kernel Version:
     - `uname`
 - Kernel Version Number:
     - `uname -r`
             

# Service Management Commands

   - `systemctl` Commands - interact with the systemd system and service manager:
        * Start a service: `sudo systemctl start service_name`
        * Stop a service: `sudo systemctl stop service_name`
        * Restart a service: `sudo systemctl restart service_name`
        * Reload a service (for services that support reloading without stopping): `sudo systemctl reload service_name`
        * To check init process in sys: `systemctl --version`
        * To check run level: `runlevel`
        * To check default systemd target set: `systemctl get-default`
        * To change it to multi-user.target: `sudo systemctl set-default multi-user.target`
        * File type is `firefox.deb` in `/root`: `sudo file /root/firefox.deb`
        * 

- Input Redirection - allows users to control the input and output of commands:
     * Input Redirection:
          * Redirect input from a file: `command < input_file`

     * Output Redirection:
          * Redirect output to a file (overwrite): `command > output_file`, e.g. `echo $SHELL > shell.txt`
          * Redirect output to a file (append): `command >> output_file`, e.g. `echo "This is a bash file" >> shell/txt`
      
     * Error Redirection:
          * Redirect error output to a file (overwrite): `command 2> error_file`, e.g. `cat missing_file 2 > error.txt`
          * Redirect error output to a file (append): `command 2>> error_file`, e.g. `cat missing_file 2 >> error.txt`
      
     * To avoid print error on screen: ` cat missing_file 2 > /dev/null` ∴ /dev/null = dum bucket
      

# Common Networking Commands


  - IP:
     * To Find IP: `IP address`
    
  - Ping:
     * Used to test the reachability of a host on an IP network: `ping <hostname_or_ip_address>`
  - Ping6:
     * Used to test the reachability of a host using IPv6: `ping6 <hostname_or_ip_address>`
   
  - Hostname:
     * Displays or sets the system's hostname: `hostname`  OR Set a New Hostname: `sudo hostname newhostname`
    
   - nslookup:
     * Queries the DNS to obtain domain name or IP address mapping.: `nslookup <hostname_or_ip_address>`
    
  - dig:
     * More advanced DNS querying tool: `dig <hostname>`
   
  - route:
     * Displays or modifies the IP routing table: `route`
       * To add a route: `sudo route add -net <network> netmask <netmask> gw <gateway>`

  - ip link:
     * Displays or modifies network interfaces: `ip link show`
         * To bring an interface up: `sudo ip link set <interface> up`
         * To bring an interface down: `sudo ip link set <interface> down`

### DNS 
       
* To Find DNS Name 
    - `cat /etc/resolv.conf`

* File that is responsible for host file-based DNS
    - ` /etc/host`
       
* Change the order to DNS & Hosts
    - `sudo vim /etc/nsswitch.conf` , then `Hosts = dnsfiles`
       
* To change DNS nameserver
    - `sudo vim /etc/resolv.conf`

## Troubleshooting a Network
   - [x] Testcase init
     
 1. Check Interface: `ip link`
 2. Check DNS Resolution: `nslookup <ip_address>`
 3. Check Connectivity: `ping <ip_address>`
 4. Check Route: `traceroute <ip_address>`
 5. Check Server: `netstat -an | grep 80 | grep -i LISTEN`
 6. Check again Interface: `ip link`


## Linux Accounts

   #### User Management:

   - Create a User: `sudo useradd username`
   - Set Password for User: `sudo passwd username`
   - Display Current User: `whoami`
   - Delete a User: `sudo userdel username`
   - Delete a User and Their Home Directory: `sudo userdel -r username`
   - To view `user` stored information: `cat /etc/passwd`

   note:     
   * To Check information about the user: `id <username>`
   * To view the last user who is currently logged- in: `who`
   * To view all logged-in users: `last`
    
   #### Group Management:

   - Create a Group: `sudo groupadd groupname`
   - Add a User to a Group: `sudo usermod -aG groupname username`
   - List Groups for a User: `groups username`
   - To view `group` stored information: `cat /etc/group`
   
   #### Superuser (Root) Privileges Management:

   - Runs a command as the root user: `sudo <command>`
   - Switch to Root User: `sudo su` OR `su -`
     
   
   #### System Accounts Management:

   - List System Accounts: `awk -F: '($3 < 1000) {print $1}' /etc/passwd`

   
   #### Service Accounts Management:

   - View Service Accounts: `awk -F: '($3 < 1000) {print $1}' /etc/passwd`
   - To view the `sudo` account stored information: `cat /etc/sudoers`
   - To edit sudoers File: `visudo`


## Access Control Commands

   - View User Information: `cat /etc/passwd`
        - Displays user information for users starting with `username`: `cat /etc/passwd | grep '^username' `
   - View Encrypted Password Information: `sudo grep '^username' /etc/shadow`
   - View Group Information: `grep '^username' /etc/group`


## Linux File Permissions

   ### Modifying File Permission:



