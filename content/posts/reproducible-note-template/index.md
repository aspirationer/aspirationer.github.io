---
title: "What Should a Reproducible Research Note Record?"
date: 2026-07-18T20:20:00+08:00
draft: false
description: "From questions and data to environments, randomness, and negative results: an experiment record your future self can understand."
summary: "Reproducibility is more than saving code. A useful research note also preserves the question, assumptions, data version, runtime environment, evaluation procedure, and negative results."
tags:
  - "Reproducible Research"
  - "Experiments"
  - "Workflow"
categories:
  - "Methods"
showToc: true
---

“The code runs” is only the starting point of reproducibility. When reopening a project months later, the more common questions are: Why was it done this way? Which data version was used? Which run produced the numbers in the figure? Why were the experiments that never appeared in the paper abandoned?

## 1. Questions and assumptions

State the research question as concisely as possible, and distinguish between:

- hypotheses to be tested;
- established background facts;
- working assumptions that have not yet been verified.

When these are mixed together, it becomes easy to overinterpret experimental results.

## 2. Data identity

Do not record only the dataset name. At a minimum, preserve:

- acquisition date and source;
- version number, commit hash, or checksum;
- sample inclusion and exclusion rules;
- preprocessing scripts and parameters;
- data-use license.

## 3. Runtime environment

Dependency lockfiles, operating systems, hardware, drivers, and random seeds can all affect results. For important experiments, the environment should be reconstructable through a script or container.

```text
commit: <git-sha>
data: <version-or-checksum>
environment: <lockfile-or-image>
seed: <integer>
command: <exact-entrypoint>
```

## 4. Evaluation and decisions

Writing down the primary evaluation metric and success criteria before seeing the results can reduce post hoc metric selection. Metrics can be changed, but the reason for the change should be documented.

## 5. Negative results

A failed experiment is still information. Record what it rules out, where the failure may have originated, and how the next experiment could distinguish between competing explanations. Your future self and collaborators will avoid repeating the same dead ends.

## A simple standard

If a note allows your future self, six months later, to answer what was done, why it was done, where the result came from, and what remains uncertain, it is already more valuable than most experiment logs.
