\# Audit CLI Specification



\## Command



```bash

datadiddler-audit run <RUN\_PATH> \[--compare <RUN\_PATH\_2>]

```



\---



\## Exit Codes



0 → PASS  

1 → execution\_failure  

2 → missing\_artifact  

3 → schema\_violation  

4 → boundary\_incomplete  

5 → reproducibility\_failure  



\---



\## Output



PASS:



```json

{

&#x20; "status": "PASS",

&#x20; "boundary\_complete": true,

&#x20; "reproducible": true

}

```



FAIL:



```json

{

&#x20; "status": "FAIL",

&#x20; "failure\_type": "boundary\_incomplete"

}

```



\---



\## Summary



CLI verifies:



\- structure  

\- boundary completeness  

\- reproducibility  

