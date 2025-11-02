# Ansible-installs-Nginx
Jenkins and Ansible setup that automates configuration across three worker nodes.   Ansible installs Nginx and updates packages using playbooks, while Jenkins runs the pipeline defined in the Jenkinsfile to deploy and manage configurations.


# 🚀 Jenkins and Ansible Server Setup

This project shows how I used Jenkins and Ansible together to automate server configuration across multiple worker nodes.

## 🧱 Project Overview

An Ansible control node and Jenkins server were created to work together for automation.  
Three worker nodes were also created, and SSH connections were set up between the control node and each worker.  
Ansible manages configuration tasks while Jenkins handles automation through a pipeline.


## 🗂 Files

`ansible.cfg` tells Ansible to use the inventory file named `hosts`  
`hosts` lists the IP addresses of all three worker nodes  
`install-nginx.yml` installs and starts Nginx on each worker node  
`update.yml` updates all required packages on the servers  
`Jenkinsfile` is a declarative pipeline that runs Ansible playbooks for setup and deployment


## ⚙️ How It Works

Jenkins connects to the Ansible server using the Jenkinsfile instructions  
Ansible reads the inventory from `hosts` and runs playbooks like `install-nginx.yml` and `update.yml` on all worker nodes  
Nginx and system updates are installed automatically using SSH


## 🧰 Tools Used

Jenkins  
Ansible  
SSH  
YAML  
Linux EC2 instances on AWS  

## ▶️ Purpose

This setup demonstrates continuous integration and configuration management using Jenkins and Ansible.  
It automates software installation, package updates, and web server setup across multiple nodes.

## 🔮 Future Plans

Add more playbooks for Docker installation and system monitoring  
Integrate Jenkins notifications and error handling

