# -Elk_Stack
Elk Stack
Automated ELK Stack Deployment
The files in this repository were used to configure the network depicted below.
Note: The following image link needs to be updated. Replace diagram_filename.png with the name of your diagram image file.
 
These files have been tested and used to generate a live ELK deployment on Azure. They can be used to either recreate the entire deployment pictured above. Alternatively, select portions of the _____ file may be used to install only certain pieces of it, such as Filebeat.
•	TODO: Enter the playbook file.
This document contains the following details:
•	Description of the Topology
•	Access Policies
•	ELK Configuration
o	Beats in Use
o	Machines Being Monitored
•	How to Use the Ansible Build
Description of the Topology
The main purpose of this network is to expose a load-balanced and monitored instance of DVWA, the D*mn Vulnerable Web Application.
Load balancing ensures that the application will be highly reliable, in addition to restricting traffic to the network.
•	TODO: What aspect of security do load balancers protect? What is the advantage of a jump box? Load balancers protect against DDoS attacks. The advantage of a jump box is that its a secure computer that all admins first connect to before launching any administrative task
Integrating an ELK server allows users to easily monitor the vulnerable VMs for changes to the logs and system traffic.
•	TODO: What does Filebeat watch for? Filebeat monitors the log files you specify
•	TODO: What does Metricbeat record? Metricbeat takes the metrics and statistics that it collects and sends them to the output you specify
The configuration details of each machine may be found below. Note: Use the Markdown Table Generator to add/remove values from the table.
Name	Function	IP Address	Operating System
Jump Box	Gateway	10.0.0.4	Linux
VM1                 	Server	10.0.0.5	Linux
VM2	Server	10.0.0.6	Linux
Elk 	Server		Linux
Access Policies
The machines on the internal network are not exposed to the public Internet.
Only the jumpbox machine can accept connections from the Internet. Access to this machine is only allowed from the following IP addresses:
•	TODO: Add whitelisted IP addresses Public IP address from home
Machines within the network can only be accessed by the jumpbox virtual machine.
•	TODO: Which machine did you allow to access your ELK VM? What was its IP address?



A summary of the access policies in place can be found in the table below.
Name	Publicly Accessible	Allowed IP Addresses
Jump Box	Yes	Home Ip
VM1	No	10.0.0.4
VM2 	No	10.0.0.4
Elk	No	10.0.0.4
Elk Configuration
Ansible was used to automate configuration of the ELK machine. No configuration was performed manually, which is advantageous because...
•	TODO: What is the main advantage of automating configuration with Ansible? The main advantage is that you can automate commands on multiple servers on a single playbook
The playbook implements the following tasks:
•	docker.io
•	python3-pip
•	docker

The following screenshot displays the result of running docker ps after successfully configuring the ELK instance.
Note: The following image link needs to be updated. Replace docker_ps_output.png with the name of your screenshot image file.
 
Target Machines & Beats
This ELK server is configured to monitor the following machines:
•	TODO: List the IP addresses of the machines you are monitoring 10.0.0.5 10.0.0.6 10.0.0.7
We have installed the following Beats on these machines:
•	TODO: Specify which Beats you successfully installed Filebeat and Metricbeat 
These Beats allow us to collect the following information from each machine:
•	TODO: In 1-2 sentences, explain what kind of data each beat collects, and provide 1 example of what you expect to see. E.g., Winlogbeat collects Windows logs, which we use to track user logon events, etc. file beat monitors and collects the changes made to log files while metricbeat collects metrics and statistics 
Using the Playbook
In order to use the playbook, you will need to have an Ansible control node already configured. Assuming you have such a control node provisioned:
SSH into the control node and follow the steps below:
•	Copy the yml file to ansible.
•	Update the host file to include...
•	Run the playbook, and navigate to kibana to check that the installation worked as expected.
TODO: Answer the following questions to fill in the blanks:
•	Which file is the playbook? Where do you copy it?
•	Which file do you update to make Ansible run the playbook on a specific machine? How do I specify which machine to install the ELK server on versus which to install Filebeat on? Edit the etc/ansible/host file and add webserver ip
•	_Which URL do you navigate to in order to check that the ELK server is running? Kibana
