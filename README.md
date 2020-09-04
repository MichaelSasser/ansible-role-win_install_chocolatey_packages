# michaelsasser.win-install-chocolatey-packages

Download and (un)install packages with chocolatey. 

## Role Variables

| Varibale                      | Description                                        |
|-------------------------------|----------------------------------------------------|
| chocolatey_install_packages   | A list of packages to be installed by chocolatey   |
| chocolatey_uninstall_packages | A list of packages to be uninstalled by chocolatey |

## Example Playbook

```yaml
- hosts: all
  become: true
  roles:
    - michaelsasser.win-install-chocolatey-packages
  vars:
    - chocolatey_install_packages:
        - python3
        - git
    - chocolatey_uninstall_packages:
        - python2
```

You can use `choco search PACKAGENAME` to look for packages.

## License

Copyright &copy; 2020 Michael Sasser <Info@MichaelSasser.org>. Released under
the GPLv3 license.
