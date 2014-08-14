# ansible-nodejs-role

<a href="https://nodesource.com"><img src="https://nodesource.com/assets/logo.svg" height="10%" width="10%"></a>

This is an ansible role which installs configures the nodesource apt repository and installs NodeJS.

Currently this role supports the following operating systems and releases.

* Ubuntu 
  * precise
  * trusty

## Usage

Install the playbook via galaxy.

```
ansible-galaxy install nodesource.nodejs
```

Then configure it as follows:

```yaml
- hosts: servers
  roles:
     - nodesource.nodejs
```

## Testing

To test this role using docker.

```
docker build .
```

## License

MIT

# Author Information

Mark Wolfe <mark@wolfe.id.au>