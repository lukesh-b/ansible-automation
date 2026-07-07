# ansible-automation

Ansible playbooks and roles for common Linux infrastructure operations, organised by task area. Each folder is a self-contained example with its own inventory and playbook.

## Role catalogue

| Area | Path | What it does |
|------|------|--------------|
| Database ops | `db-ops/` | Install and configure a database service via playbook |
| Disk ops | `disk-ops/` | End-to-end LVM setup, plus primary and logical partition creation |
| Load balancer | `lb-ops/` | HAProxy and Nginx load balancers built as roles (tasks, handlers, Jinja2 templates) |
| Service ops | `service-ops/` | Manage systemd services across hosts |
| User management | `usr-mgnt/` | Enforce SSH `PermitRootLogin` policy and related user tasks |
| Web ops | `web-ops/` | Provision a web server via a `common` role (tasks + templated MOTD) |

## Concepts demonstrated
- **Roles** with the standard `tasks/`, `handlers/`, `templates/` layout (see `lb-ops/`).
- **Handlers** triggered by `notify`, so services restart only on change.
- **Jinja2 templates** for config files (`haproxy.cfg.j2`, `nginx.conf.j2`, `motd.j2`).
- **Per-example inventories** (`hosts`, `inventory.ini`).
- **Idempotency**: re-running a playbook converges to the same state.

## Usage

```bash
cd lb-ops/haproxy-lb/roles          # example
ansible-playbook -i hosts lb.yml
```

Adjust the inventory (`hosts` / `inventory.ini`) to your target machines, then run the playbook for the area you want. Playbooks assume SSH access and sudo on the targets.
