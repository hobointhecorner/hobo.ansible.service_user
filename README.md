# hobo.ansible.service_user
Configure user and group(s) for a linux service

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

## Variables
|               Name                |     Type     | Required |       Default       | Description |
|-----------------------------------|--------------|----------|---------------------|-------------|
|         service_user_name         | string       | **yes**  |                     | The name of the user and group to be created |
|          service_user_id          | string       |   no     |                     | The UID of the user, will use a system-provided UID if not defined |
|         service_user_group_name        | string       |   no     | `service_user_name` | The name of the group to be created, defaults to the value of `service_user_name` |
|          service_user_group_id         | string       |   no     |                     | The GID of the group, will use a system-provided GID if not defined |
|     service_user_additional_groups     | list(string) |   no     |        `[]`         | A list of additional groups of which the service user should be a member |
|  service_user_additional_group_members | list(string) |   no     |        `[]`         | A list of additional users of which should be members of the service group |
| service_user_extended_group_membership | bool         |   no     |       `false`       | Add users provided in `service_user_additional_group_members` to groups provided in `service_user_additional_groups` |
