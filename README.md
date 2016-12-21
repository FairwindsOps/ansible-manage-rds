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

The result of the `rds` resource will be stored in `manage_rds_{{ rds_name | replace('-', '_') }}": "{{result}}`. A `rds_name` of `foo-bar` would be set as `manage_rds_foo_bar`.
