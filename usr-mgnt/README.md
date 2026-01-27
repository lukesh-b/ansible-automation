## Permit Root Login via Ansible

This Ansible playbook enables `PermitRootLogin yes` in `/etc/ssh/sshd_config`.
It runs on all target hosts with privilege escalation.
The playbook ensures the setting is present using `lineinfile`.
SSHD is automatically restarted to apply the change.

