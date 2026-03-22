# An NGINX Play book. But, implements a different Ansible Projects File Structure 

We demonstrate a different way of organizing an Ansible project 

This playbook: 

- Installs NGINX. 
- Copies index.html to nginx directory
- Updates index.html file with update.html in the default nginx directory


Take note, we have a hosts file, this time in .ini 

Run the playbook as follows in the project's root directory 

    ansible-playbook -i inventory/hosts/hosts nginx_playbook.yaml
