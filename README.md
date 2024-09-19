# Linear Optimization
Optimizing a Company’s Investment Strategy

## Table of Contents

- [Introduction](#introduction)
- [Data Description](#data-description)
- [Research Questions](#research-questions)
- [Methodology](#methodology)
- [Analysis](#analysis)
- [Result and discussion](#result-and-discussion)
- [References](#references)


## Introduction
This report aims to optimize a company’s investment strategy over a 12-month period, utilizing a network diagram for cash flow visualization and linear programming for decision-making. Additionally, the Markowitz model is modified to manage portfolio risk through Conditional Value at Risk (CVaR) constraints.


## Data Description

The data comprises estimated monthly receipts and expenditures for a company, alongside rates of return from various certificates of deposit (CDs) offered by two banks, CIT and NBD. This dataset serves as the foundation for cash flow analysis and investment strategy formulation.


## Research Questions

1. How can a network diagram aid in visualizing a company’s cash flow and investment strategy?

2. What optimization strategies can maximize returns while considering cash flow constraints?

3. How does modifying the Markowitz model to incorporate CVaR constraints impact portfolio optimization?

## Methodology

Part A: Cash Flow Network Diagram 

1. Graph Creation: A directed graph is established using networkx to represent monthly cash flows.
2. Node Addition: Nodes labeled from “Month 1” to “Month 12” are created.
3. Relationship Definition: Arcs are defined for investments, receipts, and expenditures.
4. Visualization: A grid layout is employed to draw the network, enhancing clarity.

Part B: Optimization Problem Formulation
1. Sets: MONTHS (1-12) and TERMS (1-, 2-, 3-month CDs).
2. Parameters: Monthly receipts, expenditures, and returns.
3. Variables: Investment amounts in each type of CD.
4. Constraints: Cash flow must remain non-negative.
5. Objective Function: Maximize total returns over the 12 months.

Part C: Linear Programming Solution
1. Model Creation: A linear programming model is developed to identify optimal investments.
2. Variable Definition: Investment variables for each CD type are created and added to the model.
3. Constraints: Ensure balanced cash flow and calculate total returns.

Part D: Introducing Investment Limits
1. New Constraints: A cap is placed on investments (max 70% in any one bank per month).
2. Model Adjustment: The investment strategy is re-evaluated under this new policy.

## Analysis

Modifying the Markowitz Model 

Part 1: Portfolio Optimization with CVaR Constraint

- Data Definition: Expected returns and covariance matrix are established.

- Objective Function: Focus on maximizing expected returns while constraining CVaR to ≤ 0.

Part 2: Varying Risk Levels
- Alpha Values: Multiple alpha values (80%-97%) are tested to assess portfolio performance.
  
- Constraint Adjustment: CVaR constraints are adjusted for each alpha.
  
Part 3: Visualization and Interpretation
- Bar Chart Representation: Optimal weights for different securities are visualized.
- Findings: The 5th security consistently emerges as the optimal choice across all alpha levels.


## Result and discussion


The analysis reveals how investment strategies adapt under varying constraints. The network diagram provides insights into cash flow management, while the linear programming solutions highlight optimal investment distributions. The modified Markowitz model underscores the importance of managing risk, with the 5th security dominating the portfolio, indicating a favorable risk-return balance.

## References







