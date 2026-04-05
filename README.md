# DCOP Algorithms Simulator

## Overview

This project implements and analyzes distributed multi-agent optimization algorithms in the context of DCOP (Distributed Constraint Optimization Problems).
We simulate several well-known algorithms and evaluate their performance under different problem structures, focusing on the trade-off between exploration and exploitation.
This was developed as part of a course on distributed systems and optimization. It focuses on decentralized decision-making and coordination between agents under constraints.
---

## Implemented Algorithms
- DSA (Distributed Stochastic Algorithm)
  - Multiple probability configurations (p = 0.2, 0.7, 1.0)
- MGM (Maximum Gain Messaging)
- MGM-2

---
## Configurations

The algorithms are evaluated on different environments and problems.

## Problem Types:

### 1. Sparse Random Graph
Low connectivity between agents, meaning fewer constraints and weaker dependencies.  
This setting encourages parallel updates and favors exploration-based algorithms.

---

### 2. Dense Random Graph
High connectivity creates strong dependencies between agents.  
Effective solutions require coordination, making algorithms like MGM and MGM-2 more suitable.

---

### 3. Graph Coloring Problem
Agents must choose values such that neighboring agents do not share the same assignment.  
The objective is conflict minimization rather than complex optimization.

Each problem varies in:
- Agent connectivity
- Constraint density
- Domain size - Number of valid assignments.

| Problem Type         | Density (p) | Domain Size | Cost Function                          |
|---------------------|------------|------------|----------------------------------------|
| Sparse Random Graph | 0.25       | 5          | cᵢⱼ ∼ U(100, 200)                      |
| Dense Random Graph  | 0.75       | 5          | cᵢⱼ ∼ U(100, 200)                      |
| Graph Coloring      | 0.1        | 3          | cᵢⱼ = 0 if xᵢ ≠ xⱼ, else penalty cost  |


---

## Conclusions

As detailed in the [project report](Project%20Report%20-%20MAO.pdf),

- Sparse environments favor higher exploration (DSA performs best)
- Dense environments benefit from coordinated algorithms (MGM, MGM-2)
- Graph coloring emphasizes conflict resolution over optimization
- Excessive exploration leads to instability and lack of convergence

Results include:
- Convergence graphs
- Cost over iterations
- Algorithm comparisons

---

## Contributors

- Leah Rosen
- [Lilach Yosef](https://github.com/LilachYosef)
- [Ofri Ratinsky]()

