---
layout: video
title: "Using Ansible Playbooks to automate deployment of various services on FreeBSD"
date: 2022-06-03
author: Roller Angel
youtube: t03fVZn5nKs
---
This talk will focus on using Ansible Playbooks to automate deployment of various services on FreeBSD. Topics covered will range from using Ansible to control local and remote FreeBSD machines, using the secure Ansible Vault to encrypt secrets used in Ansible Playbooks, storing common command line arguments into a configuration file, creating roles like database and appserver for separation of concerns as well as using a common role to store configuration to be used across many or all machines. Many Ansible concepts will be covered including: modules, tasks, templates, roles and variables. Some specific modules that will be discussed are synchronize, file, lineinfile, blockinfile, shell, command, service, package, git, copy and more!

FreeBSD pairs very well with Ansible and Python web applications along with many other useful services. This talk will include a demo showing the ease of deploying a FastAPI Python web application on a FreeBSD remote machine and will also include the code for this Ansible deployment playbook for attendees to download and peruse and their leisure. The app deployment includes configuring PostgreSQL, Nginx, Let's Encrypt and FreeBSD to all work together to make the final product available as a public service on the internet. In this case the service will be deployed on a DigitalOcean droplet but the concepts apply to using FreeBSD on other online computing services or home labs as well.
