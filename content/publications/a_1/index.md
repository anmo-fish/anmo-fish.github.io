---
title: "The Impossibility of Cohesion Without Fragmentation"
authors:
- me
date: "2026-01-16T00:00:00Z"

# Schedule page publish date (NOT publication's date).
publishDate: "2017-01-01T00:00:00Z"

# Publication type.
# Accepts a single type but formatted as a YAML list (for Hugo requirements).
# Enter a publication type from the CSL standard.
publication_types: ["article"]

# Publication name and optional abbreviated publication name.
publication: ""
publication_short: ""

abstract: "Why do division and cohesion often intensify together? This paper develops a static structural theory of relation maintenance based on minimal positional constraints. Rather than relying on utility-based or probabilistic models, social relations are formalized as constraint satisfaction problems over an abstract position space. When a bifurcation event---such as a vote or institutional assignment---fixes agents positions, relational viability is determined solely by positional compatibility. We establish three structural results. First, under any non-degenerate positional constraint, fragmentation (relational collapse) and cohesion (condition confirmation) necessarily coexist as complementary outputs of a single compatibility function. Second, we prove a structural asymmetry of veto power: relation maintenance requires logical conjunction, while collapse requires only logical disjunction, implying that fragmentation operates as a unilateral structural veto. This yields a purely logical foundation for behavioral premises such as pairwise stability. Finally, we establish a conditional impossibility theorem: under positional plurality, avoiding relational collapse is structurally impossible, leaving coercive homogenization as the only design-level guarantee for universal cohesion. The framework isolates minimal boundary conditions and provides a formal language for analyzing polarized relational structures."

tags:
- Structural Theory
- Physics and Society

featured: true

# hugoblox:
#   ids:
#     arxiv: 1512.04133v1

links:
- type: preprint
  provider: arxiv
  id: 2601.15317
# - type: code
#   url: https://github.com/HugoBlox/kit
# - type: slides
#   url: https://www.slideshare.net/
# - type: dataset
#   url: "#"
# - type: poster
#   url: "#"
# - type: source
#   url: "#"
# - type: video
# #   url: https://youtube.com
- type: custom
  label: QA NOTE
  url: https://zenodo.org/records/18452929/files/The_Impossibility_of_Cohesion_Without_Fragmentation_qa_note.pdf?download=1

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
projects: []

# Slides (optional).
#   Associate this publication with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides: "example"` references `content/slides/example/index.md`.
#   Otherwise, set `slides: ""`.
slides: ""
---
---
## Overview
**Why does a community become more unified and more divided at the same time?**

This is not a paradox. This paper shows it is a structural necessity.

---

### The Question

Empirical observers of polarized societies often note a striking pattern: as groups fragment 
along political, ideological, or institutional lines, each fragment becomes 
*more* internally cohesive. Standard approaches --- utility maximization, probabilistic tie 
formation, threshold models --- can reproduce this pattern, but they cannot *explain* it 
without importing behavioral or psychological assumptions.

This paper asks a more fundamental question: is there a purely structural reason why 
cohesion and fragmentation must co-emerge?

The answer is yes.

---

### A Structural, Not Behavioral, Theory

The framework deliberately discards:

- Preferences and utility
- Psychological motivations
- Probabilistic assumptions
- Temporal dynamics

What remains is a minimal logical skeleton. A **relation** exists between two players only 
if certain structural conditions --- called *gain axes* --- are satisfied. Each player $i$ has 
a minimum condition function:

$$a(i, g) \in \{0, 1\}$$

indicating whether gain axis $g$ is structurally required. A relation collapses if any 
required axis goes unmet.

Players occupy positions in an abstract **position space** $L$, subject to one ontological 
axiom: each player occupies exactly one position within a given structural state. Whether 
a gain axis can be satisfied between two players depends on their positions via a 
**compatibility function**:

$$f_g: L \times L \to \{0, 1\}$$

No metric, no topology, no ordering is assumed on $L$. The framework is that general.

---

### The Mechanism: Bifurcation Events

A **bifurcation event** is any structural intervention that forces every player into a 
determinate position:

$$E: P \to L$$

Examples include a vote, a loyalty declaration, institutional assignment, or even an act of 
public alignment on social media. The theory does not model *why* such events occur --- only 
what *must* follow structurally once positions are fixed.

Once $E$ is applied, local compatibility values propagate to the entire network. For every 
pair $(i, j)$, the value $f_g(E(i), E(j))$ is now determined. There is no room for 
negotiation or adjustment.

---

### Three Structural Results

**Theorem 10.2** establishes a dichotomy. Let $g$ be a gain axis relevant to the initial 
relation set, and let $E$ be any bifurcation event. Then exactly one of the following holds:

1. **Degeneracy:** $f_g(E(i), E(j))$ is constant across all relevant pairs --- the positional 
   constraint exerts no selective pressure. This is the exceptional, empirically rare case.

2. **Structural Necessity:** If non-degenerate, the post-event network *necessarily* 
   exhibits both:
   - **Fragmentation** --- relations bridging incompatible positions are structurally forced 
     to collapse ($f_g(E(i), E(j)) = 0$)
   - **Cohesion** --- relations within compatible configurations survive 
     ($f_g(E(u), E(v)) = 1$)

These are not two separate effects. They are the $0$ and $1$ outputs of the *same* 
compatibility function applied under the *same* structural constraint.

**Proposition 8.3** establishes a structural asymmetry of veto power. The logical conditions 
governing collapse and cohesion are not symmetric:

- Relational collapse requires only **unilateral** condition failure --- governed by logical 
  disjunction ($a(i,g)=1 \lor a(j,g)=1$)
- Cohesion confirmation requires **bilateral** match --- governed by logical conjunction 
  ($a(i,g)=1 \land a(j,g)=1$)

Fragmentation therefore operates as a unilateral structural veto, while cohesion requires 
mutual structural alignment. This is a purely logical consequence of the axiomatic system, 
independent of any behavioral or cultural factors. As a corollary, it provides a structural 
foundation for the behavioral premise underlying pairwise stability in network economics: 
the rule that severance is unilateral while formation is bilateral is not merely a modeling 
convention --- it is a logical necessity under constraint satisfaction.

**Theorem 11.3** establishes the conditional impossibility of universal cohesion. Under 
positional plurality, there is no bifurcation event that avoids relational collapse for every 
possible initial relation set --- except coercively homogenizing ones, which enforce 
compatibility across all pairs by design.

---

### What This Means

The paper establishes two corollaries with direct interpretive force.

First, the only structural condition permitting universal cohesion --- cohesion without any 
fragmentation --- is a globally existence-dependent gain axis: one where $f_g \equiv 1$ 
everywhere. Every genuinely position-dependent constraint imposes selective relational 
mortality.

Second, and perhaps most strikingly: **forming an in-group structurally necessitates the 
definition of an out-group.** Under any non-trivial positional constraint, any cohesive 
subset $C \subseteq P$ is necessarily incompatible with at least one player outside $C$. 
This is not a sociological observation. It is a theorem.

---

### Why This Matters

The intensification of in-group cohesion alongside inter-group division requires no 
additional mechanism --- no radicalization dynamics, no echo chamber effects, no strategic 
calculation. It is the unavoidable output of relation-maintenance constraints operating 
under positional commitment.

This provides a common structural language applicable across polarized political networks, 
institutional sorting, and identity-based alignment --- one that remains agnostic about the 
specific processes generating any particular bifurcation event.