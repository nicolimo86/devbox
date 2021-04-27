[![ansible palybook pipeline](https://github.com/nicolimo86/devbox/actions/workflows/ansible-playbook.yml/badge.svg)](https://github.com/nicolimo86/devbox/actions/workflows/ansible-playbook.yml) [![ansible role pipeline](https://github.com/nicolimo86/devbox/actions/workflows/ansible-role.yml/badge.svg)](https://github.com/nicolimo86/devbox/actions/workflows/ansible-role.yml)

My Dev Box 
=========

This Vagrant file creates an Ubuntu 18.04 box configured with the following tools:

CLOUD
    
    - aws-cli

INFRASTRACTURE TOOLS

    - terraform
    - packer
    - docker-dive
    - ansible
    - ansible-lint
    - yamllint
    - molecule
    - test-infra
    - task
    - buildpack
    - gopass
    - summon

PROGRAMMING

    - python3
    - pip3
    - virtualenv
    - tox
    - go


Example
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
