# App Store installation role for Ansible

[![GitHub workflow status](https://img.shields.io/github/workflow/status/ayltai/ansible-macos-appstore/CI?style=flat)](https://github.com/ayltai/ansible-macos-appstore/actions)
[![Ansible quality score](https://img.shields.io/badge/quality-5-success)](https://galaxy.ansible.com/ayltai/macos_appstore)
[![Ansible role](https://img.shields.io/badge/role-ayltai.macos_appstore-blue)](https://galaxy.ansible.com/ayltai/macos_appstore)
![Maintenance](https://img.shields.io/maintenance/yes/2020?style=flat)
[![Release](https://img.shields.io/github/release/ayltai/ansible-macos-appstore.svg?style=flat)](https://github.com/ayltai/ansible-macos-appstore/releases)
[![License](https://img.shields.io/github/license/ayltai/ansible-macos-appstore.svg?style=flat)](https://github.com/ayltai/ansible-macos-appstore/blob/master/LICENSE)

Installs applications with App Store on macOS.

[![Buy me a coffee](https://img.shields.io/static/v1?label=Buy%20me%20a&message=coffee&color=important&style=flat&logo=buy-me-a-coffee&logoColor=white)](https://buymeacoff.ee/ayltai)

## Quick start

Make sure you have [Homebrew](https://brew.sh) installed on macOS.

### Installation
```sh
ansible-galaxy install ayltai.macos_appstore
```

### Usage
```yaml
---
- hosts: all
  roles:
    - ayltai.macos_appstore
  vars:
    macos_appstore_apps:
      - 540348655 # The app ID on App Store
      # Example: https://apps.apple.com/us/app/monosnap-screenshot-editor/id540348655
```

## Variables
| Name | Type | Default | Description |
|------|------|---------|-------------|
| `macos_appstore_apps` | `list` | `[]` | A list of application IDs to install with App Store. |
| `macos_mas_package` | `string` | `mas` | The package to install with Homebrew for controlling App Store. |
| `macos_pause` | `integer` | 10 | Controls how long to wait before an information message is dismissed automatically. |

## License
[MIT](https://github.com/ayltai/ansible-macos-appstore/blob/master/LICENSE)

## References
* [Ansible](https://www.ansible.com)
* [Ansible Galaxy](https://galaxy.ansible.com)
