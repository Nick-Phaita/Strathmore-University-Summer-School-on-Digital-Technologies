# Introduction to an Ansible Playbook 

In this lab, we show a simple playbook that pings the remote host. 


Run the command (replace the IP with your remote host IP address)

     ansible-playbook -i 192.168.64.6, ping_playbook.yaml


Expected Output 

    PLAY [192.168.64.6] *******************************************************************************************************************************************

    TASK [Gathering Facts] ****************************************************************************************************************************************
    [WARNING]: Platform linux on host 192.168.64.6 is using the discovered Python interpreter at /usr/bin/python3.10, but future installation of another Python interpreter could change the meaning of that path. See https://docs.ansible.com/ansible-core/2.18/reference_appendices/interpreter_discovery.html for more information.
    ok: [192.168.64.6]

    TASK [Ping the target host to check connectivity] *************************************************************************************************************
    ok: [192.168.64.6]

    PLAY RECAP ****************************************************************************************************************************************************
    192.168.64.6               : ok=2    changed=0    unreachable=0    failed=0    skipped=0    rescued=0    ignored=0   