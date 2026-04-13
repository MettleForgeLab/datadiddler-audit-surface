
# Boundary Completeness Specification



## Definition



A boundary is considered \*\*complete\*\* when all variables capable of influencing canonical artifact bytes are explicitly declared and observable.



```text

boundary\_complete := ∀ v, (influences\_output(v) → declared(v) ∧ observable(v))

```



---



## Boundary Components



A valid boundary MUST include:



### 1. Input Data

- file paths explicitly listed  

- file hashes recorded  

- encoding declared  



### 2. Configuration State

- full config snapshot  

- no implicit defaults  

- versioned or hashed  



### 3. Tool Code

- exact version or commit hash  

- immutable reference  



### 4. Tool Mapping

- tools.json explicitly declared  

- stage → tool mapping fixed  



### 5. Execution Order

- explicit stage order  

- no runtime reordering  



### 6. Runtime Environment

- language version  

- OS/platform  

- dependency versions  



### 7. Filesystem Behavior

- path resolution rules  

- ordering behavior controlled  



### 8. Canonicalization Rules

- sorting rules  

- serialization format  

- encoding  

- float precision  



### 9. Observability

- run record exists  

- artifacts addressable  

- hashes retrievable  



---



## Completeness Test



```text

boundary(R₁) == boundary(R₂)

→ artifact(R₁) == artifact(R₂)

```



---



## Incompleteness Detection



```text

artifact(R₁) ≠ artifact(R₂)

AND boundary(R₁) == boundary(R₂)

→ hidden variable exists

```



---



## Summary



A boundary is complete when:



```text

no unobserved variable can affect artifact bytes

```
