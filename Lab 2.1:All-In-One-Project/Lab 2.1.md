# A more complex Play book. But it is an all in one 

This playbook installs: 

- Installs Apache web server. 
- Creates the first web page content
- Installs Firewalld and enables port 80 
- Tests web server locally 


Run the playbook as follows (replace the IP with your remote host IP address)

    ansible-playbook -i  192.168.64.6, apache_playbook.yaml 