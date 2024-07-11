# Basic Commands in Linux

- Present Working Directory: `pwd`
  
- List Content: `ls`

- Make Directory
  - Make a New Directory: `mkdir <file or directory name>`
  - Make a Multiple Directory: `mkdir <file1> <file2> <file3>`
  - Make a Directory without going inside the directory: `mkdir <filename>/<newfile>`
  - Create a child directory without simultaneously creating a parent directory: `mkdir -p <newfile1>/<newfile2>`

 
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
