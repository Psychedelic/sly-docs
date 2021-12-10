---
date: "1"
---
# SLY - WASM Optimizer

## SLY - WASM Optimizer

Just like our Candid utilities, we also figured users usually need `ic-cdk-optimizer` when
developing canisters for the Internet Computer, so we bundled that functionality inside SLY. 

This optimizer tool will help reduce the file size of a compiled WASM module and outputs the optimized version.

Simply run the following command and target your desired WASM:
```
sly wasm optimize -o file-opt.wasm input.wasm
```

