# linux_user_managing 

enviroment : amazon linux 2

### How to check user permission about root?

First you have to access root account

~~~
sudo su

cd /etc/sudoers.d

vim 90-cloud-init-users

# Created by cloud-init v. 18.5-2.amzn2 on Thu, 09 Jan 2020 03:32:43 +0000
# User rules for ec2-user
ec2-user ALL=(ALL) NOPASSWD:ALL
example1 ALL=(ALL) NOPASSWD:ALL
example2 ALL=(ALL) NOPASSWD:ALL

~~~

### How to add user?

~~~

sudo useradd -m sm5

m means create deafault folder

~~~

### How to access user?

But you have to intialize password

~~~

[ec2-user@ip-10-0-0-86 /]$ cd /home/
[ec2-user@ip-10-0-0-86 home]$ ls
ec2-user  sm5
[ec2-user@ip-10-0-0-86 home]$ cd sm5
-bash: cd: sm5: Permission denied
[ec2-user@ip-10-0-0-86 home]$ su sm5
Password: 

crtrl + c

you need password setting

[ec2-user@ip-10-0-0-86 home]$ sudo passwd sm5
Changing password for user sm5.
New password: 
Retype new password: 
passwd: all authentication tokens updated successfully.
[ec2-user@ip-10-0-0-86 home]$ su sm5
Password: 
[sm5@ip-10-0-0-86 home]$ 

~~~

### How to delete user?

~~~

[ec2-user@ip-10-0-0-86 ~]$ sudo userdel -r sm5
[ec2-user@ip-10-0-0-86 ~]$ cd /home/ && ls
ec2-user

~~~

### The difference between sudo, su, su-
