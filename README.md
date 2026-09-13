# Mathematics Foundational Corpus

A dependency-ordered corpus of the foundational and landmark theorems that form the structural backbone of modern mathematics.

The goal is not to produce an encyclopedia. It is to build a **conceptual map of mathematics** in which each major theorem is explained at a level that answers:

1. **What does it actually say?**
2. **Why was it needed?**
3. **What conceptual problem does it solve?**
4. **Why is it a big deal?**
5. **What earlier mathematics does it depend on?**
6. **What later mathematics depends on it?**
7. **What is the core proof idea?**
8. **What should remain in one's head after the details are forgotten?**

The intended style is mathematically serious but explanatory: rigorous enough for a mathematically mature reader, but focused on structural significance rather than textbook completeness.

## Organization

The corpus is ordered primarily by **logical and conceptual dependency**, not by historical date.

Each theorem has its own Markdown chapter using a common template. The global dependency map lives in [`ROADMAP.md`](ROADMAP.md).

Initial major layers:

1. Foundations, logic, sets, and proof
2. Arithmetic and elementary algebra
3. Linear algebra and abstract algebra
4. Real analysis and measure
5. Topology
6. Complex analysis
7. Differential geometry and manifolds
8. Functional analysis
9. Probability and stochastic analysis
10. Algebraic topology
11. Commutative algebra and algebraic geometry
12. Lie theory and representation theory
13. Number theory and arithmetic geometry
14. PDE, dynamical systems, and global analysis
15. Category theory and homological algebra
16. Great synthesis theorems
17. Computability, information, and complexity

## Chapter format

Each chapter should contain, as appropriate:

- **The theorem** — precise statement, with variants if needed
- **Before the theorem** — what problem existed beforehand
- **The central idea** — intuitive mathematical content
- **Why it matters** — structural significance
- **Canonical examples**
- **Proof architecture** — the decisive ideas, not line-by-line bookkeeping
- **Consequences**
- **Dependencies**
- **What it unlocks**
- **What to remember**
- **Further directions**

## Math formatting convention

All Markdown in this repository uses GitHub's supported mathematical notation:

- Inline mathematics: `$ ... $`
- Display mathematics: `$$ ... $$`

Do not use `\\(...\\)` or `\\[...\\]` delimiters in repository Markdown, since those are not rendered consistently by GitHub clients, especially on mobile.

## Status

This repository is intended to grow incrementally. The first exemplar chapter is Hilbert's Nullstellensatz, since it illustrates the desired depth and explanatory style especially well.
