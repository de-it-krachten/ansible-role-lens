[![CI](https://github.com/de-it-krachten/ansible-role-lens/workflows/CI/badge.svg?event=push)](https://github.com/de-it-krachten/ansible-role-lens/actions?query=workflow%3ACI)


# ansible-role-lens

Installs Lens desktop<br>
https://k8slens.dev<br> 



## Dependencies

#### Roles
None

#### Collections
- community.general

## Platforms

Supported platforms

- Red Hat Enterprise Linux 7<sup>1</sup>
- Red Hat Enterprise Linux 8<sup>1</sup>
- Red Hat Enterprise Linux 9<sup>1</sup>
- CentOS 7
- RockyLinux 8
- RockyLinux 9
- OracleLinux 8
- OracleLinux 9
- AlmaLinux 8
- AlmaLinux 9
- Debian 10 (Buster)
- Debian 11 (Bullseye)
- Ubuntu 18.04 LTS
- Ubuntu 20.04 LTS
- Ubuntu 22.04 LTS
- Fedora 36
- Fedora 37

Note:
<sup>1</sup> : no automated testing is performed on these platforms

## Role Variables
### defaults/main.yml
<pre><code>
# Lens desktop executable
lens_executable: /usr/local/bin/lens

# Lens download url
lens_url: https://api.k8slens.dev/binaries/latest.x86_64.AppImage
</pre></code>




## Example Playbook
### molecule/default/converge.yml
<pre><code>
- name: sample playbook for role 'lens'
  hosts: all
  become: "yes"
  roles:
    - deitkrachten.gnome_desktop
  tasks:
    - name: Include role 'lens'
      ansible.builtin.include_role:
        name: lens
</pre></code>
