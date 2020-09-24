# tufin
Ansible stuff for Tufin: Firewall Management &amp; Network Security Policy Software

(Rehat Ansible, described in https://docs.ansible.com/ansible/latest/index.html)

# Files
inventory: list of Tufin hosts, ordered according Tufin upgrade instructions (SecureTrack, Distribution Server, SecureChange, SecureApp)

upgrade.yml: ansible playbook with instructions for upgrade Tufin hosts

# Usage
> ansible-playbook -k -i inventory [-l host] upgrade.yml

-k askes you for the root passwd (I have to improve this!).

# Notes
I don't have access to a HA environment neither to a SecureApp, so use it more carefully in these scenarios

# How can I use it?
1) Review the Installation Instructions for the new release, prior to upgrade :)
1) download the new TOS version to ~/src folder
2) execute this playbook according **Usage**

# upgrade.yml, what this ansible playbook does?
1) creates a remote destination folder ~/src
2) uploads the upgrade file to remote destination folder
3) unpacks the upgrade file
4) executes the screen upgrade command, as recommended by Tufin
