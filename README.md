# Ansible mount cephfs volume

This role takes care of mounting a cephfs volume on a host. It is

## Requirements

None

## Role Variables

| Variable          | Description                    | Default |
| ----------------- | ------------------------------ | ------- |
| lab_name          | Name of the lab                |         |
| ceph_mon          | IP address of the ceph monitor |         |
| ceph_cluster_name | Name of the ceph cluster       |         |

## Dependencies

None

## Example Playbook

```yaml
- name: 'Mount required volumes'
  hosts: all
  remote_user: root
  tasks:
    - name: 'Mount the cephfs volume'
      ansible.builtin.include_role:
        name: ansible_mount_cephfs_volume
      vars:
        lab_name: 'ivrl'
        ceph_mon: 'icitsrv5.epfl.ch'
        ceph_cluster_name: 'floki'
```

## License

MIT

## Author Information

Emmanuel Jaep
