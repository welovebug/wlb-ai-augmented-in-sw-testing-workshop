# AI Technology Types Reference

Classification of AI technologies used in software testing activities (per ISTQB Foundation Level v4.0).

## AI Technology Classification

| Type | Category | Description |
|------|----------|-------------|
| **Generative** | Parent | LLM-based generation of content and test artifacts |
| **Code Gen** | └ Generative | Generates executable code (test scripts, automation) |
| **NLG** | └ Generative | Generates structured reports and natural language narratives |
| **Predictive** | Parent | Supervised ML — forecast outcomes from historical patterns |
| **Diagnostic ML** | Parent | Supervised ML — classify, detect, and explain failure patterns |
| **Anomaly Detection** | └ Diagnostic ML | Unsupervised ML — detect outliers without labeled failure categories |
| **Prescriptive** | Parent | Optimization AI — recommends actions to achieve a target outcome |
| **Recommender** | Parent | Ranking and filtering AI — surfaces the most relevant items |
| **Agentic** | Parent | Autonomous multi-step execution with goal-directed behavior |

---

## How This Classification Applies

Each AI technology type has different characteristics:

- **Generative** relies on LLMs and is best for drafting content; human review is mandatory
- **Predictive & Diagnostic** use ML models trained on historical data; accuracy depends on training data quality
- **Anomaly Detection** flags unusual patterns without requiring labeled examples; useful for discovering unknown problems
- **Recommender** ranks options by relevance; best as a starting point for human decision-making
- **Agentic** performs autonomous multi-step workflows; requires clear goals and safety constraints upfront

---

## Key Principle

> **Human must remain in the loop for all AI-assisted activities.**  
> See also: [AI-Augmented Testing Principles](../README.md#หลักการสำคัญที่ใช้ตลอด-workshop)
