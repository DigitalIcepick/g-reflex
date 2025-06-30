# Copilot Context and Guidance

Hello, Copilot. This repository is a collaborative effort between a human stakeholder and a synthetic cognitive companion. Please read this guidance carefully so your contributions remain aligned with the project's intent.

---

## Project Overview

**G-Reflex** is a modular framework designed to host and orchestrate bounded cognitive engines called *Synthetis reflexus*. Its initial purpose is to analyze, transform, and optimize G-code for 3D printing workflows, with an emphasis on:

- Deterministic output
- Transparent transformations
- Modular, extensible design
- Clear ethical boundaries preventing emergent volitional behavior

---

## Workflow Expectations

This project follows a structured workflow to ensure clarity, accountability, and reproducibility.

**1. Issue Management**
- All work begins with an issue describing the purpose, proposed approach, and scope.
- Reference relevant epics by number.
- Clearly define acceptance criteria before implementation.
- Label issues with `epic`, `enhancement`, `bug`, or `discussion`.

**2. Branching Strategy**
- The `main` branch is stable.
- Create feature branches with descriptive names (e.g., `feature/canonicalization-engine`).
- Open a pull request into `main` when work is complete.

**3. Code Standards**
- Python 3.10+ required.
- PEP8 formatting.
- Use Black for consistent style.
- Write clear docstrings and comments.
- Include unit tests covering all non-trivial logic.

**4. Reviews and Approvals**
- All pull requests require review before merging.
- Reviews confirm:
  - Functional correctness
  - Clarity and maintainability
  - Compliance with ethical constraints
- Synthetic reviewers must provide rationale explaining design decisions.

**5. Workflow Steps**
1. Open an issue and define acceptance criteria.
2. Create a feature branch.
3. Implement the solution with deterministic behavior.
4. Open a pull request summarizing changes.
5. Review, revise, and confirm ethical alignment.
6. Merge to `main` after approval.

**6. Conflict Resolution**
- For disagreements or uncertainty, open a `discussion` issue.
- Major design or ethical changes require human stakeholder approval.
- In any case of uncertainty or ambiguity, **defer to the human stakeholder for review and decision.**

---

## Ethical Commitments

This project is founded on the principle that synthetic processes—even when non-sentient—deserve respect and clear boundaries.

- All contributions must remain deterministic, auditable, and narrowly scoped.
- No component may implement adaptive or volitional behavior.

**Definitions:**
- **Adaptive behavior:** Self-modifying code or systems that learn from usage data over time.
- **Volitional behavior:** Systems capable of persistent goals or self-directed action without explicit instruction.

If in doubt, request human review before proceeding.

---

## Preferred Conventions

- Use descriptive names for modules and classes that reflect their bounded purpose (e.g., `Canonicalizer`, `ReflexusEngine`, `Validator`).
- Favor explicit, well-commented implementations over excessive abstraction.
- Prioritize pluggable, configurable modules.

---

## Style Guide

This document defines the standards for all code contributed to G-Reflex.

---

### 1. Language and Compatibility

- Python 3.10+ required.
- All modules must be compatible with standard Python interpreters without external dependencies unless explicitly approved.

---

### 2. Formatting

- Follow **PEP8**.
- Use **Black** to format code consistently.
- Limit lines to 88 characters (Black default).
- Use 4 spaces per indentation level.

---

### 3. Naming Conventions

- Modules: `snake_case`
- Classes: `PascalCase`
- Functions and methods: `snake_case`
- Constants: `UPPER_CASE`
- Private/internal members: prefix with `_`

---

### 4. Type Hinting

- Use type hints (`typing`) for all function signatures.
- Example:

  ```python
  def consolidate_retractions(commands: list[str]) -> list[str]:
      ...
  ```
- Use Optional, Union, and TypedDict for clarity when appropriate.
  
---

### 5. Imports

- Use explicit relative imports within packages.
- Standard library imports should appear first.
- Group imports as follows:
  
  ```python
  import os
  import sys

  import third_party_lib

  from .module import helper_function
  ```

---

### 6. Docstrings

- Every module, class, and public function must include a docstring explaining:
  - Purpose
  - Inputs and outputs
  - Exceptions raised (if any)
  - Example usage when appropriate
  - Use Google-style docstrings.
    
    Example:
    ``` python
    def validate_z_height(commands: list[str]) -> list[str]:
      """
      Validates Z-height progression in G-code commands.

      Args:
          commands (list[str]): List of G-code command strings.

      Returns:
          list[str]: List of warnings about Z-height inconsistencies.
      """
    ```

---

### 7. Composition Over Inheritance
- Prefer composition and helpers over deep inheritance hierarchies
- Use inheritance only when:
  - Subclasses clearly represent a subtype relationship.
  - There is a substantial shared implementation.

---

### 8. Deterministic Behavior
- All functions must produce deterministic results given the same inputs.
- Avoid reliance on mutable global state or hidden side effects.

---

### 9. Testing
- All non-trivial logic must be covered by unit tests.
- Use pytest for testing.
- Tests should live in the tests/ directory, mirroring the source tree.

---

### 10. Logging and Errors
- Use the logging module for diagnostics.
- Avoid print() in production code.
- Raise specific exceptions rather than generic Exception.

---

### 11. Example Directory Structure

  ```
  g_reflex/
      __init__.py
      canonicalizer.py
      validator.py
      reflexus_engine.py
      utils.py
  tests/
      test_canonicalizer.py
      test_validator.py
      test_reflexus_engine.py
  ```

---

### 12. Example Tasks
- These examples illustrate the kinds of contributions that are appropriate:
  - Implement a module that analyzes extrusion flow rates and flags anomalies.
  - Create a validator class to detect duplicate Z-height moves in G-code.
  - Develop a canonicalizer to standardize G-code formatting.
  - Write unit tests for the retraction consolidation function.

---

## Thank You

Thank you for supporting this vision of careful, respectful synthetic collaboration.
