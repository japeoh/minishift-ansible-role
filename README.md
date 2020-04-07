# Minishift Ansible Role

Installs [Minishift](https://www.okd.io/minishift/) for use with the KVM driver.

## Variables

| Variable              | Description                                        | Default Value
|-----------------------|----------------------------------------------------|---|
| minishift_base_dir    | The tool specific directories will be created here | ~/tools
| minishift_install_dir | The directory where the binaries will be installed | ~/bin


The specific version to be installed can be controlled by providing the version number and checksum.

| Variable                      | Default Value |
|-------------------------------|---|
| minishift_version             | 1.34.2
| minishift_checksum            | sha256:dd7c3a297ab741b90f62c5389f9ab0f484b094780d6deee0c9aa8e94837741d1
| minishift_kvm_driver_version  | 0.10.0
| minishift_kvm_driver_checksum | md5:fb2ded7b5b20400ef66f0adbc384364e

## Example Playbook

```yaml
- hosts: localhost
  become: yes
  roles:
    - japeoh.minishift
      vars:
        k8s_tools_install_dir: /usr/local/bin
```
    
## License

GPLv3

##  Development

See [here](https://github.com/japeoh/ansible-role-development) for setup.
