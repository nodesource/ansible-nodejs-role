# ansible-nodejs-role

This is an Ansible role that adds the NodeSource APT repository and installs Node.js.

## Supported Operating Systems

Currently, this role supports the following operating systems and releases:

- **Ubuntu 20.04 LTS** (Focal Fossa)
- **Ubuntu 22.04 LTS** (Jammy Jellyfish)
- **Ubuntu 24.04 LTS** (Noble Numbat)
- **Debian 11** (Bullseye)
- **Debian 12** (Bookworm)

## Usage

### Install and Run Locally

To install and test this role locally, run:

```sh
ANSIBLE_ROLES_PATH=../ ansible-playbook playbook.yml --ask-become-pass
```

### Install via Ansible Galaxy

You can install this role directly from Ansible Galaxy:

```sh
ansible-galaxy install nodesource.node
```

Alternatively, use a `requirements.yml` file:

```yaml
- src: https://github.com/nodesource/ansible-nodejs-role
```

Then install it using:

```sh
ansible-galaxy install -r requirements.yml
```

## Configuration

Example playbook configuration:

```yaml
- hosts: servers
  roles:
    - nodesource.node
```

## Role Variables

- `nodejs_nodesource_pin_priority`: Pin-Priority of the NodeSource repository (default: `500`).
- `nodejs_version`: Set the Node.js version (options: `18.x`, `20.x`, `22.x`, `23.x`, default: `22.x`).

## Testing

This role is automatically tested using GitHub Actions. To see how the CI/CD pipeline is configured, check the `.github/workflows/ci.yml` file.

## Author

Originally developed by Mark Wolfe.
Maintained by NodeSource.

## License

This code is licensed under the MIT License. See the included [LICENSE.md](./LICENSE.md) file for more details.
