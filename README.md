# Classic Mathematical and Operational Research (OR) Problems

This repository outlines some classic problems in Operational Research (OR) and Mathematics, categorized by their application areas.

---

## 1. Optimization Problems

- **Traveling Salesman Problem (TSP)**  
  *Goal*: Find the shortest possible route for a salesman to visit all cities exactly once and return to the origin.  
  *Applications*: Logistics, circuit design, DNA sequencing.

- **Knapsack Problem**  
  *Goal*: Select items with maximum total value without exceeding a weight limit.  
  *Variants*: 0-1 (binary choices), fractional (continuous).  
  *Applications*: Resource allocation, financial portfolios.

- **Linear Programming (LP)**  
  *Goal*: Optimize a linear objective function subject to linear constraints.  
  *Example*: Resource allocation for factories under production constraints.

- **Nonlinear Optimization**  
  *Goal*: Optimize a nonlinear objective function (e.g., quadratic programming).  
  *Example*: Portfolio optimization balancing risk and return.

- **Integer Programming**  
  *Goal*: Linear/nonlinear optimization with integer variables.  
  *Example*: Facility location (binary decisions to open/close sites).

---

## 2. Scheduling and Routing

- **Job Shop Scheduling**  
  *Goal*: Schedule jobs on machines to minimize completion time (makespan).  
  *Applications*: Manufacturing, project management.

- **Vehicle Routing Problem (VRP)**  
  *Goal*: Optimize delivery routes for multiple vehicles with capacity constraints.  
  *Variants*: Time windows, dynamic demand.

- **Shortest Path Problem**  
  *Goal*: Find the shortest path between nodes in a graph (e.g., Dijkstra’s algorithm).  
  *Applications*: GPS navigation, network routing.

---

## 3. Resource Allocation

- **Assignment Problem**  
  *Goal*: Assign tasks to workers/machines at minimum cost (e.g., Hungarian algorithm).  
  *Applications*: Workforce management, matchmaking systems.

- **Transportation Problem**  
  *Goal*: Minimize shipping costs between suppliers and consumers.  
  *Example*: Delivering goods from warehouses to stores.

- **Set Cover Problem**  
  *Goal*: Select the smallest subset of sets that covers all elements.  
  *Applications*: Network coverage, sensor placement.

---

## 4. Network and Flow Problems

- **Maximum Flow Problem**  
  *Goal*: Determine the maximum flow through a network (e.g., Ford-Fulkerson algorithm).  
  *Applications*: Traffic flow, pipeline networks.

- **Minimum Spanning Tree (MST)**  
  *Goal*: Connect all nodes in a graph with the least total edge weight (e.g., Kruskal’s algorithm).  
  *Applications*: Network design, clustering.

- **Graph Coloring**  
  *Goal*: Color graph nodes with the fewest colors such that adjacent nodes differ.  
  *Applications*: Timetabling, register allocation.

---

## 5. Queuing and Inventory

- **M/M/1 Queuing Model**  
  *Goal*: Analyze system performance (wait times, queue length) with Poisson arrivals and exponential service times.  
  *Applications*: Call centers, traffic light timing.

- **Economic Order Quantity (EOQ)**  
  *Goal*: Determine optimal order quantity to minimize holding and ordering costs.  
  *Example*: Retail inventory management.

- **Newsvendor Problem**  
  *Goal*: Decide how much inventory to stock under uncertain demand.  
  *Applications*: Perishable goods, fashion retail.

---

## 6. Game Theory

- **Prisoner’s Dilemma**  
  *Goal*: Analyze strategic interactions between rational agents.  
  *Applications*: Economics, auction design, cybersecurity.

- **Nash Equilibrium**  
  *Goal*: Identify stable strategies where no player benefits from changing their move.  
  *Example*: Pricing competition between firms.

---

## 7. Stochastic and Dynamic Problems

- **Dynamic Programming**  
  *Goal*: Solve multi-stage problems by breaking them into simpler subproblems.  
  *Example*: Inventory restocking over time.

- **Markov Decision Process (MDP)**  
  *Goal*: Optimize decisions in stochastic environments with states and rewards.  
  *Applications*: Robotics, healthcare treatment planning.

---

## 8. Classic Mathematical Puzzles

- **Monty Hall Problem**  
  *Goal*: Probability-based decision-making (switch or stay after a door reveal).

- **Seven Bridges of Königsberg**  
  *Goal*: Determine if a path exists that crosses each bridge exactly once.  
  *Note*: Foundation of graph theory.

- **Towers of Hanoi**  
  *Goal*: Recursive puzzle to move disks between pegs with minimal moves.

---

## Real-World Applications

- **Energy Grid Optimization**: Balance supply/demand using mixed-integer programming.  
- **Healthcare Scheduling**: Assign shifts to nurses while minimizing overtime.  
- **Supply Chain Resilience**: Model disruptions and reroute logistics dynamically.  
- **Airline Crew Scheduling**: Assign crews to flights while complying with regulations.

---

> These problems form the backbone of OR and mathematical modeling, with applications in industries ranging from logistics to finance.

# 🧰 Tools and Python Libraries for Operations Research Problems

## 1. Optimization Libraries

| Library / Tool       | Description                                                                                  |
|----------------------|----------------------------------------------------------------------------------------------|
| **PuLP**             | Linear programming library in Python. Interfaces with solvers like CBC, GLPK, CPLEX, Gurobi. |
| **OR-Tools**         | Google’s open-source suite for combinatorial optimization and routing problems.              |
| **CVXPY**            | Python library for convex optimization problems (LP, QP, SOCP, SDP).                         |
| **Pyomo**            | Extensive modeling language for linear, nonlinear, integer, and stochastic programming.      |
| **SciPy.optimize**   | Offers functions for general-purpose optimization (minimize, curve fitting, etc.).           |
| **GEKKO**            | Optimization suite for dynamic systems, non-linear models, and differential equations.       |
| **Optuna**           | Framework for hyperparameter and black-box optimization (useful in ML and OR blend).         |

---

## 2. Solvers (Backends for Libraries)

| Solver         | Type                        | Description                                                                 |
|----------------|-----------------------------|-----------------------------------------------------------------------------|
| **CBC**        | LP, MILP                    | Open-source solver, default for PuLP.                                       |
| **GLPK**       | LP, MILP                    | GNU Linear Programming Kit (open-source, slower for large problems).        |
| **CPLEX**      | LP, MILP, QP, etc.          | IBM’s high-performance commercial solver (free for academics).              |
| **Gurobi**     | LP, MILP, QP, NLP           | Commercial solver, very fast, free academic license.                        |
| **SCIP**       | MILP, Nonlinear             | Open-source for academic use, powerful for constraint integer programming.  |
| **HiGHS**      | LP, MILP                    | Modern high-performance solver, integrated with SciPy.                      |

➡️ *Note: Solvers like Gurobi and CPLEX integrate with PuLP, Pyomo, CVXPY.*

---

## 3. Specialized Libraries by Problem Type

### Graph, Routing, Scheduling
| Library           | Description                                                                                |
|-------------------|--------------------------------------------------------------------------------------------|
| **NetworkX**      | Graph theory and network analysis. Great for shortest paths, graph coloring, MST, etc.   |
| **Graph-Tool**    | Fast graph analysis using C++ backend (for large networks).                               |
| **OR-Tools**      | Excellent for VRP, TSP, job-shop scheduling, flow problems.                               |

---

### Queuing and Simulation
| Library           | Description                                                                 |
|-------------------|-----------------------------------------------------------------------------|
| **SimPy**         | Discrete-event simulation in Python (queuing systems, resource modeling).   |
| **Arena / AnyLogic** | Commercial tools for simulation (if you need GUI modeling).               |

---

### Game Theory
| Library           | Description                                                              |
|-------------------|--------------------------------------------------------------------------|
| **Nashpy**        | For computing Nash equilibria in 2-player games.                         |
| **Axelrod-Python**| For iterated prisoner's dilemma simulations.                             |

---

### Dynamic Programming & MDPs
| Library           | Description                                                                       |
|-------------------|-----------------------------------------------------------------------------------|
| **MDPtoolbox**    | Solves Markov Decision Processes via policy/value iteration.                     |
| **RLlib**         | Reinforcement Learning library (useful for large MDPs, stochastic control).       |

---

### Inventory & Stochastic Models
| Library             | Description                                                                 |
|---------------------|-----------------------------------------------------------------------------|
| **PyMC**            | Probabilistic modeling using Bayesian inference (for stochastic demand).    |
| **statsmodels**     | Time series analysis, statistical modeling (e.g., EOQ under uncertainty).   |
| **ForecastingTools**| Demand forecasting, ARIMA, etc. (or use Prophet for demand predictions).    |

---

## 4. Solvers with GUI / Other Languages (if needed)

| Tool               | Description                                                         |
|--------------------|---------------------------------------------------------------------|
| **IBM CPLEX Studio** | GUI + Python/Java support for complex LP/MIP problems.              |
| **AMPL / GAMS**    | Modeling languages with interfaces to many solvers. Costly.         |
| **Excel Solver**   | Good for small LP/MILP problems (educational use).                  |

---

## 5. Additional Tools for Real-World OR Applications

| Tool/Library       | Use Case                                                                          |
|--------------------|-----------------------------------------------------------------------------------|
| **Dash / Streamlit** | Build dashboards to visualize OR solutions and models.                           |
| **Plotly / Matplotlib** | Visualization of routes, graphs, networks, flows, etc.                         |
| **Pandas / NumPy**   | Data manipulation, matrix operations for LP/ILP modeling.                        |
| **Jupyter Notebooks**| Interactive coding and modeling environments for optimization problems.         |

---

# 🧩 Example Stack by Problem

| Problem Type               | Recommended Tools                                                    |
|----------------------------|----------------------------------------------------------------------|
| LP, MILP                   | PuLP / Pyomo + CBC/CPLEX/Gurobi                                      |
| TSP, VRP                   | OR-Tools, NetworkX, Google Maps API (for real-world routing)         |
| Queuing Models             | SimPy, SciPy, NumPy                                                  |
| Game Theory                | Nashpy, Axelrod-Python                                               |
| Flow/Graph Problems        | NetworkX, OR-Tools, Graph-Tool                                       |
| Scheduling (Job-shop, etc.)| OR-Tools, Pyomo                                                      |
| Inventory/EOQ              | Pyomo, SciPy.optimize, PyMC for stochastic demand                    |
| MDP / Dynamic Programming  | MDPtoolbox, RLlib, NumPy                                             |

---


