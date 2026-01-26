# ansible-auto
# ansible-auto

This repository contains Ansible automation playbooks and roles.

- `playbooks/setup-webserver.yml` - sets up nginx webserver on hosts.
- Role `common` installs nginx and customizes the message of the day.

## Usage

Run:

```bash
ansible-playbook -i inventory.ini playbooks/setup-webserver.yml

