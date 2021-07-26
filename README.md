# Ansible Role: SystemD Resolvd

[![License](https://img.shields.io/badge/license-MIT%20License-brightgreen.svg)](https://opensource.org/licenses/MIT)
[![GitHub tag](https://img.shields.io/github/tag/OnkelDom/ansible-role-systemd-resolved.svg)](https://github.com/OnkelDom/ansible-role-systemd-resolved/tags)
[![GitHub issues](https://img.shields.io/github/issues/OnkelDom/ansible-role-systemd-resolved)](https://github.com/OnkelDom/ansible-role-systemd-resolved/issues)
[![GitHub license](https://img.shields.io/github/license/OnkelDom/ansible-role-systemd-resolved)](https://github.com/OnkelDom/ansible-role-systemd-resolved/blob/master/LICENSE)

## Description

Configure Systemd Resolvd using ansible.

## Requirements

- Ansible >= 2.5 (It might work on previous versions, but we cannot guarantee it)

## Role Variables

All variables which can be overridden are stored in [defaults/main.yml](defaults/main.yml) file as well as in table below.

| Name           | Default Value | Description                        |
| -------------- | ------------- | -----------------------------------|
| `systemd_resolved_dns_server` | "127.0.0.1" | Set local DNS-Server |
| `systemd_resolved_dns_stublistener` | "no" | disable stub listener |

## Example

```yaml
- hosts: all
  roles:
    - onkeldom.ansible-role-systemd-resolved
  vars:
    systemd_resolved_dns_server: "127.0.0.1"
    systemd_resolved_dns_stublistener: "no"
```

## Contributing

See [contributor guideline](CONTRIBUTING.md).

## License

This project is licensed under MIT License. See [LICENSE](/LICENSE) for more details.
