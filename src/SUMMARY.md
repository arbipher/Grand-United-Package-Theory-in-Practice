# Grand Unified Package Theory in Practice

## 🚧 **Under Construction** 🚧

## Overview

Package management issues are ubiquitous in software development and usage. Ecosystem tools around programming languages, such as package managers, build systems, compilers, and interpreters, play a critical role in modern software engineering. However, these tools are often ad hoc, brittle, and error-prone, leading to significant deployment and maintenance challenges.

Package management of one programming language often involves complex interactions with tools for other languages and systems. Many _low-level_ details of binding and resolving, are often less understood, leading to fragile systems that are hard to maintain and evolve.

The vagueness and complexity comes from both the the package (think of a _box_) and the component be packaged (think of the thing _inside the box_). For users, we hope the package abstraction can just work, however, for developers and maintainers, they have to be aware of enough details. I have been fixing various package management issues, either for my own machine setup or for open-source projects. Through these experiences, I have observed many recurring patterns and common pitfalls across different package management scenarios. I also noticed the **packages** and the things inside the packages share similar concepts, structures, and mechanisms. These things includes files, modules, native binaries, environment variables, etc.

This book is based on my Ph.D. thesis research at Johns Hopkins University, which aims to provide a comprehensive principled and practical understanding of the above topics. We propose a unified framework that models and reasons about package management and its surrounding ecosystem tools, especially, treating concepts and artifacts are **records**. **Records** natually contain **name** and **value** pairs. In practice, people often use terms like **binding** a name to a resource, or **resolving** a name to a resource. We treat them as an implicit record. How to create and how to look up records also natually exists. In Programming Languages (PL) or Logics, we can describe these steps as _introduction_ and _elimination_ rules. We will argue and reason about many existing artifacts are quite similar in the perspective of records.

## Principles

The work doesn't aim to replace existing essential tools, like compilers, build systems, or binary utilities. The framework also doesn't target to formaly verify these tools. Instead, the principles we seek to follow are:

**_Package Transparency Principle_**: Packages are used to pack and deliver software artifacts. These hese artifacts should behave the same as if they are used directly without packaging and delivering. We don't seek to guarantee the correctness of the artifacts themselves. This priciple set us free from the burden of verifying complex software, but focus on the topic of package management.

**_Graded Record Soundness_**: Programming Languages people pursue sound semantics for language constructs. 

Two-folded motivations: 1. observe from the real-world, 2. abstraction natually into a language

The structure of the book is as follows:

## Introduction

- [Summary](SUMMARY.md) This Page
- [Preface](preface.md) Introduction of Grand Unified Package Theory in Practice (GUPT)

## Real-World Case Study

- [Bugfix Reports]()
  - [bugfix report 1]()
- [Forum Discussions]()
  - [post 1]()
- [GitHub Issues]()
  - [issue 1]()
- [Several cases on Z3's opam bindings](case/demo_z3_opam.md)

## Fairyland Case Study

- [Tola Package Manager](case/tola_pkgm.md)

## Understanding Real-World Package Managers

- [Homebrew](case/homebrew.md)
- [npm](case/npm.md)
- [opam](case/opam.md)
- [pip](case/pip.md)
- [Cargo](case/cargo.md)

## Understanding Record-like Artifacts

## Movitation, Challenge, and Solution

## Software Tools

- [Language Sandpiper \\(\lambda_{sp}\\)](tools/sandpiper/intro.md)
  - [Primitives from Package Managers](tools/sandpiper/primitives_pm.md)
  - [Primitives from Language Ecosystems](tools/sandpiper/primitives_eco.md)
  - [Checking for \\(\lambda_{sp}\\)](tools/sandpiper/checking.md)

## Theory

- [Theory of Packages]()
  - [Distributed Key-value Stores](theory/store.md)
  - [Version Logic](theory/version-logic.md)
- [Theory of Records]()
  - [Computer Artifacts as Records](theory/artifacts_as_records.md)
  - [Binding and Resolving](theory/binding_and_resolving.md)
  - [Record Soundness](theory/record-soundness.md)
  - [Lambda Record \\(\lambda_{r}\\)](theory/lambda-record.md)

## Discussion

- [Impact in the AI Era](discuss/ai.md)

## Academic Material

[Report: Grand Unified Package Theory in Practice](report/gupt.md)

[Paper: Package Managers a la carte](report/pkgm-a-la-carte.md)

## Author's Logs

[Todo List](todo.md) Things to do