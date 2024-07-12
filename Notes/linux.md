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

- Documentation and Get help Commands\
   - Command is used to describe how a command name is interpreted. It can identify whether a command is internal or external: `type grep`
   - Command for displaying a brief description of other commands" `whatis echo`
   - Manual command to view detailed documentation (man pages) for other commands: `man echo`
   - Command-line option to display a brief help message with usage information for a command: `echo --help`
   - Command for searching the manual page names and descriptions for a keyword: `apropos modpr`
