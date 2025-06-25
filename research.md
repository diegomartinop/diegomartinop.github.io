---
layout: default
title: Research
permalink: /research/
---

# Research

## Inventory Routing Problem

The study of the Inventory Routing Problem (IRP) began in 2021 and is ongoing to this day. This work is part of my doctoral thesis, for which I got the degree in November 2024.
The IRP is a vehicle routing problem with inventory management over a multi-period horizon. It involves determining the delivery routes and the quantities to deliver to all customers from a central supplier, ensuring that no stockouts occur, while minimizing transportation and inventory holding costs.

As part of my thesis, a contribution to the classical IRP was proposed. It focuses on the definition of a new, more complex variant of the problem, which includes a heterogeneous fleet of vehicles, time-dependent inventory costs and customer demands, and a delivery policy based on lot sizes.
A mathematical formulation (MILP), a metaheuristic, and a new benchmark set of 80 problem instances were developed for this IRP variant.

The proposed metaheuristic is capable of solving instances with 170 customers over a 28-period time horizon, as well as instances with 183 customers over 7 periods. This represents a significant contribution to the literature, compared to previous studies on IRP-type problems, which are generally limited to a maximum of 12 periods.

## Truck Driver Scheduling Problem

The Truck Driver Scheduling Problem (TDSP) is a vehicle routing problem that involves determining routes while accounting for the regulations imposed by European labor laws regarding driver working hours. This consideration is necessary because traditional vehicle routing problems often produce solutions with excessively long routes that are not feasible for human drivers. Additionally, time windows must be respected, and rest periods must be scheduled to ensure legal compliance.

To solve this problem, a Constraint Programming (CP) approach was developed — considered to be the first of its kind for this problem. Branching strategies inspired by those proposed in the Choco solver were applied to a set of benchmark instances from the literature, and the results are competitive with existing solutions.

This work was conducted as part of my engineering project and continued during my second-year internship, both during the 2019/2020 academic year.

## Strong Network Orientation Problem

The Strong Network Orientation Problem (SNOP) consists in assigning directions to the edges of an undirected graph so that the resulting graph is strongly connected, meaning every node is reachable from any other node. This problem has practical applications in urban networks, where edges represent streets/avenues/roads and nodes represent intersections. The objective is to find a minimum-cost orientation that ensures strong connectivity, while considering the overlap of paths leading to all nodes.

To solve this problem, classic graph algorithms (such as Dijkstra and Kosaraju) were applied, and a General Variable Neighborhood Search (GVNS) metaheuristic was developed specifically for the SNOP. A novel local search move was introduced, based on cycle reversal within the graph. These methods improved both the solution quality and the computation time, compared to existing mathematical formulations and metaheuristics from the literature.

This work was conducted as part of a research project funded by the Brazilian National Council for Scientific and Technological Development (CNPq). The results were presented at the International Conference on Variable Neighborhood Search (ICVNS) — a specialized conference on metaheuristics such as VNS and VND — held in October 2019 in Rabat, Morocco.