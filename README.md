[![ansible palybook pipeline](https://github.com/nicolimo86/devbox/actions/workflows/ansible-playbook.yml/badge.svg)](https://github.com/nicolimo86/devbox/actions/workflows/ansible-playbook.yml) [![ansible role pipeline](https://github.com/nicolimo86/devbox/actions/workflows/ansible-role.yml/badge.svg)](https://github.com/nicolimo86/devbox/actions/workflows/ansible-role.yml)

My Dev Box 
=========

This Vagrant file defines my personal devbox. It creates an Ubuntu 18.04 box configured with the following tools:

CLOUD
    
    - aws-cli

CONFIGURATION MANAGEMENT TOOLS

    - terraform     
    - packer        
    - ansible       
    - ansible-lint  
    - yamllint      
    - molecule      
    - test-infra    
    - task          
    - buildpack     
    - gopass        
    - summon        

CONTAINERS

    - docker        
    - docker-dive   
    - Kind          
    - kubectl       
    - Helm          


PROGRAMMING

    - python3
    - pip3
    - virtualenv
    - tox        
    - go         
    - shellcheck 


Prerequisites
----------------

    - install virtualbox
    - install vagrant

Optional:

    vagrant plugin install vagrant-vbguest #virtualbox guest additions
    vagrant plugin install vagrant-hosts #update /etc/hosts host
    vagrant plugin install vagrant-netinfo #show forwared ports
    vagrant plugin install vagrant-disksize #resize disk in virtualbox
    vagrant plugin install vagrant-scp


Usage
----------------

Starting the box:

    vagrant up

Connecting to the box:

    vagrant ssh

VSCode configuration
----------------

Install Remote Development plugin.
Launch VS Code Quick Open (Ctrl+P), paste the following command, and press enter.
    
    ext install ms-vscode-remote.vscode-remote-extensionpack

Add Vagrant host to the ssh config:
    
    vagrant ssh-config >> ~/.ssh/config

Connect to the Vagrant host from inside VSCode:
    
    F1 -> Remote-SSH: Connect to Host...
