Antkey
======

Antkey is a small bash script for mac osx that pulls your sfdc passwords from the key chain and runs ant for salesforce.com metadata migration.  

Quick Start
-----------------
Create two entries in the key chain:  
  
`security add-generic-password -a sfdctestpassword -s "Sfdc Test Login: sfdctestpassword" -w yourpassword`  
`security add-generic-password -a sfdcpassword -s "Sfdc Prod Login: sfdcpassword" -w yourpassword`  
  
*Replace "yourpassword" with your password*
  
Update your build.properties and build.xml to use the sfdcpassword and sfdctestpassword as in the sample files in this repo.  

  

Warning
-------------------
This script creates the following temporary files:  
> build.bak  
> new.properties - holds your password in clear  
> new2.properties - holds your password in clear  
  
**Make sure to delete these temporary files in case the script fails to delete them**
