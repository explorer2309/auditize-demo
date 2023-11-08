# Audit

- standard fk not_null
- functional_area fk not_null
- audit_type enum internal/external not_null
- status enum in_progress/completed/cancelled not_null
- start_date datetime not_null
- end_date datetime not_null
- scope text not_null
- internal_auditor fk
- external_auditor text
- auditee fk

# Audit_Execution

- audit_id fk not_null
-

# Non_conformance

- functional_area fk not_null
- origin enum (customer, supplier, internal_audit) not_null
- title string not_null
- description text not_null
- classification enum (major, minor) not_null
- objective_evidence text
- status enum (active, completed, abandoned) not_null
- target_completion_period int not_null
- target_completion_date date not_null
- site string null

## CAR

- root_cause text
- correction text
- corrective_action text
- verification_of_effectiveness text
- method_of_verification text
- target_completion_date date not_null
  - auditors_comments text
