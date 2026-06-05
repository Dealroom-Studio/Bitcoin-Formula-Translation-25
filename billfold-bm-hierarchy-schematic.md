# Billfold Technologies — Business Machine Hierarchy Schematic
## FIG. 1 — Patent Reference Document

### Overview
This reference defines the Billfold Technologies Business Machine hierarchy using Numbermaiden CIA component/package mapping with CBOE/XBRL conventions. The architecture is partitioned into four tiers: EIP-1155 token control, permission technologies, silicon wraps packaging, and audit/registry logging. Canonical labels use patent-legible identifiers with C# SDK aligned names such as `BusinessMachineNode`, `ParticleNode`, `RendererNode`, `IExecutable`, `IParticleCompiler`, and `IBusinessMachineCompiler`; enum labels follow PascalCase (`Fungible`, `NonFungible`, `Owner`, `Registrar`, `Auditor`, `Client`) and XML element naming follows established Siloscript conventions.

### Architectural Tiers
| Tier | Name | Key Standard | Components |
|---|---|---|---|
| Tier 1 | Token Layer | EIP-1155 multi-token | `bm-70`, tokenized business machine package anchor |
| Tier 2 | Permission Technologies Layer | CBOE/XBRL permission conventions | `re-70`, `as-70`, `no-70`, `of-70` |
| Tier 3 | Silicon Wraps Packaging Layer | silicon wraps package class wrapping | `s_70`, `e_70`, `l_70`, `p_70`, `a_70`, `t_70`, `ss_70` |
| Tier 4 | Audit & Registry Layer | XBRL-aligned audit and registry controls | `sm-l/shel=l3` audit log, registry references |

### Component Hierarchy (Install Relationships)
```text
electroplate
  └── bm-70  [Business Machine]
        ├── re-70  [Renderer]
        │     └── ds-70  [Data Serial]
        │     └── of-70  [Orderfiche]
        ├── as-70  [Asset]
        ├── no-70  [Node]
        │     ├── ds-70  [Data Serial]
        │     ├── ne-70  [Network]
        │     └── cp-70  [Particle Compiler]
        ├── of-70  [Orderfiche]
        └── cb-70  [BM Compiler]
```

### Compiler Pipelines
#### cp-70 Particle Compiler
| Stage | Identifier | Data Core Source | Output |
|---|---|---|---|
| 1 | `cp-sr1` | Electroplate-Store-v1 / syntax-management | Source read stream |
| 2 | `cp-lx2` | Electroplate-Store-v1 / syntax-management | Lexical tokens |
| 3 | `cp-pa3` | Electroplate-Store-v1 / syntax-management | Parsed structures |
| 4 | `cp-sb4` | Electroplate-Store-v1 / syntax-management | Symbol-bound graph |
| 5 | `cp-op5` | Electroplate-Store-v1 / syntax-management | Optimized package model |
| 6 | `cp-em6` | Electroplate-Store-v1 / syntax-management | Emitted particle payload |

#### cb-70 Business Machine Compiler
| Stage | Identifier | Data Core Source | Output |
|---|---|---|---|
| 1 | `cb-sr1` | Electroplate-Store-v1 / syntax-management | Source read stream |
| 2 | `cb-lx2` | Electroplate-Store-v1 / syntax-management | Lexical tokens |
| 3 | `cb-pa3` | Electroplate-Store-v1 / syntax-management | Parsed business machine graph |
| 4 | `cb-sb4` | Electroplate-Store-v1 / syntax-management | Symbol-bound machine model |
| 5 | `cb-le5` | Electroplate-Store-v1 / syntax-management | Link and execution package |
| 6 | `cb-re6` | Electroplate-Store-v1 / syntax-management | Runtime-ready machine artifact |

### Shell Mechanics Reference
| Identifier | Shell ID | Name | Function |
|---|---|---|---|
| `sm-a` | `shel=a1` | Actions | Declares executable action semantics |
| `sm-e` | `shel=e2` | Executables | Declares runnable executable units (`IExecutable`) |
| `sm-l` | `shel=l3` | Log | Captures immutable audit log records |
| `sm-p` | `shel=p4` | Parameter In | Defines ingress parameters |
| `sm-s` | `shel=s5` | Sheet | Defines sheet payload structures |
| `sm-s2` | `shel=s6` | Snippet | Defines snippet payload segments |
| `sm-t` | `shel=t7` | Tag | Defines taxonomy and tags |

### Package Classes Reference
| Class | Identifier | Silicon Wraps | Description |
|---|---|---|---|
| Snippet | `s_70` | Wrapped | Snippet package unit |
| Extension | `e_70` | Wrapped | Extension package unit |
| Library | `l_70` | Wrapped | Library package unit |
| Plugin | `p_70` | Wrapped | Plugin package unit |
| App | `a_70` | Wrapped | Application package unit |
| Trade Engine | `t_70` | Wrapped | Trade engine package unit |
| Stylesheet | `ss_70` | Wrapped | Stylesheet package unit |

### Data Flow Summary
1. `Syntax-Management Data Core` feeds the `cp-70` particle compiler pipeline.
2. `Syntax-Management Data Core` feeds the `cb-70` business machine compiler pipeline.
3. `cp-70` compiler outputs feed `no-70` and `bm-70` integration points.
4. `cb-70` compiler outputs feed `bm-70` and `re-70` integration points.
5. `of-70` emits log-forward records into `Audit (shel=l3 log)`.

### Patent Claim Reference Notes
1. A four-tier machine package hierarchy is anchored by `bm-70` at an EIP-1155 tokenized root with downstream package install dependencies.
2. Dual compiler chains (`cp-70` and `cb-70`) are sourced from a shared syntax-management data core while maintaining separate stage identifiers.
3. Shell mechanics (`sm-a` through `sm-t`) define deterministic execution, parameter ingress, and immutable audit logging controls.
4. Silicon wraps uniformly encapsulate all package classes (`s_70` through `ss_70`) to standardize package deployment semantics.
5. CBOE/XBRL-aligned Numbermaiden CIA mappings provide stable identifier semantics across component, package, and registry layers.

### References
1. Electroplate-Store-v1 syntax-management commit `58f4c935`.
2. `businessparticledocument.xml` SHA256 registry.
3. CBOE Technical Specifications.
4. XBRL US Data Quality Rules.
5. Numbermaiden CIA Component &amp; Package Mapping conventions.
