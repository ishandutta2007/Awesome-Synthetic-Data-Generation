# Tabular Synthetic Data

Tabular synthetic data replication focuses on modeling structural relational databases (like transaction databases or EHRs) while maintaining joint probabilities and correlations between columns.

## Key Methods
1. **Marginal Distribution Modeling:** Capturing individual column characteristics.
2. **Copulas and Bayesian Networks:** Modeling the dependency structure across different attributes.
3. **Conditional GANs (e.g., CTGAN):** Handling mixed-type data and imbalanced columns.

## Generation Diagram
```mermaid
graph TD
    Schema[Database Schema] --> CTGAN[Conditional Tabular GAN]
    CTGAN --> JointProb[Joint Probability Modeling]
    JointProb --> Sample[Conditional Sampling]
    Sample --> SyntheticDB[Synthetic Relational Tables]
```

[Back to Main README](../README.md)
