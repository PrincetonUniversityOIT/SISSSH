## SIS SSH Setup
This contains the .ssh files for accessing SIS windows and linux servers.

**Setup**

 1. Open a terminal (Git Bash for Windows, iTerm2 or similar on Mac) and go to your home directory if not already there. 
 2. Rename your existing .ssh folder! Run `mv .ssh .ssh-old` Do this for two reasons - to have a good backup of your current setup and because you cannot follow the next step if the .ssh folder already exists in your home directory.
 3. Run the following command `git clone org-67022956@github.com:PrincetonUniversityOIT/SISSSH.git .ssh`
 4. Copy your key files from the directory you made in step 2 to .ssh. Run `cp .ssh-old/id* .ssh`  

