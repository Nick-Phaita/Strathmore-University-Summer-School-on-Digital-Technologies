# A more complex Play book. But, implements Ansible Projects File Structure 


This playbook still installs: 

- Installs Apache web server. 
- Creates the first web page content
- Installs Firewalld and enables port 80 
- Tests web server locally 


Take note of the following files

- ansible.cfg -- We specifically tell Ansible where to locate the roles 

- inventory/hosts.yaml - we have defined the remote hosts there and we do not need to pass the IP address in the Ansible command


In the project's root folder, run the command as follows 

    ansible-playbook -i inventory/hosts.yaml  playbooks/apache_playbook.yaml