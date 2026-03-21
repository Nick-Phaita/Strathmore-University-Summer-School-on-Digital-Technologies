# Getting Started with Ansible; Installation and Remote Host Testing 


## Install Ansible on Ansible Control Node

``` sudo apt update ```
``` sudo apt install ansible -y ```

## Set up SSH to access remote managed hosts 


Since Ansible communicates via SSH, we need to set up SSH on the remote managed hosts, to enable a seamless login without requiring passwords. 

On the Ansible control node type 

``` ssh-keygen -t rsa ```

Copy the generated key to the remote host (change the user and hostname variables in the command)

``` ssh-copy-id user@remote_host ```