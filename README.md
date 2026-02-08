# Market Basket Analysis of Hospital Medication Prescriptions
## Overview
This project applies Market Basket Analysis (MBA) to uncover patterns in hospital medication co‑prescriptions. By identifying which medications are most frequently prescribed together, the analysis supports safer clinical decision‑making, optimized pharmacy inventory management, and improved visibility into prescribing behaviors.
## Business Question
Which ten medications are most frequently prescribed alongside other medications, based on antecedent–consequent relationships in patient prescription patterns?
## Goal of the Analysis
The goal is to identify the most common co‑prescribed medication pairs and evaluate their support, confidence, and lift. These insights help the hospital anticipate medication demand, detect potentially risky drug combinations, and understand treatment patterns across patient encounters.
## Data Preparation
- Loaded and cleaned the medication dataset
- Removed rows containing only null values
- Converted the dataset into a transaction list format
- Encoded transactions using TransactionEncoder

This prepared the data for Apriori‑based association rule mining.
## Association Rule Mining
- Applied the Apriori algorithm to identify frequent itemsets
- Generated association rules with lift ≥ 1 to ensure positive relationships
- Calculated support, confidence, and lift for each rule

## Top Medication Associations
The top ten rules identified:
- Have support ≥ 0.040, meaning they appear in at least 4% of all transactions
- Show confidence ≥ 0.20, indicating moderate conditional dependence
- Exhibit lift > 1.1, confirming meaningful positive associations
These patterns reflect clinically relevant co‑prescriptions rather than random pairings.
## Practical Significance
The results provide actionable insights for:
- Inventory management: Stocking commonly paired medications together
- Clinical safety: Reviewing frequent combinations for potential interactions
- Prescribing oversight: Identifying patterns that may warrant guideline updates
- Operational planning: Anticipating medication demand more accurately
Some pairs show confidence values as high as 0.45, meaning nearly half of patients prescribed one medication also receive the paired medication—an important signal for both clinical and operational teams.
## Recommendations
- Optimize pharmacy inventory by aligning stock levels with high‑support, high‑confidence medication pairs
- Establish a clinical review process to evaluate the safety and appropriateness of frequently co‑prescribed medications
- Monitor emerging patterns indicated by rules with high lift but lower support, as these may represent evolving treatment practices
