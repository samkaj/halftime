---
marp: true
title: Developing an Open Source Performance Benchmarking Git Bot
_class: invert
---

# **Halftime** - Developing an Open Source Performance Benchmarking Git Bot

**Students:** Ali Alkhaled, Elin Hagman, Samuel Kajava, Jonathan Linder, Kasper Ljunggren & Linus Lundgren

**Supervisor:** Philipp Leitner

---

## The Problem

Using Continuous Integration (CI) for evaluating programs is necessary for a project's longevity, and is most commonly based on running tests - **it works or it doesn't**.

**What about performance?** Few tools exist to run performance benchmarks in projects, and bugs slowing down the code remain hidden as a result. Similar CI tools for this kind of evaluation barely exist at all.

## Our Task

Provide a **GitHub Bot** for developers who wants to measure their projects' performance continuously.

---

## Some Background

-   **Java Microbenchmarking Harness (JMH)** [[1]](#sources) - run performance tests on your Java projects
-   **GitHub Apps** [[2]](#sources) - communication with GitHub, send updates (**webhook events**) regarding projects to the Performance Bot
-   **MongoDB** [[3]](#sources) - open source NoSQL document-based database

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

<h2> Progress and Continunation - Development</h2>

<div style="columns: 2; height: 40vh">
<div style="margin-bottom: 100px">

<h3 style="margin-top: 0"> Progress </h3>

-   Receive webhook events
-   Run code in containers
-   Store results in database
-   Open GitHub issue with results

</div>
<div>

### Upcoming

-   **Statistical analysis and presentation**
-   **Configurability** - build tools, which tests to run, etc.
-   **Deployment** - ship the bot and make it available for public use

</div>
</div>

---

## Progress and Continunation - Thesis Work

<div style="columns: 2; height: 40vh">
<div style="margin-bottom: 100px">

<h3 style="margin-top: 0"> Progress </h3>

-   Preliminary structure
-   Background - both academic and technical
-   References

</div>
<div>

### Upcoming

-   Describe the process
-   Scientific relevancy
-   Importance of performance analysis in CI

</div>
</div>

---

## Some Experiences

-   Large stack
-   Learning by doing

---

## Questions?

---

<!-- _class: invert -->

## Sources

**[1]** OpenJDK, _JMH_ - [https://github.com/openjdk/jmh](https://github.com/openjdk/jmh)

**[2]** GitHub, _About apps_ - [https://docs.github.com/en/apps/creating-github-apps/creating-github-apps/about-apps](https://docs.github.com/en/apps/creating-github-apps/creating-github-apps/about-apps)

**[3]** MongoDB Inc., _What Is MongoDB_ - [https://www.mongodb.com/what-is-mongodb](https://www.mongodb.com/what-is-mongodb)
