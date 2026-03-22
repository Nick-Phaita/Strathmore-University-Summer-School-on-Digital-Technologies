# Getting Started with Ansible; Installation and Remote Host Testing 


## Install Ansible on Ansible Control Node


Update your system 

    sudo apt update

Install Ansible 

    sudo apt install ansible -y

## Set up SSH to access remote managed hosts 


Since Ansible communicates via SSH, we need to set up SSH on the remote managed hosts, to enable a seamless login without requiring passwords. 


Check if you have existing private and public key combinations

    ls -la ~/.ssh/

If not, in the Ansible control node create the keys.  

    ssh-keygen -t rsa

Copy the generated key to the remote host (change the user and hostname variables in the command)

    ssh-copy-id -i {your_public_key} user@remote_host


Enable Public Key authentication in the managed hosts and disable password login 

    sudo vim /etc/ssh/sshd_config

Look for the lines 

+ PubkeyAuthentication no and uncomment and change to PubkeyAuthentication yes 

+ AuthorizedKeysFile  .ssh/authorized_keys and uncomment 

+ PasswordAuthentication yes uncomment and change to PasswordAuthentication no 

Close and restart sshd 


    sudo systemctl restart sshd 


# Test for Ansible connectivity on the Ansible Control Node


On the Ansible Control Node, test if Ansible can connect to the managed hosts using password-less SSH



    ansible all -i "{remote_host_ip_with_the_comma,}" -u {remote_host_username} -m ping


Expected success output 

    remote_host_ip | SUCCESS => {
    "ansible_facts": {
        "discovered_interpreter_python": "/usr/bin/python3.10"
    },
    "changed": false,
    "ping": "pong"
    } 
