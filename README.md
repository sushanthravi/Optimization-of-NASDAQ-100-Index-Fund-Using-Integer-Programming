# Optimization-of-NASDAQ-100-Index-Fund-Using-Integer-Programming
In this project, we are constructing an **Index Fund** that tracks the **NASDAQ-100 index** using **Integer Programming (IP)**.

## Project: Optimization of NASDAQ-100 Index Fund Using Integer Programming

The goal is to select a subset of stocks from the index that can closely replicate the index’s performance, while minimizing transaction and rebalancing costs. The steps involve stock selection, portfolio weight optimization, and evaluating the tracking accuracy across different portfolio sizes.

### Key Steps:

1. **Stock Selection**:
   - We formulated an **integer programming** model to select **m stocks** from the NASDAQ-100. The selection is based on maximizing the similarity (measured by a correlation matrix) between the selected stocks and the entire index.

2. **Portfolio Weights**:
   - After selecting the stocks, we solved a **linear programming** problem to determine the optimal portfolio weights, minimizing the tracking error between the portfolio and the index returns.

3. **Portfolio Evaluation**:
   - The selected portfolio is tested on **out-of-sample data** (2024) to evaluate how closely it tracks the NASDAQ-100 index, based on the stock selections and weight optimizations from the **in-sample data** (2023).

4. **Incremental Analysis**:
   - We repeated the process for different values of **m** (e.g., 5, 10, 20, ..., 100) to assess whether increasing the number of selected stocks improves tracking accuracy or results in diminishing returns.

5. **Mixed-Integer Programming**:
   - We also explored an alternative method by solving the portfolio optimization problem directly using **Mixed-Integer Programming (MIP)**, constraining the number of non-zero weights to **m stocks**.

6. **Out-of-Sample Testing**:
   - The performance of the portfolio constructed from 2023 data is tested on the 2024 data, with tracking accuracy measured by comparing the index and portfolio returns over time.

7. **Final Recommendations**:
   - Based on the analysis, we provide recommendations on the optimal number of stocks for constructing an efficient index fund, balancing accuracy with cost efficiency.

### Tools and Techniques:
- **Gurobi Optimizer**: To solve the integer and linear programming models.
- **Python**: Used for implementing optimization models, data handling, and portfolio performance analysis.

### Conclusion:
This project demonstrates the use of **integer programming** and **linear programming** to construct an index fund that tracks the NASDAQ-100, evaluating trade-offs between tracking accuracy and the number of selected stocks.
