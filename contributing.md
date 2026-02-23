# Contributing to Apex Language

Thank you for your interest in contributing to Apex.

Apex is an open-source English-extension programming language designed to compile to LLVM and WebAssembly with native AI integration. Contributions of all sizes are welcome.

---

## Philosophy

Apex prioritizes:

- Clarity over cleverness
- Structured English syntax
- Compiler correctness
- Performance via LLVM
- Long-term maintainability

Before submitting changes, ensure your contribution aligns with these principles.

---

## Ways to Contribute

You can contribute by:

- Improving the compiler (lexer, parser, AST, backend)
- Expanding the grammar
- Writing tests
- Improving documentation
- Adding examples
- Reporting bugs
- Proposing language enhancements

---

## Development Setup (Planned)

The compiler will primarily use:

- Rust (core compiler)
- LLVM
- Python (AI lowering engine prototype)

Setup instructions will be finalized as v1 stabilizes.

---

## Contribution Workflow

1. Fork the repository
2. Create a new branch:

   ```
   git checkout -b feature/your-feature-name
   ```

3. Commit changes with descriptive messages:

   ```
   git commit -m "Add parser support for for-each loop"
   ```

4. Push to your fork:

   ```
   git push origin feature/your-feature-name
   ```

5. Open a Pull Request

---

## Pull Request Guidelines

PRs should:

- Be focused on a single improvement
- Include clear descriptions
- Include test cases where applicable
- Follow existing formatting conventions

Large architectural changes should be discussed in an issue before implementation.

---

## Code Style Guidelines

### Rust Compiler Code
- Use idiomatic Rust
- Avoid unnecessary unsafe blocks
- Prefer clarity over micro-optimization

### Apex Examples
- Follow English-structured syntax
- Use clear naming
- Avoid abbreviations

---

## Issues

When reporting bugs, include:

- Apex source snippet
- Expected behavior
- Actual behavior
- Environment details

---

## Roadmap Alignment

Before implementing major features, check:

- Open roadmap
- Existing discussions
- v1 scope boundaries

---

## Contributor Conduct

All contributors must follow the Code of Conduct.

---

Thank you for helping build Apex.
