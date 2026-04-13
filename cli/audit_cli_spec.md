# Audit CLI Specification

## Command

```bash
datadiddler-audit run <RUN_PATH> [--compare <RUN_PATH_2>]
```

---

## Exit Codes

0 → PASS  
1 → execution_failure  
2 → missing_artifact  
3 → schema_violation  
4 → boundary_incomplete  
5 → reproducibility_failure  

---

## Output

PASS:

```json
{
  "status": "PASS",
  "boundary_complete": true,
  "reproducible": true
}
```

FAIL:

```json
{
  "status": "FAIL",
  "failure_type": "boundary_incomplete"
}
```

---

## Summary

CLI verifies:

- structure  
- boundary completeness  
- reproducibility  
