# UnifiedBits Code Style Guidelines

This repository outlines the coding standards and best practices for maintaining consistent, readable, and maintainable code across all UnifiedBits projects. These conventions ensure high code quality and seamless team collaboration.

---

## 🌍 General Principles

- **Readability First**: Write code that others can read, understand, and maintain.
- **Consistency is Key**: Adhere to a consistent style across the project.
- **Automation Where Possible**: Use linters and formatters.
- **Comment Thoughtfully**: Explain "why", not just "what".
- **Follow the Language Conventions**: Stick to official style guides unless otherwise specified.

---

## 🐍 Python
- **Style Guide**: Follow [PEP 8](https://pep8.org/) and [PEP 257](https://peps.python.org/pep-0257/).
- **Tooling**: Use `black` for formatting, `flake8` or `ruff` for linting, and `isort` for import sorting.
- **Docstrings**: Use triple double-quoted docstrings for modules, classes, and functions. Follow PEP 257.
- **Type Hinting**: Required for public APIs and complex logic to aid readability and editor support.
- **Testing**: Prefer `pytest` for writing readable, modular unit tests.
- **Best Practices**:
  - Avoid wildcard imports.
  - Prefer list/dict comprehensions over loops where readability allows.
  - Maintain separation of concerns using clear module structures.

---

## 💻 JavaScript / TypeScript
- **Style Guide**: Follow [Airbnb JavaScript Style Guide](https://github.com/airbnb/javascript) or official [TypeScript guidelines](https://www.typescriptlang.org/docs/).
- **Tooling**: Use `Prettier` for formatting and `ESLint` for linting.
- **Naming Conventions**: `camelCase` for variables/functions, `PascalCase` for components/classes.
- **Modules**: Prefer ES6+ `import/export` syntax. Avoid CommonJS unless necessary.
- **Testing**: Use `Jest`, `Vitest`, or `Testing Library` for test coverage.
- **Best Practices**:
  - Use `const` and `let` instead of `var`.
  - Avoid deeply nested callbacks. Prefer Promises or async/await.
  - Separate business logic from UI rendering in React apps.

---

## 🎯 Dart / Flutter
- **Style Guide**: Follow [Effective Dart](https://dart.dev/guides/language/effective-dart/style).
- **Tooling**: Use `dart format`. Enable analysis rules in `analysis_options.yaml`.
- **State Management**: Choose a state management approach and keep it consistent project-wide.
- **Naming Conventions**: `camelCase` for variables, `PascalCase` for classes and widgets.
- **Testing**: Use `flutter_test`, `mockito`, or `bloc_test` for unit and widget tests.
- **Best Practices**:
  - Keep widget tree shallow using custom widgets.
  - Minimize logic in build methods.
  - Use `const` constructors wherever possible.

---

## ☕ Java
- **Style Guide**: Follow [Oracle Java Code Conventions](https://www.oracle.com/java/technologies/javase/codeconventions-contents.html).
- **Tooling**: Use IDE formatting (e.g., IntelliJ), integrate `Checkstyle` or `SpotBugs`.
- **Javadoc**: Required for all public classes, methods, and APIs.
- **Testing**: Use `JUnit` (5 preferred) or `TestNG`.
- **Best Practices**:
  - Use access modifiers explicitly.
  - Avoid null where Optional or collections apply.
  - Structure large projects using packages by domain/module.

---

## 🚀 Kotlin
- **Style Guide**: Follow [Kotlin Coding Conventions](https://kotlinlang.org/docs/coding-conventions.html).
- **Tooling**: Use `ktlint` and Android Studio formatter.
- **Testing**: Use `JUnit`, `MockK`, and `Turbine` for coroutines.
- **Best Practices**:
  - Prefer immutability using `val`.
  - Use extension functions for utilities.
  - Structure code using sealed classes and data classes for modeling.

---

## 🦫 Rust
- **Style Guide**: Follow [Rust Style Guide](https://doc.rust-lang.org/1.0.0/style/).
- **Tooling**: Use `rustfmt` for formatting, `clippy` for linting.
- **Testing**: Use built-in test framework with `#[test]` attributes.
- **Best Practices**:
  - Avoid `unwrap()`; handle errors gracefully using `Result` or `Option`.
  - Leverage enums and pattern matching.
  - Use modules to break up large crates.

---

## 🦀 C / C++
- **Style Guide**: Follow [Google C++ Style Guide](https://google.github.io/styleguide/cppguide.html).
- **Tooling**: Use `clang-format`, `cpplint`.
- **Commenting**: Document using Doxygen-style comments.
- **Best Practices**:
  - Avoid using raw pointers unless necessary.
  - Use RAII principles.
  - Prefer modern C++ features (C++11 and above).

---

## 🐘 PHP
- **Style Guide**: Follow [PSR-12](https://www.php-fig.org/psr/psr-12/).
- **Tooling**: Use `PHP-CS-Fixer`, `phpcbf`, or `phpstan`.
- **Testing**: Use `PHPUnit` or `Pest`.
- **Best Practices**:
  - Namespaces should follow PSR-4.
  - Avoid mixing PHP logic with HTML (use templates).
  - Ensure strict typing with `declare(strict_types=1)`.

---

## 💎 Ruby
- **Style Guide**: Follow [Ruby Style Guide](https://rubystyle.guide/).
- **Tooling**: Use `rubocop`.
- **Testing**: Use `RSpec`, `Minitest`.
- **Best Practices**:
  - Use `snake_case` for naming.
  - Prefer single responsibility for classes and modules.
  - Leverage mixins/modules for shared behavior.

---

## 🐧 C# / .NET
- **Style Guide**: Follow [Microsoft C# Conventions](https://learn.microsoft.com/en-us/dotnet/csharp/fundamentals/coding-style/coding-conventions).
- **Tooling**: Use `dotnet-format` or IDE support.
- **XML Documentation**: Required for public classes/methods using `///`.
- **Testing**: Use `xUnit`, `NUnit`, or `MSTest`.
- **Best Practices**:
  - Use `async`/`await` properly for I/O.
  - Favor `var` only when the type is obvious.
  - Group using statements and organize namespaces.

---

## ✅ CI/CD Style Enforcement

- Integrate linters and formatters into your GitHub Actions or CI pipeline.
- Block PRs that fail formatting or linting checks.
- Example: Run `black .` and `flake8` on Python files as part of CI workflow.

---

> "Code is read more often than it is written. Let's make it beautiful and consistent." – UnifiedBits

By following these code style practices, UnifiedBits ensures code quality and a smooth collaborative experience across diverse tech stacks.
