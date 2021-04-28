[![ansible palybook pipeline](https://github.com/nicolimo86/devbox/actions/workflows/ansible-playbook.yml/badge.svg)](https://github.com/nicolimo86/devbox/actions/workflows/ansible-playbook.yml) [![ansible role pipeline](https://github.com/nicolimo86/devbox/actions/workflows/ansible-role.yml/badge.svg)](https://github.com/nicolimo86/devbox/actions/workflows/ansible-role.yml)

My Dev Box 
=========

This Vagrant file creates an Ubuntu 18.04 box configured with the following tools:

CLOUD
    
    - aws-cli (2.0.30)

CONFIGURATION MANAGEMENT TOOLS

    - terraform (0.14.9)
    - packer    (1.7.0)
    - ansible   (2.10.7)
    - ansible-lint  (5.0.6)
    - yamllint  (1.26.0)
    - molecule  (3.1.5)
    - test-infra    (6.2.0)
    - task  (3.2.2)
    - buildpack (0.18.0)
    - gopass    (1.12.5)
    - summon    (0.8.3)

CONTAINERS

    - docker
    - docker-dive   (0.9.2)
    - Kind  (0.10.0)
    - kubectl   (1.21.0)


PROGRAMMING

    - python3
    - pip3
    - virtualenv
    - tox   (3.22.0)
    - go    (1.16.3)


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
