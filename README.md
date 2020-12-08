# Ansible playbooks. Test task. 
These playbooks is used to:
1. Prepare host for lxc container deployment
1. Configure firewall 
1. Deploy 2 LXC containers, install squid proxy and dante socks inside every container

## Usage

```ansible-playbook <playbook_name.yml> --ask-vault-pass```

* *setup_bridge.yml* configures host, creates bridge, installs required packages.
* *setup_iptables.yml* installs required packages, configures iptables
* *create_containers.yml* creates, 2 containers with installed and configured squid proxy and dante socks server.

## Configuration

Configuration values stored in group_vars/oxy.

## To Do
- [ ] run containers in unprivileged mode
- [ ] encrypt entire group_vars/oxy file ? 
