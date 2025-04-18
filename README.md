# ansible-podman-playbooks
 Custom Ansible Podman playbooks for specific open source packages.

## Operating System

These playbooks are designed to run against [AlmaLinux](https://almalinux.org/), tested against AlmaLinux 9 x64.

The playbooks are designed to enable automatic updates, both for the operating system and the containers being run.

## Notes

Generic command to run ansible playbook: `ansible-playbook -i hosts baseline.yml`

For the [n8n](https://www.n8n.io) playbook, for example, copy these files to a new folder, edit the `inventory.yml` file to add your host(s) and SSH username, edit the hostnames and any other variables that you find useful or that need customization in the other files, and then run this command in the folder to, for example, configure n8n fronted by a Caddy reverse proxy:

`ansible-playbook -i inventory.yml baseline.yml caddy.yml n8n.yml`
