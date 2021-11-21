
# 115 - [Unspecific compiler version pragma](./Unspecific%20compiler%20version%20pragma.md)

Unspecific compiler version pragma For most source-units the compiler version pragma is very unspecific `^0.6.0`. While this often makes sense for libraries to allow them to be included with multiple different versions of an application, it may be a security risk for the actual application implementation itself. A known vulnerable compiler version may accidentally be selected or security tools might fall-back to an older compiler version ending up actually checking a different evm compilation that is ultimately deployed on the blockchain.


1. Recommendation: Avoid floating pragmas. We highly recommend pinning a concrete compiler version (latest without security issues) in at least the top-level "deployed" contracts to make it unambiguous which compiler version is being used. Rule of thumb: a flattened source-unit should have at least one non-floating concrete solidity compiler version pragma.
2. [ConsenSys's Audit of 1inch Liquidity Protocol](https://consensys.net/diligence/audits/2020/12/1inch-liquidity-protocol/#unspecific-compiler-version-pragma)


___
## Slide Screenshot
![115.png](../../images/8.%20Audit%20Findings%20201/115.png)
___
## Slide Text
- 
___
## References
- Youtube Reference
___
## Tags