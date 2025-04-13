# Remove Package Role

This role removes packages and their associated services from the system.

## Requirements

None.

## Role Variables

- `package_name`: Name of the package to remove (required)
- `stop_service`: Whether to stop the service before removing the package (default: true)
- `direct_command`: Whether to use a direct command to stop the service (default: false)
- `additional_packages`: Additional packages to remove (dependencies) (default: [])

## Example Playbook

```yaml
- name: Remove UFW
  hosts: your_hosts
  roles:
    - role: remove_package
      vars:
        package_name: ufw
        direct_command: true

- name: Remove Apache
  hosts: your_hosts
  roles:
    - role: remove_package
      vars:
        package_name: apache2
        additional_packages: 
          - libapache2-mod-php
          - php
```

## License

MIT

## Author Information

Created by Your Name 