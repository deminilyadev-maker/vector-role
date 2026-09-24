# Vector Role

Ansible role for installing Vector on Linux hosts.

## Description

This role installs Vector from the official Vector archive.

The role performs the following tasks:

- creates the `/opt/vector` installation directory;
- downloads the specified Vector version;
- extracts the Vector archive to `/opt/vector`.

The role is designed to be used as part of the Ansible playbook for deploying ClickHouse, Vector and Lighthouse.

## Requirements

- Ansible
- Linux target host
- DNF/YUM-based Linux distribution
- Internet access from the target host

## Role Variables

### `vector_version`

Specifies the Vector version to install.

Default value:

```yaml
vector_version: "0.34.1"
```
## Dependencies

This role has no dependencies on other Ansible roles.

## Versioning

The role uses Semantic Versioning.

Current version:

```text
1.0.0
```

## Author

**Демин Илья Викторович**
