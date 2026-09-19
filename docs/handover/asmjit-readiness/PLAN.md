# AsmJit Readiness Plan — wow_cdn_exporter_cli_2026

Status: PREPARED_ONLY
Branch: `prep/asmjit-readiness-2026-09-19`
Decision: DO NOT INTEGRATE under the current/exporter scope.

The repository is intended for WoW CDN/export CLI work. Runtime native machine-code generation does not address CDN transfer, archive/database parsing, decompression, filesystem export, or serialization bottlenecks.

## Preferred optimization path
1. Establish real exporter implementation and profiling.
2. Measure CDN/network latency and throughput.
3. Measure decompression/parsing and file-output costs.
4. Optimize streaming, batching, concurrency, caching, and static native libraries where needed.
5. Revisit AsmJit only if a future explicit runtime compiler/code-generation subsystem appears.

## Constraints
No AsmJit dependency, native JIT code, PR, merge, or production behavior change is authorized by this branch.
