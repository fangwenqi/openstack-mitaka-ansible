# Openstack-Mitaka_With-Ansible
Openstack Mitaka With Ansible
#Prerequisites:-
One node with Ansible installed. (You can use ansible in any one of openstack nodes or in separate node)
2 nodes with below configurations.

i. VM1(Controller) - Hard disk 50GB, RAM 4 GB, 1 CPU, Interfaces 3 ( 1 NAT, 2 Host only adapter vboxnet0 )

ii. VM2(Compute) - Hard disk 50GB, RAM 2 GB, 2 CPU, Interfaces 3 (1 NAT, 2 Host only adapter vboxnet0 )

All 2 VMs should communicate with each other and with ansible node.

#How to use :-
. Clone the abloe code or download the zip file.
  git clone https://github.com/vrajasekhar123/openstack-mitaka-ansible.git
  
. Copy the cloned directory (openstack-mitaka-ansible) to any of the location. Suppose, /usr/local/

  cp - rp openstack-mitaka-ansible /usr/local/
  
  (or)
  unzip openstack-mitaka-ansible-master.zip /usr/local/
   
. Goto /usr/local/openstack-mitaka-ansible/

   cd /usr/local/openstack-mitaka-ansible/
   
. And edit the below two file.

i. inventory/hosts :- Host file to ansible. Define the controller and compute IPs here.

ii. group_vars/all:- Define IPs, user names and passwords. 

And you can simply install the OpenStack with single command from openstack_main.yml file location.

#command:-
ansible-playbook -i inventory/ openstack_main.yml -vvv
