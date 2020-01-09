# linux_user_managing 

enviroment : amazon linux 2

### 1. How to check user permission about root?

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

### 2. How to add user?

~~~

sudo useradd -m example

m means create deafault folder

~~~

### 3. How to access user?

But you have to intialize password

~~~

su example

sudo passwd sm5

su example

~~~

### 4. How to delete user?

~~~

sudo userdel -r [OPTION] example

~~~
