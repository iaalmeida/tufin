# tufin
Ansible stuff for Tufin: Firewall Management &amp; Network Security Policy Software

# Files
inventory: list of Tufin hosts

upgrade.yml: ansible playbook with instructions for upgrade Tufin hosts

# Usage
> ansible-playbook -k -i inventory [-l host] upgrade.yml
