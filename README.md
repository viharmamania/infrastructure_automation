# Installation of Ansible

# For MAC

Step 1: Install Ansible via Brew $ brew install ansible

Step 2: Make directory for ansible $ mkdir /usr/local/etc/ansible

Step 3: SSH configuration

Generate an ssh key via key generation command. If you already have one go to next step
Copy your ssh id to the client machine
$ ssh-copy-id user@10.55.xxx.xxx

here 10.55.xxx.xxx is the client machine which we want to configure

Note: If ssh-copy-id is not there, install it using brew

Step 4: Configure the hosts $ vim /usr/local/etc/ansible/hosts Write the following to the hosts file –

[testing] host1 ansible_ssh_host=10.55.xxx.xxx ansible_ssh_user=user

Step 5: Test the ssh connection $ ansible host1 –m ping

# For UBUNTU

Step 1: apt-add-repository ppa:ansible/ansible

Step 2: apt-get update

Step 3: apt-get install ansible

Step 4: ansible --version
