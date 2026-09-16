# Worked Example 02 — "My algorithm is better; how do I turn it into a stronger research project?"

## User request

> I improved an existing tensor/multiview algorithm and the benchmark metrics are better than the original paper. How should I extend it into a stronger project and paper?

---

## Default execution-first response

A conventional assistant may suggest:

- add more datasets;
- compare more baselines;
- tune hyperparameters;
- add ablations;
- make the network deeper;
- write a stronger Introduction.

All of these may improve execution while preserving an incremental project.

---

# ROUTE analysis

## R — Reframe

**Surface task:** Extend an improved algorithm into a stronger paper.

**Real objective:** Create a research contribution whose importance is not dependent on a small benchmark gain over the closest method.

The key reframing is:

> Do not ask only "How can we improve this algorithm further?"  
> Ask "What important scientific/data problem becomes solvable if we use the student's mathematical capability differently?"

---

## O — Outcome

**Key stakeholder:** Future reviewer and scientific user.

**Success criterion:** The work owns a problem that matters, and the algorithm becomes necessary because of the problem—not the other way around.

A stronger paper should ideally survive this test:

> If the algorithmic component were renamed, would the reader still care about the problem and result?

**Non-goal:** Maximize the number of technical modifications.

---

## U — Understand the game

Algorithmic student projects often inherit their problem definition from the previous paper.

This creates path dependence:

```text
previous paper
   ↓
its benchmark
   ↓
its metric
   ↓
small method improvement
   ↓
same scientific importance ceiling
```

A student with strong mathematical skills may have more leverage by transferring the method to a domain with unmet constraints, for example:

- incomplete or unpaired scientific multimodal data;
- streaming/large-scale measurements;
- uncertainty-aware inference;
- expensive labels;
- physically constrained observations;
- data acquired adaptively during an experiment.

The scientific constraint should select the algorithmic innovation.

---

## T — Test

### Framing test
Why does the current benchmark matter outside the method literature?

### Failure test
Suppose the new model beats the best baseline by 2–3%. Would a skeptical scientist change how they work?

### Transfer test
Which part of the student's method is genuinely valuable?

Examples:
- low-rank modeling;
- incomplete-view inference;
- robust graph construction;
- optimization under missing observations;
- scalable decomposition.

Can that capability address a more important scientific bottleneck?

### Second-order test
If the project remains benchmark-centric, the student may become increasingly good at incremental algorithm optimization but weaker at defining scientific questions.

### Alternative routes

**Route A — Continue algorithm optimization**  
Lowest risk; likely incremental.

**Route B — Scientific problem first**  
Select a real measurement/data bottleneck, derive method requirements from it, then adapt the algorithm.

**Route C — Methodological generalization**  
Identify a general limitation (scaling, missingness, uncertainty, online updates) that affects many domains and redesign around it.

### Recommended route
Prefer **B** when credible domain access/data exist; otherwise **C**.

---

# Strategy Contract

**Surface task:** Improve and publish an algorithm.  
**Real objective:** Build a scientifically or methodologically important research contribution.  
**Key stakeholder:** Reviewer + eventual scientific user.  
**Success criterion:** The problem remains compelling even before the new algorithm is introduced.  
**Strategic risk:** Optimizing inside the previous paper's problem definition and inheriting its novelty ceiling.  
**Recommended first move:** Inventory the student's transferable mathematical strengths, then match them to a real scientific data bottleneck.

---

# E — Execute by gates

## Strategy
Write two lists separately:

**Student capability**
- mathematical tools;
- optimization strengths;
- data assumptions the method handles well.

**Scientific constraints**
- missing modalities;
- sparse labels;
- high throughput;
- uncertainty;
- online acquisition;
- physical constraints.

Find a high-value intersection.

## Structure
Define:

1. scientific/data bottleneck;
2. why existing approaches fail;
3. new methodological requirement;
4. method;
5. benchmark + real scientific demonstration.

## Artifact
Only then design experiments and paper figures.

## Polish
Write the story around the problem-to-method logic rather than "we improve method X."

---

## Teaching point

**AI can make incremental work faster. Strategy decides whether faster execution raises or merely reaches the same ceiling sooner.**
