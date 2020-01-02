# linux_user_managing 

enviroment : amazon linux 2

### 1. How to check user permission about root?

First you have to access root account

sudo su -> cd /etc/sudoers.d

vi 90-cloud-init-users

* * *

### 2. How to add user?

sudo useradd -m example

m means create deafault folder

* * *

### 3. How to access user?

su example -> But you have to intialize password

-> sudo passwd sm5

-> su example -> Success !
