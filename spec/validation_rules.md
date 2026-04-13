
# Validation Rules

## Overview

Validation determines whether:

- structure is intact  
- boundary is declared  
- output is reproducible  

---

## Execution Validation

```text
rc == 0 → success
rc != 0 → failure
````

---

## Artifact Presence

```text
all required outputs must exist
empty outputs are valid
```

---

## Schema Validation

* valid NDJSON
* parseable
* correct structure

---

## Canonicalization

* deterministic ordering
* consistent encoding
* stable serialization

---

## Boundary Validation

* inputs declared
* tools declared
* config declared
* environment declared

---

## Reproducibility

```text
same boundary → same artifact
```

---

## Outcome

PASS:

* boundary_complete == true
* reproducible == true

FAIL:

* execution_failure
* missing_artifact
* schema_violation
* boundary_incomplete
* reproducibility_failure



