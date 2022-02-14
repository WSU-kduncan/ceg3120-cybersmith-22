# Project 2

## Part 1 - Build a VPC

1. Create VPC   
   ![SMITH-VPC created](absolute path)

2. Create Subnet   
   ![SMITH-Subnet created](absolute path)

3. Create Internet Gateway   
   ![SMITH-gw created](absolute path)

4. Create Route Table   
   ![SMITH-routetable created](absolute path)

5. Create Security Group   
   ![SMITH-sg created](absolute path)


## Part 2 - EC2 Instances
1. Instance Details   
   ![instance details](absolute path)
   - AMI Selected: Ubuntu Server 18.04 LTS 
      - Default Username: ubuntu
   - Instance type: t2.micro 

2. Attach Instance to VPC   
   On step 3, under the network tab, select the instance's desired VPC. 
      For my instance, I attached my VPC I created in Part 1, SMITH-VPC.

3. Public IP Auto-Assign   
   Opted not to auto-assign a public ip address because I felt the elastic ip was sufficent. I also didn't want to go back a fix things later on if the address changed.  

4. Storage Volume   
   On step 4, there is an option to adjust the instance's storage. 
      For my instance, I assigned it 16 GB. Up to 30 GB of SSD storage is available for free.  

5. Tag Instance   
   On step 5, there is the option to add tags to the instance like the name. 
      For my instance, I entered "Name" under the Key column, then added "SMITH-instance" in the Value column.  

6. VPC Security Group   
   On step 6, to add the instance to an already created security group, choose "Select an ***existing*** security group", then select the instance's desired security group. 
      For my instance, I selected the security group that I created in Part 1, SMITH-sg.  

7. Elastic IP   
   - To create an Elastic IP for the instance:
      1.  Under "Network & Security", select "Elastic IPs".  
      2.  Click the orange "Allocate Elastic IP address" button in the top right.   
      3. Keep the default settings and add a name tag.   
         - For my instance, under Key I added, "Name" and under Value, "SMITH-EIP".   
      4. Click the orange "Allocate" button in the bottom right. The allocated Elastic IP has been created! 
   - To associate that Elastic IP to an instance: 
      1. Under the "Actions" drop down, select "Associate Elastic IP address".  
      2. Under "Instance" select the instance that will be associated with the Elastic IP.   
      3. Under "Private IP address" select select the given address. This is the IP address that is already associated with the instance.  
      4. Click the orange "Associate" button in the bottom right. The allocated Elastic IP address is now associated with the instance!

8. Hostname   
   - To change the hostname for the instance through the command line:
      1. SSH into the instance
      2. It is a good idea to copy the original config files before changing hostname.   
         `cp /etc/hostname /etc/hostname.old`
      3. Using `sudo`, edit the hostname file. Delete the old name and replace it with the new host name.   
         `sudo vim /etc/hostname`   
         - For my instance, I changed it to SMITH-Ubuntu.   
      4. If necessary, edit the /etc/hosts file using `sudo`.   
         `sudo vim /etc/hosts`   
         - In my case, the old hostname was not mentioned, so I did not have to edit this file. 
      5. Reboot the system and SSH back in. 
         `sudo reboot` 

9. Successful SSH   
   ![successful SSH](absolute path)