# Yellowstone
The main purpose of this network is to expose a load-balanced and monitored instance of DVWA.

Load balancing ensures that the application will be highly available by distributing incoming traffic among other operating virtual networks.
Load balancers affect the overall performance of a companies web traffic while reducing downtime or loss of service.
Integrating an ELK server allows users to easily monitor the vulnerable VMs for changes to the virtual machine and keep log tracks.
-Downloading Filebeat ships logs and data occuring on the machine over to Kibana for documentation.
-Downloading Metricbeat ships the metric and statistics from machine over to Kibana for documentation.

The configuration details of each machine may be found below.


| Name        | Function          | IP Address | Operating System |
|-------------|-------------------|------------|------------------|
| Jump Box    | Default Directory | 10.0.0.16   | Linux           |
| Web 1       | Web Internal VM   | 10.0.0.14   | Linux           |
| Web 2       | Web Internal VM   | 10.0.0.15   | Linux           |
| Yellowstone | Elk Server        | 10.1.0.4    | Linux           |

### Access Policies

The machines on the internal network are not exposed to the public Internet. 
Only the Default Directory and Elk Server can accept connections from the Internet. Access to this machine is only allowed from the following Source IP addresses:
- 141.156.198.203 (personal computer)

Machines within the internal network can only be accessed by internal IP address of the Jump-Box virtual machine.
-Web 1 & 2 can be accessed by Jump-Box Provisioner, IP ADDRESS: 10.0.0.16

A summary of the access policies in place can be found in the table below.

| Name      | Publicly Accessible | Allowed IP Addresses |
|-----------|---------------------|----------------------|
| Jump Box  | Yes                 | 141.156.198.203      |
| Web 1 & 2 | No                  | 10.0.0.16            |
|           |                     |                      |

### Elk Configuration

Ansible was used to automate configuration of the ELK machine. No configuration was performed manually, which is advantageous because...
- Utilizing Ansible is a simpler way to configure and manage even complex commands.

The playbook implements the following tasks:
- Connect to your Ansible container and run docker image to view your image
- Once you've started you will connect to it by running docker run -it cyberxsecurity/ansible/bin/bash
- Once you are in root, you will generate a public ssh/id_rsa.pub; reset passwords in virtual network
- You will edit your Host and config file to gain access and edit your playbook
-A Yaml file will created to run appropriate installations
The following screenshot displays the result of running `docker ps` after successfully configuring the ELK instance.

**Note**: The following image link needs to be updated. Replace `docker_ps_output.png` with the name of your screenshot image file.  
