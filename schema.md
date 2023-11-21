# Audit

- standard FK not_null
- functional_area FK not_null
- audit_type enum internal/external not_null
- status enum in_progress/completed/cancelled not_null
- start_date datetime not_null
- end_date datetime not_null
- scope text not_null
- internal_auditor FK
- external_auditor text
- auditee FK

# Audit_Execution

- audit_id FK not_null
-

## Execution_line

- checkpoint
- nc_comment text
- can_improve text
- doing_well text
- linked_nc FK

# Non_conformance

- functional_area FK not_null
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
