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
```
