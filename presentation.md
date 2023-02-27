---
marp: true
title: Developing an Open Source Performance Benchmarking Git Bot
_class: invert
---

# **Halftime** - Developing an Open Source Performance Benchmarking Git Bot

**Students:** Ali Alkhaled, Samuel Kajava, Jonathan Linder, Linus Lundgren, Elin Hagman & Kasper Ljunggren

**Supervisor:** Philipp Leitner

---

## The Problem

Using Continuous Integration (CI) for evaluating programs is necessary for a project's longevity, and is most commonly based on running tests - **it works or it doesn't**.

**What about performance?** Few tools exist to run performance benchmarks in projects, and bugs slowing down the code remain hidden as result. Similar CI tools for this kind of evaluation barely exist at all.

## Our Task

Provide a **GitHub Bot** for developers who wants to measure their projects' performance continuously.

---

## The Plan

-   Using tools provided by **GitHub**, listen for requests to run a project's benchmarks
-   Run received benchmarks
-   Save benchmark results to a **MongoDB** database
-   Perform statistical analysis
-   Open an issue on **GitHub** with the results from the aforementioned analysis

## Measuring Success

The project is deemed successful if it can run a number of large projects using **JMH** (benchmarking framework for Java) and open issues on **GitHub** providing valuable information regarding the results from the run.

---

## Progress So Far

---

## Questions

---

<!-- _class: invert -->

## Sources
