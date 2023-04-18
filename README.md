# ActiveDirectoryHomeLab
All things related to my active directory experiments!
Loaded an ISO into virtualbox and got to work. After windows server 2016 was installed. 
Started getting into best practices and named my server DC01-WV bc I am from WV and it sounds way more legit compared to the name it was giving me. 
Went through and created my forest, then setting up Active Directory by installing it from the manage window. 



Installed a RAS/NAT
-to allow our clients to get access to the internet. 
-went to tools in my server and clicked on routing & remote access.
-set up NAT 
*insert NAT Screenshot*

-Went to Manage;add roles and features 
-looked up and added DHCP Server
*insert DHCP screenshot*

-Click on tools and click on DHCP
*reminder the whole role of DHCP is to allow computers to automatically get their IP addresses*
-look for IPv4 and click on add scope.
*InsertDHCPRangeScopeScreenShot*
-Checked and confirmed IPv4 was green and running

-Used link to obtain scripts from github
-extracted powershell script folder on desktop
-ran powershell ISE as admin and opened up script folder
-TRIED to run powershell but ran into an error message

-Typed in command Set-ExecutionPolicy unrestricted
*insert powershellcommand set up Screenshot*
-The powershell command we are using is essentially creating a bunch of users for our active directory server. 

-Typed in cd c:\users\a-alexis\desktop\AD-PS-master
*this command placed us in the directory of our desktop's sscript folder.*
*Kept getting an error that the .text file could not be found. which resulted in me staring at what I was doing. When it installed I didn't realize the typo in my command.
switched to cd c:\users\a-alexis\desktop\AD_PS-master which continued giving me errors because it couldn't find the .text file then I realized I had to change the directory one more time and create the new command: cd c:\users\a-alexis\desktop\AD_PS-master\AD_PS-master

this worked. 
*insert thousands of accounts screenshot*

-Went to Virtual Box and created a new Windows 10 machine
*insert screenshot of network settings for machine*

Another problem.. I didn't have a default gateway 
*insert default gateway screenshot*
-I went through and opened my DC back up. Looked through the DHCP settings.
Realized that I didn't have a router set up in my server options so I added that. 

I then tried running ipconfig on my client1 computer and still wasn't getting an internet connection. I went back to my domain controller, looked into my internal network and realized I didn't assign an IP address. I corrected this and finally fixed my issue. 
*Insertscreenshot*

*insertwhoamiconfirmation* 

Excited to have my own little lab to run experiments on now!



