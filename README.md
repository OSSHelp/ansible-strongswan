# strongswan

[![Build Status](https://drone.osshelp.ru/api/badges/ansible/strongswan/status.svg)](https://drone.osshelp.ru/ansible/strongswan)

Ansible role for strongSwan installation and configuration.

## Usage (example)

```yaml
    - role: strongswan
```

Check [this playbook](molecule/custom/playbook.yml) for example of role call with custom parameters.

## Available parameters

### Main

| Param | Default | Description |
| -------- | -------- | -------- |
| `strongswan_setup` | `full` | Setup mode. See [OSSHelp KB article](https://oss.help/kb4895) |
| `strongswan_conn_default` | see [defaults](defaults/main.yml) | List of default conn parameters. You could override it with yours. |
| `strongswan_conn` | `[]` | Array to describe connections with. |
| `strongswan_place_certs` | `false` | Whether to place certs from repo to server. When enabling make sure to set appropriate source and destination paths. Check [this playbook](molecule/custom/playbook.yml) for example. |

### Misc

No need to change these.

| Param | Default | Description |
| -------- | -------- | -------- |
| `strongswan_packages` | `[strongswan]` | Package list to install |
| `strongswan_config_base` | `/etc` | Directory where main configuration files will be stored. Not created by default. |

## Useful links

- [Official documentation](https://www.strongswan.org/documentation.html)
- [Our article: Site-to-Site VPN](https://oss.help/kb509)
- [Our article: IPSec-tunnel](https://oss.help/kb518)

## TODO

None, so far.

## License

GPL3

## Author

OSSHelp Team, see <https://oss.help>
