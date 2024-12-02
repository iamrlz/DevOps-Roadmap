# Shell Script for Beginners 

#### How to run a `script` as a `command`



   - [x]  Example_init

       1. Create a file: `mkdir create-directory-structure.sh`
       2. Create the script file and open it in a text editor: `vim create-directory-structure.sh`
       3. Copy and paste the following script content into the text editor:

         ```
         # Create directories
         mkdir -p /home/iamrlz/countries/Pakistan /home/iamrlz/countries/USA /home/iamrlz/countries/UK 

          # Create capital.txt files and add capital cities' names
            echo "Islamabad" > /home/iamrlz/countries/Pakistan/capital.txt
            echo "Washington, D.C" > /home/iamrlz/countries/USA/capital.txt
            echo "London" > /home/iamrlz/countries/UK/capital.txt

         # Print the system uptime
         uptime

         ```
     
       5. Make the script executable: `chmod +x create-directory-structure.sh`
       6. Run the script: `create-directory-structure.sh`
  

      
       
