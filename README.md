Manage RDS
=========

## Usage
```
- role: reactiveops.manage-rds
  rds_environment: "{{ env }}"
  rds_context: "{{ context }}"
  rds_security_group_ids: "{{ hostvars[inventory_hostname][context + '_data'] }}"
  rds_master_username: "{{ lookup('env', 'RDS_USER') }}"
  rds_master_password: "{{ lookup('env', 'RDS_PASSWORD') }}"
  rds_db_engine: "postgres"
  rds_db_engine_version: "9.5.4"
```

For a list of valid `rds_db_engine` and `rds_db_engine_version` values, run `aws rds describe-db-engine-versions`.

The result of the `rds` resource will be stored in `manage_rds_{{ rds_name | replace('-', '_') }}": "{{result}}`. A `rds_name` of `foo-bar` would be set as `manage_rds_foo_bar`.
