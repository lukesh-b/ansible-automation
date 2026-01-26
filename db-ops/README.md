# DBs-prj4 
(Simple MariaDB and PostgreSQL Install)

This project provides a lightweight Ansible playbook for installing and enabling **MariaDB** and **PostgreSQL** on remote Linux servers.

## Project Files

- `hosts` — Inventory file listing your target servers
- `playbook.yml` — Main Ansible playbook
- `README.md` — This documentation
- `LICENSE` — MIT License

## Requirements

- Control node with Ansible installed
- Target servers should be Debian/Ubuntu-based
- SSH access with a user that has sudo privileges

To run the playbook:
```bash
ansible-playbook -i hosts playbook.yml
```


