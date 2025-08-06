[![CI](https://github.com/de-it-krachten/ansible-role-lens/workflows/CI/badge.svg?event=push)](https://github.com/de-it-krachten/ansible-role-lens/actions?query=workflow%3ACI)


# ansible-role-lens

Installs Lens desktop<br>
https://k8slens.dev<br> 



## Dependencies

#### Roles
None

#### Collections
None

## Platforms

Supported platforms

- Red Hat Enterprise Linux 8<sup>1</sup>
- Red Hat Enterprise Linux 9<sup>1</sup>
- Red Hat Enterprise Linux 10<sup>1</sup>
- RockyLinux 8
- RockyLinux 9
- RockyLinux 10
- OracleLinux 8
- OracleLinux 9
- OracleLinux 10
- AlmaLinux 8
- AlmaLinux 9
- AlmaLinux 10
- Debian 11 (Bullseye)
- Debian 12 (Bookworm)
- Debian 13 (Trixie)
- Ubuntu 20.04 LTS
- Ubuntu 22.04 LTS
- Ubuntu 24.04 LTS
- Fedora 41
- Fedora 42

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
  become: 'yes'
  roles:
    - deitkrachten.gnome_desktop
  tasks:
    - name: Include role 'lens'
      ansible.builtin.include_role:
        name: lens
</pre></code>
