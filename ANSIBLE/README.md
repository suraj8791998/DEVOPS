# ANSIBLE
Establishing password less authentication between servers

# Steps to Establish password-less authentication

sudo apt update -y  **Ansible server**

sudo apt install ansible -y  **Ansible server**

ssh-keygen **Ansible server**

Go to the above path as mentioned in above and go for cat ID_RSA_PUB

Copy the content

Login to Target Server

ssh-keygen **Target Server**

Go to the above path as mentioned in above and go for Authorized keys

Paste the content that you have copied above

ssh @private_ip_address for the authentication **Ansible server**
