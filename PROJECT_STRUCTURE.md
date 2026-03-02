# Synen Language — Project Structure

This document defines the initial repository layout for Synen v1.

The structure is designed to support:

- Compiler modularity
- Clear separation of concerns
- Future scalability
- Open-source collaboration

---

## Root Directory

```
Synen-language/
│
├── README.md
├── LICENSE
├── CONTRIBUTING.md
├── CODE_OF_CONDUCT.md
├── PROJECT_STRUCTURE.md
│
├── compiler/
├── runtime/
├── stdlib/
├── examples/
└── docs/
```

---

## Compiler

The compiler is written primarily in Rust.

```
compiler/
│
├── Cargo.toml
│
├── src/
│   ├── main.rs
│   │
│   ├── lexer/
│   │   ├── mod.rs
│   │   └── token.rs
│   │
│   ├── parser/
│   │   ├── mod.rs
│   │   └── grammar.rs
│   │
│   ├── ast/
│   │   └── nodes.rs
│   │
│   ├── semantic/
│   │   └── analyzer.rs
│   │
│   ├── ai_lowering/
│   │   └── engine.rs
│   │
│   └── llvm_backend/
│       └── generator.rs
```

### Purpose of Each Module

**lexer/**
- Converts source code into tokens
- Maps English keywords into compiler symbols

**parser/**
- Converts tokens into AST nodes
- Enforces grammar rules

**ast/**
- Defines abstract syntax tree node structures

**semantic/**
- Type checking
- Scope validation
- Symbol resolution

**ai_lowering/**
- Extracts `think` blocks
- Sends instructions to LLM
- Injects generated C++/IR

**llvm_backend/**
- Converts AST to LLVM IR
- Produces native binary or WebAssembly

---

## Runtime

```
runtime/
└── core/
    └── everything.rs
```

Contains:

- Base `Everything` class
- Core type system definitions
- Runtime utilities
- Memory model (future)

---

## Standard Library

```
stdlib/
├── io.Synen
├── math.Synen
└── web.Synen
```

Planned modules:

- IO operations
- Mathematical utilities
- Web abstractions
- Data structures
- AI utilities

---

## Examples

```
examples/
├── hello_world.Synen
├── tensor_example.Synen
└── web_server.Synen
```

Purpose:

- Demonstrate syntax
- Provide test coverage
- Show real use cases

---

## Documentation

```
docs/
├── language_specification.Synen
└── architecture.md
```

Contains:

- Full grammar specification
- Compiler architecture overview
- Roadmap documentation

---

## Future Expansion (Reserved Directories)

These may be added in later versions:

```
lsp/              # Language Server Protocol
package_manager/  # Synen package manager
benchmarks/       # Performance benchmarks
tests/            # Compiler and runtime tests
```

---

## Design Philosophy Behind Structure

The repository layout enforces:

- Clear compiler phase separation
- Replaceable AI backend
- Modular LLVM backend
- Scalable growth for v2+

Each folder represents a logical compiler stage.

---

## Status

This structure represents Synen v1 foundation phase.

Additional components will be added as the compiler matures.

---

Synen is open source and evolving.
