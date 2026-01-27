## SSH Root Login Management with Ansible

This Ansible playbook manages the `PermitRootLogin` directive in `/etc/ssh/sshd_config`
across all target hosts using privilege escalation. It safely updates commented or
existing values, creates timestamped backups before making changes, and validates
the SSH configuration syntax prior to restarting the SSH service.

The playbook is designed to be idempotent and distribution-aware, ensuring reliable
execution across multiple Linux distributions while minimizing the risk of SSH lockouts.

### Usage

Run the playbook using the following command:

```bash
ansible-playbook permit_root_login.yml -i inventory
```

```
Ensure you have SSH access and sufficient privileges (sudo/root) on the target hosts
before execution.
```
