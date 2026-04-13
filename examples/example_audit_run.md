\# Example Audit Run



\## Overview



Illustrates a complete audit process.



\---



\## Result



PASS:



\- boundary complete  

\- reproducible  



\---



\## Failure Example



If:



```text

artifact(R₁) ≠ artifact(R₂)

AND boundary(R₁) == boundary(R₂)

```



Then:



```text

boundary incomplete

```



\---



\## Summary



Valid runs must be reproducible under identical boundaries.

