\# Audit Procedure



\## Overview



Step-by-step verification of a DataDiddler run.



\---



\## Steps



1\. Load run record  

2\. Verify execution (rc, stages)  

3\. Verify artifact presence  

4\. Validate structure (NDJSON)  

5\. Validate schema  

6\. Verify canonicalization  

7\. Validate boundary declaration  

8\. Verify observability  

9\. Compare runs (optional)  



\---



\## Output



PASS → boundary complete  

FAIL → boundary incomplete or structural error  



\---



\## Summary



The audit confirms:



\- structure  

\- declared boundary  

\- reproducibility  

