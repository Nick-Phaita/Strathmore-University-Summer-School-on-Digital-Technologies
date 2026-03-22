# Install MicroK8s and Multus CNI on your target machine 

This lab installs MicroK8s and Multus on the target server 

It covers 

- Package management modules and adding External Repositories

- Command line modules 

- Creating repositories 

- Variables and Facts 

- Task Registration & Conditionals

- Error Handling

- Initial Task Verification 


Run the lab as follows in the Lab's root directory 

    ansible-playbook -i inventory/hosts/host.yaml kubernetes_playbook.yaml