# ansible_tutorial

 https://www.youtube.com/watch?v=3RiVKs8GHYQ&list=PLT98CRl2KxKEUHie1m24-wkyHpEsa4Y70
 All of the tutorials in this repo are from the "Getting started with Ansible" tutorial series
 by LearnLinuxTV
 
 OpenSSH - standard for remote automation and execution on servers/other computers must be installed on the     workstation and servers

SSH Keys - Secure the connection into servers from devices. Tutorial uses command:
    - "ssh-keygen -t ed25519 -C /"user default/""


Network Topology: 

	workstation : 192.168.60.10
	server-1 : 192.168.60.11
	server-2 : 192.168.60.12
	server-3 : 192.168.60.13


Useful commands: 

  - "ansible all -m gather_facts" -> useful for finding info about all of the clients within inventory. You can use "--limit <ip>" to narrow down clients

  - "ansible-playbook --ask-become-pass site.yml" to run basic plays

  - "ansible-playbook --tags ubuntu --ask-become-pass site.yml" to run plays only with specified tags. In this case it will only run plays with tag: Ubuntu
    For multiple tags: use parentheses: ex: --tags "apache Ubuntu"
