# Advanced-Data-Engineering-

# Workload-Balanced Multi-Objective Delivery Route Optimization

## Overview
This project presents a multi-objective Genetic Algorithm (GA) framework for solving delivery route optimization with workload balancing.

Traditional routing approaches primarily focus on minimizing travel distance. However, such methods often lead to uneven workload distribution among delivery agents. This system addresses that limitation by simultaneously optimizing route efficiency and workload balance.

---

## Problem Statement
In delivery logistics, minimizing distance alone can result in certain agents being overloaded while others remain underutilized. This leads to inefficiency, delays, and poor resource utilization.

The objective of this project is to develop a system that:
- Minimizes total travel distance  
- Ensures balanced workload distribution among agents  
- Maintains fairness in task allocation  

---

## Approach

### Solution Representation
Each solution (chromosome) represents delivery assignments:
- Each index corresponds to a delivery  
- Each value represents the assigned agent  

---

### Optimization Technique
The system uses a Genetic Algorithm with the following components:
- Tournament selection  
- Fixed two-point crossover  
- Mutation  
- Elitism  
- Periodic diversity injection  

---

### Local Route Optimization
Each agent’s route is improved using the 2-opt heuristic to ensure more accurate distance computation.

---

## Multi-Objective Fitness Function

The fitness function integrates multiple objectives:

- Total route distance  
- Workload variance  
- Maximum workload  
- Fairness index  
- Overload penalty  
- Distribution of delivery stops  
- Cluster compactness  

### Cluster Compactness
A clustering term is included to ensure that deliveries assigned to each agent are geographically close. This improves route efficiency while maintaining workload balance.

---

## Results

The Genetic Algorithm is compared with a baseline round-robin assignment strategy.

| Metric        | Baseline | Genetic Algorithm |
|--------------|----------|------------------|
| Distance     | Higher   | Lower            |
| Max Load     | Higher   | Lower            |
| Variance     | Higher   | Near zero        |
| Fairness     | Lower    | Significantly improved |

The results show that the proposed method improves both efficiency and workload distribution.

---

## Baseline Clarification
The baseline used in this project is a round-robin assignment method. It does not perform optimization and serves only as a reference for comparison.

---

## Key Contributions
- Multi-objective formulation of delivery routing  
- Integration of workload balancing into optimization  
- Use of fixed crossover for structural consistency  
- Inclusion of clustering to improve spatial efficiency  
- Fairness-driven evaluation framework  

---

## Future Scope
- Pareto-based multi-objective optimization methods (e.g., NSGA-II)  
- Inclusion of additional constraints such as vehicle capacity and delivery priorities  
- Integration with real-world distance metrics  
- Scalability improvements for larger problem instances  

---

## Tech Stack
- Python  
- NumPy  
- Matplotlib  

---

## Team
- Riya Susan Samuel  23MID0150
- Neha Srikanth   23MID0168
- Pragna Madineni Jayadev  23MID0375

---

## How to Run
Run the main Python file:
