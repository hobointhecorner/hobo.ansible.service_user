# hobo.ansible.service_user
Configure user and group(s) for a linux service

Check out [argument_specs.yml](./meta/argument_specs.yml) for available configuration options

## Installation
[Ansible Galaxy](https://galaxy.ansible.com/docs/using/installing.html) can be used to install the role:

`ansible-galaxy install git+https://github.com/hobointhecorner/hobo.ansible.nginx.git[,<branch or commit hash>]`

Or by adding the following to a role's `dependencies` block or `roles` block in a requirements.yml file:

```
- src: git+git@github.com:hobointhecorner/hobo.ansible.service_user.git
  version: v1
  name: hobo.service_user
  service_user_name: example_user
```
