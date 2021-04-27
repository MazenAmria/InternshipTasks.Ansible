# Ansible Task

Write an ansible playbook that does the following:

- Read items from Yaml file, Example:

```
---
hypervisor_files:
  - {path: /root/cbis-installer/templates/generic/firstboot/cbis/general_utils}
undercloud_files:
  - {path: /home/stack/templates/firstboot/cbis/general_utils, folder: files}
  - {path: /usr/share/cbis/undercloud/templates/generic/firstboot/cbis/general_utils}
  - {path: /usr/share/cbis}
overcloud_files:
  - {path: /usr/share/cbis/undercloud/templates/generic/firstboot/cbis/general_utils}
  - {path: /usr/share/cbis/}
  - {path: /usr/share/cbis/utils}
```

- Copy the files from the above hostgroups to the master server to a defined location, &quot;As variable in the
  same YAML file or as an argument&quot;

Solved in `fetch-playbook.yml`

- Add another playbook to compare the files from two different runs. And display the diff.
- Not only files content need to be compared between runs, but also Permissions/Owners/Group/SELinux

Solved in `diff-playbook.yml`
