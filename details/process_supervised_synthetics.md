# Process-Supervised Synthetics (PRM Generators)

Training and scaling models by supervising the individual steps of reasoning (process-based supervision) instead of just checking the final answer (outcome-based supervision).

## Key Advantages
1. **Hallucination Detection:** Pinpoints exactly which step went wrong.
2. **Reinforcement Alignment:** Provides step-level feedback signals for reinforcement learning.
3. **Dense Reward Signals:** Offers richer feedback compared to sparse final outcomes.

## Generation Diagram
```mermaid
graph TD
    Q[Complex Question] --> Step1[Step 1 Generation]
    Step1 --> PRM1[PRM Evaluator: Positive]
    Step1 --> Step2[Step 2 Generation]
    Step2 --> PRM2[PRM Evaluator: Negative]
    PRM2 --> Reject[Reject Path & Regenerate Step 2]
```

[Back to Main README](../README.md)
