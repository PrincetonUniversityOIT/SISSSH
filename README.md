## SIS SSH Setup
This contains the .ssh files for accessing SIS windows and linux servers.

**Setup**

 1. Open a terminal (Git Bash for Windows, iTerm2 or similar on Mac) and go to your home directory if not already there. 
 2. Rename your existing .ssh folder! Run
 ```
 mv .ssh .ssh-old
 ``` 
 Do this for two reasons - to have a good backup of your current setup and because you cannot follow the next step if the .ssh folder already exists in your home directory.
 
 3. Run the following command 
```
 git clone https://github.com/PrincetonUniversityOIT/SISSSH.git .ssh
```
 4. Copy your key files from the directory you made in step 2 to .ssh. Run
```
cp .ssh-old/id* .ssh
```  
 5. Run this command to create your User file (enter your vi account for <username>)
```
echo "    User <username>" > ~/.ssh/config.d/princeton.user (username is your vi account)
```
 6. Start sshing!

Macs should have no problem using this repository. Windows computers may require a little coaxing since it appears Git Bash may be installed in different locations on different computers. 
To make this work correctly on a Windows computer two additional steps:

1. Add your Git Bash bin directory to your system path. Git Bash actually has a few bin directories, but you want the Git\usr\bin directory that contains the program `uname`.
2. Edit the proxy.host file so that the connect.exe file path is correct. Git Bash has another program called connect.exe and it is in a DIFFERENT bin folder. You don't need to add this to your path as, due to an openssh for windows bug, you need to include the path to this file in the ssh configuration.

That should be all you need to do to get this working. You can add an 'SSH to Epoxy' function to your Windows terminal by opening terminal, going to Settings, clicking "+Add New Profile", Duplicate your Powershell profile (not your Windows Powershell profile - it should just say Prowershell), and changing the Command Line setting to `C:\Windows\System32\OpenSSH\ssh epoxy`.
