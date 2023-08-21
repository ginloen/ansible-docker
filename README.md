# ansible-docker
Prerequisites
- Ansible must be installed on control node
- 3 additional files must be created in the same folder
    1. inventory (containing IP address of managed nodes)
    2. ansible.cfg (specifying defaults e.g.)
    ```
    [defaults]

    inventory = inventory

    host_key_checking = False

    deprecation_warnings = False

    remote_user = ubuntu

    private_key_file = ansible.pem
    ```
    3. private_key_file (for SSH into managed nodes)

Ansible commands:
```
ansible all -m ping #check SSH connectivity

ansible-playbook <playbook_yaml_file> #run ansible playbook
```
