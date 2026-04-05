# 🧠 DCOP Algorithms Simulator

## 📖 Overview
This project implements and analyzes **distributed multi-agent optimization algorithms** in the context of **Distributed Constraint Optimization Problems (DCOP)**.

We simulate several well-known algorithms and evaluate their performance under different problem structures, with a focus on the trade-off between **exploration** and **exploitation**.

> Developed as part of a course on distributed systems and optimization, this project explores decentralized decision-making and coordination between agents under constraints.

---

## ⚙️ Implemented Algorithms
- **DSA (Distributed Stochastic Algorithm)**  
  - Probability configurations: `p = 0.2, 0.7, 1.0`
- **MGM (Maximum Gain Messaging)**
- **MGM-2**

---

## 🧪 Experimental Setup

### Problem Types

#### 1. Sparse Random Graph
Low connectivity between agents leads to weaker dependencies and fewer constraints.  
This environment encourages parallel updates and favors **exploration-driven algorithms**.

---

#### 2. Dense Random Graph
High connectivity creates strong interdependencies between agents.  
Effective solutions require coordination, making **MGM and MGM-2** more suitable.

---

#### 3. Graph Coloring Problem
Agents must select values such that neighboring agents do not share the same assignment.  
The objective is **conflict minimization**, rather than complex optimization.

---

### Key Configuration Parameters
Each problem varies in:
- **Agent connectivity**
- **Constraint density**
- **Domain size** (number of possible assignments)

---

### 📊 Problem Configuration Summary

| Problem Type         | Density (p) | Domain Size | Cost Function                          |
|---------------------|------------|------------|----------------------------------------|
| Sparse Random Graph | 0.25       | 5          | cᵢⱼ ∼ U(100, 200)                      |
| Dense Random Graph  | 0.75       | 5          | cᵢⱼ ∼ U(100, 200)                      |
| Graph Coloring      | 0.1        | 3          | cᵢⱼ = 0 if xᵢ ≠ xⱼ, else penalty cost  |

---

## 📈 Results & Insights

As detailed in the [project report](Project%20Report%20-%20MAO.pdf):

- Sparse environments favor **exploration-heavy approaches** (DSA performs best)
- Dense environments benefit from **coordinated algorithms** (MGM, MGM-2)
- Graph coloring emphasizes **conflict resolution** over optimization
- Excessive exploration leads to **instability and lack of convergence**

### Outputs include:
- Convergence graphs  
- Cost vs. iteration analysis  
- Algorithm performance comparisons  

---

## 👥 Contributors
- **Leah Rosen**
- [Lilach Yosef](https://github.com/LilachYosef)
- Ofri Ratinsky

---

## 🔮 Future Work
- Asynchronous agent communication  
- Reinforcement learning-based agents  
- Real-world applications (e.g., smart grids, traffic systems)  
