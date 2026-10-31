# Views

The 3 required database views (`v_daily_compliance_summary`,
`v_auditor_work_queue`, `v_rule_effectiveness`) are defined in
[`../00_schema_ddl.sql`](../00_schema_ddl.sql), alongside the tables
they depend on, so the whole schema builds from a single script as the
brief requires (Section 4.1: "a single schema creation script that
builds every object from an empty database").

- `v_daily_compliance_summary` backs `SQL-01`
- `v_auditor_work_queue` backs `SQL-05`
- `v_rule_effectiveness` backs `SQL-06`

`dashboard/app.py` queries these views directly.
