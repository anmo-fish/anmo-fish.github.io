---
title: "Space Reduction and Representability of Relational Feasibility : A Short Note on Factorization under Coarsening Maps"
authors:
- me
date: "2026-01-21T00:00:00Z"

# Schedule page publish date (NOT publication's date).
publishDate: "2017-01-01T00:00:00Z"

# Publication type.
# Accepts a single type but formatted as a YAML list (for Hugo requirements).
# Enter a publication type from the CSL standard.
publication_types: ["article"]

# Publication name and optional abbreviated publication name.
publication: ""
publication_short: ""

abstract: "A feasibility pattern factors through a labeling if and only if it is invariant across label classes; otherwise, any label-level rule necessarily introduces errors that manifest as spurious cohesion or fragmentation, independent of the underlying objective mechanism."

tags:
- Category theory

featured: true

# hugoblox:
#   ids:
#     arxiv: 1512.04133v1

links:
- type: custom
  label: PREPRINT
  url: https://zenodo.org/records/18620289

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder. 
image:
  caption: 'Image credit: [**Unsplash**](https://unsplash.com/photos/s9CC2SKySJM)'
  focal_point: ""
  preview_only: false

# Associated Projects (optional).
#   Associate this publication with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `internal-project` references `content/project/internal-project/index.md`.
#   Otherwise, set `projects: []`.
projects:
- internal-project

# Slides (optional).
#   Associate this publication with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides: "example"` references `content/slides/example/index.md`.
#   Otherwise, set `slides: ""`.
slides: ""
---
---
## Overview

When we describe social reality, we almost always compress it. Political opinions
become "left" or "right." People become demographic categories. Users become
interest clusters. This compression is not a flaw — it is how institutions, algorithms,
and human cognition operate.

But compression has a structural cost. This paper asks a precise question: **when
does a simplified description faithfully reproduce the underlying relational pattern,
and when does it necessarily fail?**

The answer is a clean theorem. Exact representation is possible if and only if the
objective pattern is *invariant on the fibers* of the compression map. When that
condition fails, errors are not a modeling choice — they are forced. And those errors
have a recognizable shape: some relations that should not exist appear to exist, and
some that should exist appear broken. In network terms, apparent cohesion and
apparent fragmentation.

---

## Setup: Two Levels of Description

Fix an objective position space $L$ — the full, latent space of actual positions agents
occupy — and a label space $\Sigma$, the coarser space on which agents and institutions
actually act. A **coarsening map** assigns each latent position a label:

$$\rho: L \to \Sigma$$

When $\rho$ is non-injective, distinct positions share the same label. Information
is lost.

An **objective feasibility pattern** $R^*: L \times L \to \{0,1\}$ records which ties
are structurally feasible at the latent level. The question is whether there exists a
**label-level rule** $\hat{R}: \Sigma \times \Sigma \to \{0,1\}$ that reproduces $R^*$
exactly:

$$R^*(x, y) = \hat{R}(\rho(x), \rho(y)) \quad \forall\, x, y \in L$$

---

## The Core Theorem: Fiberwise Invariance

**Theorem 3.1** gives the exact condition.

$R^*$ is representable on $\Sigma$ under $\rho$ **if and only if** it is invariant on
$\rho$-fibers: whenever two pairs of positions share the same labels,

$$\rho(x) = \rho(x') \;\wedge\; \rho(y) = \rho(y') \;\implies\; R^*(x,y) = R^*(x',y')$$

If this condition fails, no label-level rule $\hat{R}$ can match $R^*$ on $L$. The
failure is not a limitation of any particular model — it is the inescapable consequence
of the coarsening.

The political example makes this concrete. Collapse a continuous ideological space into
two labels, "left" and "right," and define $R^*$ by a proximity threshold. Two
far-apart positions may share the same label; two nearby positions may be split across
the boundary. No binary rule on the two labels can reproduce the threshold relation.

---

### When Errors Are Unavoidable

Once fiberwise invariance fails, errors are structurally forced for any rule $\hat{R}$.

- **False positives:** a pair $(i,j)$ is predicted feasible ($\hat{R}_{ij} = 1$) but is
  objectively infeasible ($R^*_{ij} = 0$). In network terms: spurious ties.
- **False negatives:** a pair is predicted infeasible but is objectively feasible.
  In network terms: real ties removed.

The canonical over-approximation $R^\exists := f^*(\exists_f(R))$ is the smallest
representable relation containing $R^*$. The canonical under-approximation
$R^\forall := f^*(\forall_f(R))$ is the largest representable relation contained in $R^*$.
Together they bracket the objective pattern:

$$R^\forall \subseteq R^* \subseteq R^\exists$$

False positives concentrate in $\Delta^\exists := R^\exists \setminus R^*$; false
negatives in $\Delta^\forall := R^* \setminus R^\forall$.

When these errors are not uniformly distributed — when they cluster in certain regions
of the label space — they present as *apparent cohesion* or *apparent fragmentation*:
features that look structural but are artifacts of the compression.

---

### Asymmetry and Sensitivity

Not all fibers are equal. If one fiber $\rho^{-1}(\sigma)$ is large and internally
heterogeneous with respect to $R^*$, the canonical over-approximation tends to fill
in many pairs within that fiber. Players whose latent positions fall inside such a
fiber face a systematically higher rate of false positives than players in small,
homogeneous fibers. This asymmetry comes from the fiber structure of $\rho$ alone —
not from behavior.

The sensitivity observation is equally important. If $R^*$ is close to fiberwise
invariance, $\Delta^\exists$ may be small. But a small change in $R^*$ — say, caused
by a bifurcation event in the sense of the companion paper — can break invariance on
a single fiber and cause $\Delta^\exists$ to grow suddenly. The event does not create
incompatibility; it changes which pairs fall on which side of $R^*$. Previously
hidden structure becomes visible at once.

---

## Appendix B: Inference Under Coarsening as Interval Structure

This is perhaps the most practically consequential part of the paper.

Even when $R^*$ does not factor through $\rho$, one might still attempt to *infer* or
*approximate* $R^*$ using only label-level information. **Proposition B.1** shows that
such inference is necessarily interval-valued.

The tightest representable lower bound is $R^\forall$; the tightest representable upper
bound is $R^\exists$. Any concrete rule $\hat{R}$ on $\Sigma$ selects a representable
relation — but by Theorem 3.1, no such relation can coincide with $R^*$ when
fiberwise invariance fails. The best one can do is locate $R^*$ within the interval
$[R^\forall, R^\exists]$.

The **ambiguity region** captures this irreducible indeterminacy:

$$B := R^\exists \setminus R^\forall = \Delta^\exists \cup \Delta^\forall$$

$B$ records precisely those pairs whose feasibility status *cannot be determined* from
label-level information alone. This is not noise or model uncertainty — it is structural
indeterminacy forced by the identification of distinct latent positions within the same
fiber of $\rho$.

### Design: Conservative vs. Permissive

When $R^*$ is not representable, any designer choosing a label-level rule must decide
how to handle the ambiguity region $B$. The paper identifies two poles:

- **Conservative design** moves $\hat{R}$ toward $R^\forall$, eliminating ambiguous
  pairs. This minimizes false positives at the cost of more false negatives.
- **Permissive design** moves $\hat{R}$ toward $R^\exists$, admitting ambiguous pairs.
  This minimizes false negatives at the cost of more false positives.

The interval $[R^\forall, R^\exists]$ describes the full range of structurally admissible
inferences. Exact recovery of $R^*$ is possible if and only if the interval collapses
to a point — which, by Theorem 3.1, happens precisely when $R^*$ is invariant on
$\rho$-fibers.

---

## Relation to the Companion Paper

This note sits alongside the author's axiomatic theory of relational impossibility.
That work studies feasibility in the objective space $L$ under position-dependent
constraints, showing that some relational patterns cannot occur there. This note takes
the objective pattern as given and asks a different question: does it survive compression
without distortion?

The two results cleanly separate two sources of structural limitation:

- **Objective limitation:** infeasibility caused by constraints internal to $L$.
- **Representational limitation:** information loss under $\rho$ that prevents exact
  description on $\Sigma$.

Both result in apparent fragmentation or apparent cohesion. But their causes are
entirely distinct — and conflating them produces misdiagnosis.