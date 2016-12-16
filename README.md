Manage RDS
=========

## Usage
```
- role: reactiveops.manage-rds
  rds_environment: "{{ env }}"
  rds_context: "{{ context }}"
  rds_security_group_ids: "{{ hostvars[inventory_hostname][context + '_data'] }}"
  rds_master_username: 'db_user1'
  rds_master_password: 'db_pass_2CH88NG33Eme#^^!'
  rds_engine: 'postgres'
  rds_engine_version: '9.5.4'
```

It is also possible to use this role to modify an instance. To do so it is easiest to override settings from the command line:

```shell
ansible-playbook stack.yml  -e 'rds_command=modify' -e 'apply_immediately=yes'
```
