# Disk LVM Complete Setup - Ansible Playbook

This repository contains an Ansible playbook that automates the setup of disk partitioning, LVM configuration, and filesystem mounting on a target group of database servers (`dbservers`).

##  Project Structure
```yaml
disk-prj3/
├── disk_lvm_complete_setup/
│ ├── full_lvm.yml # Main Ansible playbook
│ └── hosts # Inventory file
```

##  Description

The playbook performs the following tasks on the `/dev/sdc` device of the target hosts:

1. Creates a **primary partition** 
2. Gathers partition info
3. Creates an **extended partition**
4. Creates a **logical partition** 
5. Sets up a **Volume Group** named `vgdata`
6. Creates a **Logical Volume** (`lvdata`)
7. Formats the LV with the **XFS** filesystem
8. Mounts it

Run the playbook:
```bash
ansible-playbook -i hosts full_lvm.yml
```

 NOTE: This playbook modifies disk partitions and filesystems. Ensure to use as a test or backup the existing partition first

## License
This project is licensed under the MIT License.


