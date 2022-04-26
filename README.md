# Ansible Role for Opinionated Host Setup

This Ansible role provides an opinionated host setup procedure.

This role is not *yet* on Galaxy. You can install this from the GitHub
repository:

```sh
ansible-galaxy install --force git+https://github.com/telostat/ansible-role-teloshost
```

## Requirements

> **TODO:** Any pre-requisites that may not be covered by Ansible itself or the
> role should be mentioned here. For instance, if the role uses the EC2 module,
> it may be a good idea to mention in this section that the boto package is
> required.

## Role Variables

> **TODO:** A description of the settable variables for this role should go
> here, including any variables that are in defaults/main.yml, vars/main.yml,
> and any variables that can/should be set via parameters to the role. Any
> variables that are read from other roles and/or the global scope (ie.
> hostvars, group vars, etc.) should be mentioned here as well.

## Dependencies

> **TODO:** A list of other roles hosted on Galaxy should go here, plus any
> details in regards to parameters that may need to be set for other roles, or
> variables that are used from other roles.

## Example Playbook

See [playbook.yml](./playbook.yml) for an example playbook and
[config.example.yml](./config.example.yml) for an example configuration file.

## License

BSD-3-Clause

## Author Information

[Telostat Pte Ltd](https://www.telostat.com)

## Testing

Launch a Vagrant machine:

```sh
vagrant up
```

Get the SSH configuration and add it to your personal SSH configuration file:

```sh
vagrant ssh-config --host teloshost >> ~/.ssh/conf.d/teloshost
```

Test SSH connection:

```sh
ssh teloshost
```

Install the role from local git repository:

```sh
ansible-galaxy install --force git+file://<absolute-path-to-this-repository>
```

... or from remote git repository

```sh
ansible-galaxy install --force git+https://github.com/telostat/ansible-role-teloshost
```

Copy the example configuration file:

```sh
cp config.example.yml config.yml
```

..., edit it, and run the test playbook:

```sh
ansible-playbook -i teloshost, -e @config.yml playbook.yml
```
