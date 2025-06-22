# Network UPS Tools (NUT) Ansible Role

This role installs and configures Network UPS Tools (NUT) for managing UPS devices.

## Configuration

### Password Security

**IMPORTANT**: The default passwords in `defaults/main.yml` are placeholders and should be changed.
Do not use these passwords in production!

## Usage

Run the playbook with:

```
ansible-playbook playbooks/install_nut.yml -i inventory.yml --limit nuc
```

## Role Variables

See `defaults/main.yml` for all available configuration options.

## UPS Status

Check UPS status with:

```
ansible your_host -i inventory.yml -a "upsc ups"
```

## Supported UPS Devices

This role is configured for a CyberPower CP1500 AVR UPS but can be modified for other UPS devices
by changing the driver and device parameters in the defaults.
