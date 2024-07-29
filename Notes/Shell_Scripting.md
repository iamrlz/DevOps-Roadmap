# Shell Script for Beginners 

#### How to run a `script` as a `command`



   - [x]  Example_init

       1. Create a file: `mkdir create-directory-structure.sh`
       2. Create the script file and open it in a text editor: `vim create-directory-structure.sh`
       3. Copy and paste the following script content into the text editor:

         ```
         # Create directories
         mkdir -p /home/bob/countries/USA /home/bob/countries/UK /home/bob/countries/India

          # Create capital.txt files and add capital cities' names
            echo "Washington, D.C" > /home/bob/countries/USA/capital.txt
            echo "London" > /home/bob/countries/UK/capital.txt
            echo "New Delhi" > /home/bob/countries/India/capital.txt

         # Print the system uptime
         uptime

         ```
     
       5. Make the script executable: `chmod +x create-directory-structure.sh`
       6. Run the script: `create-directory-structure.sh`
  

      
       
