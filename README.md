# motd

Ansible role to set motd banner

## Installation

```yaml
   ansible-galaxy install zerodowntime.motd
```

## Requirements

This role requires Ansible 2.5 or higher.

Supported platforms:

```yaml
  platforms:
    - name: EL
      versions:
        - 7
```

## Default role variables

| Variable name | Required? |  Type  | Description                                           |
|:------------- |:---------:|:------:|:----------------------------------------------------- |
| motd__content |    yes    | string | Package state (present or latest). Default: 'present' |

**All variables are described in [defaults/main.yml](defaults/main.yml) file.**

## Example Playbook

```yaml
  - hosts: all
    become: true
    roles:

    - role: zerodowntime.motd
        motd__content: |

          WARNING !!!: Unauthorized access to this system is forbidden and will be
          prosecuted by law. All connections are monitored and recorded.

          !!! Disconnect IMMEDIATELY if you are not an authorized user!
          ---
```

## License

[Apache License 2.0](LICENSE)

## Support

ansible@zerodowntime.pl
