# linux_user_managing 

enviroment : amazon linux 2

### 1. How to check user permission about root?

First you have to access root account

~~~
sudo su

cd /etc/sudoers.d

vim 90-cloud-init-users

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

su example -> Success !

~~~

### 4. How to delete user?

~~~

sudo userdel -r [OPTION] example

~~~
