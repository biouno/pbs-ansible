# Ansible+Vagrant for PBS Batch Server

This is a simple Ansible playbook with custom rules, files 
and tasks for creating a PBS Batch Server that runs on a 
Vagrant VM.

It was created for the development of a Java API, based on the 
DRMAA spec, for the BioUno project. 

Licensed under the MIT License.

## Running

    vagrant up # starts the VM
    vagrant provision # calls ansible
    sudo su # become root
    qsub test.job -u root

Alternatvely you can use <code>vagrant ssh</code> and qsub, without 
having to impersonate root first.

The server will be available in the torquesever machine, IP 
192.168.1.10, listening to default ports. Preferably install 
torque-client in some other computer to qsub jobs easier to the 
master node.
