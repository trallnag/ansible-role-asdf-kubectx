[![role](https://img.shields.io/ansible/role/55781)](https://galaxy.ansible.com/trallnag/asdf_kubectx)
[![quality](https://img.shields.io/ansible/quality/55781)](https://galaxy.ansible.com/trallnag/asdf_kubectx)
[![downloads](https://img.shields.io/ansible/role/d/55781?label=downloads)](https://galaxy.ansible.com/trallnag/asdf_kubectx)

# Ansible Role `trallnag.asdf_kubectx`

Installs and setups [kubectx][tg] with [`asdf`][asdf] on Linux.

[tg]: https://github.com/gruntwork-io/kubectx
[asdf]: https://github.com/asdf-vm/asdf

Available on [Ansible Galaxy](https://galaxy.ansible.com/trallnag/asdf_kubectx).

## Role Variables

```yaml
asdf_kubectx_version:
  default: 0.31.1
  type: raw
  required: false
  description: >-
    Terraform version to install and activate globally.

asdf_kubectx_git_url:
  default: https://github.com/lotia/asdf-kubectx
  type: raw
  required: false
  description: >-
    Git repo containing the plugin.
```

## Example Playbook

```yaml
- name: Playbook
  hosts: myhost
  remote_user: myuser
  vars:
    rolespec_validate: true
  roles:
    - name: trallnag.asdf_kubectx
      vars:
        asdf_kubectx_version: 0.31.1
        asdf_kubectx_git_url: https://github.com/lotia/asdf-kubectx
```

## Special Requirements

* `asdf` must be installed.

## Special Dependencies

None.

## License

Apache-2.0

## Author Information

Trallnag
