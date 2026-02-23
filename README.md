# Apex Language

Apex is an open-source, English-extension, object-oriented programming language that compiles to LLVM and WebAssembly.

It is designed to bridge human thought and machine execution by combining:

- Natural English-like syntax
- Native AI integration (`think` blocks)
- First-class Tensor support
- Declarative English UI
- High-performance LLVM compilation

---

## Vision

Apex aims to make software development more expressive without sacrificing performance.

Instead of forcing developers to think in symbols, Apex allows structured English constructs like:

```apex
to start the engine begin
    let matrix is a Tensor of [10,10]
end
```

Apex compiles to:

- Native machine code (via LLVM)
- WebAssembly (for browser and edge deployment)

---

## Core Features (v1)

### 1. English-Based Syntax

Readable, structured, and compiler-friendly:

```apex
to calculate sum with a and b begin
    return a plus b
end
```

---

### 2. AI-Powered `think` Blocks

Apex integrates with Large Language Models during compilation.

```apex
think "Detect objects in the image and return a JSON list"
```

During compilation:

1. The compiler extracts the string.
2. Sends it to an LLM (GPT/Claude).
3. Receives optimized C++.
4. Injects the generated code.
5. Continues LLVM compilation.

This allows human-intent-driven code generation while preserving performance.

---

### 3. Tensor as a Primitive Type

Built-in support for data science and machine learning:

```apex
let matrix is a Tensor of [10, 10]
```

No external framework required.

---

### 4. Declarative English UI

```apex
create a Button with text "Click Me" and color "Blue"
```

Automatically lowers to:

- Web (DOM / WASM)
- Mobile (future adapters)
- Desktop

---

### 5. Unified Type System

All types inherit from `Everything`:

- Text
- Number
- Boolean
- Tensor
- List
- Map
- UIComponent
- NeuralNetwork

---

## Architecture Overview

```
.apex Source
      ↓
Lexer (Rust)
      ↓
Parser
      ↓
AST
      ↓
AI Lowering Engine (think blocks)
      ↓
C++ / LLVM IR
      ↓
LLVM Backend
      ↓
Native Binary / WebAssembly
```

---

## Project Structure (Planned)

```
apex-language/
│
├── compiler/
│   ├── lexer/
│   ├── parser/
│   ├── ast/
│   ├── semantic/
│   ├── ai-lowering/
│   └── llvm-backend/
│
├── runtime/
│
├── stdlib/
│
├── examples/
│
└── docs/
```

---

## Installation (Future)

Coming soon.

The compiler will be written primarily in Rust and will require LLVM installed locally.

---

## Example

```apex
import Web.Server
import AI.Vision

to start the engine begin
    let model is a NeuralNetwork from "path/to/model"
    
    create a WebServer on port 8080 begin
        on request "POST /analyze" begin
            let image is request.body.image
            think "Use the vision model to detect objects and return JSON"
        end
    end
end

start the engine
```

---

## Open Source

Apex is open source.

License: MIT (recommended)

You are free to:

- Use
- Modify
- Fork
- Contribute
- Distribute

Contributions are welcome.

---

## Roadmap

### v1
- Grammar specification
- Lexer
- Parser
- AI lowering engine
- LLVM IR generation
- WASM support

### v2
- Standard library
- Package manager
- Concurrency model
- JIT mode
- Language server (LSP)

---

## Why Apex?

As AI reduces the friction of writing code, programming languages must evolve.

Apex is built for:

- AI-native development
- High-performance systems
- Readable code
- Modern web and ML workloads

---

## Contributing

1. Fork the repository
2. Create a feature branch
3. Submit a PR

Please follow the code style guidelines once published.

---

## Status

Early development — specification phase.

---

## Author

Created as part of the Apex universal language initiative.

---

## Future

Apex is designed to become:

- A systems language
- A web language
- A data science language
- An AI-native language

All in one.

---

Open source. Built for the next generation.
