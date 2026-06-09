# AI Technology Mapping — ISTQB Activities

Mapping ISTQB Foundation Level v4.0 testing activities to specific AI technologies and practical workshop tools.

**References:**
- ISTQB Foundation Level v4.0 (2023)
- WLB AI Technology Classification (see [AI Technology Types](./AI-Technology-Types.md))
- **Key principle:** Human must remain in the loop for all AI-assisted activities.

---

## 1. Test Planning & Test Monitoring / Control

| ISTQB Activity (FL v4.0) | AI Technology | Application in Testing | AI Applications (ที่ใช้ในการฝึก) |
|--------------------------|---------------|----------------------|----------------------------------|
| Define test objectives & scope | Generative | Extract testable objectives from requirements, user stories, and acceptance criteria | Claude, Microsoft Copilot, Google Gemini, Qwen Chat |
| Identify & analyze risks (product & project) | Predictive | Analyze requirements and test basis to surface risk indicators and high-risk areas | Claude, Kimi Chat, Google Gemini |
| Estimate test effort & schedule | Predictive | Assist effort estimation by analyzing scope, complexity, and comparable project context | Claude, Microsoft Copilot, Google Gemini |
| Define test approach & entry/exit criteria | Generative | Generate test strategy and definition-of-done criteria from project context | Claude, Microsoft Copilot, Google Gemini, Qwen Chat |
| Monitor test progress (metrics & trends) | Diagnostic ML | Analyze test execution summaries and metrics to identify trends and flag concerns | Claude, Kimi Chat, Google Gemini |
| Test status reporting | NLG | Auto-generate test progress reports, executive summaries, and quality dashboards | Claude, Microsoft Copilot, Google Gemini, Qwen Chat |
| Corrective action planning | Prescriptive | Recommend resource and priority adjustments based on test trend analysis | Claude, Microsoft Copilot, Google Gemini |

---

## 2. Test Development ⚠️

> ⚠️ *Test Development* is WLB's grouping of ISTQB FL v4.0 activities: **Test Analysis + Test Design + Test Implementation**

| ISTQB Activity (FL v4.0) | AI Technology | Application in Testing | AI Applications (ที่ใช้ในการฝึก) |
|--------------------------|---------------|----------------------|----------------------------------|
| Analyze test basis (requirements & specs) | Generative | Extract and structure test conditions from user stories, AC, and specifications | Claude, Microsoft Copilot, Qwen Chat, Kimi Chat |
| Identify testability issues in requirements | Diagnostic ML | Review requirements for ambiguity, missing acceptance criteria, and inconsistencies | Claude, Qwen Chat, Kimi Chat |
| Design test cases (EP, BVA, DT, ST) | Generative | Generate test cases aligned to ISTQB test design techniques from test conditions | Claude, Microsoft Copilot, Google Gemini, Qwen Chat, Kimi Chat |
| Design BDD / Gherkin scenarios | NLG | Convert acceptance criteria to structured Given-When-Then feature files for ATDD/BDD | Claude, GitHub Copilot, Kiro |
| Test case prioritization | Recommender | Prioritize test cases by risk, change impact, and coverage via AI-assisted analysis | Claude, Microsoft Copilot, Google Gemini |
| Test data design & generation | Generative | Synthesize realistic, diverse, PII-safe test datasets via prompt-based generation | Claude, Qwen Chat, Ollama (sensitive data) |
| Implement automated test scripts | Code Gen | Generate Playwright / Robot Framework scripts from test cases or natural language steps | GitHub Copilot, Claude Code, Kiro |
| Test script maintenance (locator repair) | Agentic | Detect and suggest repairs for broken selectors and stale test steps | Kiro, Claude Code, GitHub Copilot |

---

## 3. Test Execution

| ISTQB Activity (FL v4.0) | AI Technology | Application in Testing | AI Applications (ที่ใช้ในการฝึก) |
|--------------------------|---------------|----------------------|----------------------------------|
| Test suite selection (CI/CD pipeline) | Recommender | Recommend test subset for changed code via AI-assisted impact analysis | Claude, GitHub Copilot, Kiro |
| Visual & functional result comparison | Diagnostic ML | Review test result screenshots and UI differences using multimodal AI analysis | Google Gemini, Claude (multimodal), Kimi Chat |
| Log & result anomaly detection | Anomaly Detection | Analyze large-scale logs and test output for error patterns using long-context AI | Kimi Chat (262K context), Claude, Google Gemini |
| Defect triage & classification | Diagnostic ML | Classify defect type, severity, and affected component via AI-assisted analysis | Claude, Microsoft Copilot, Qwen Chat, Kimi Chat |
| Root cause analysis | Diagnostic ML | Analyze failure patterns and logs to identify root causes via conversational AI | Claude, Kimi Chat (long context), Google Gemini |
| Defect report generation | NLG | Generate structured defect descriptions from failure observations and log evidence | Claude, Microsoft Copilot, Google Gemini, Qwen Chat |
| Performance anomaly detection | Anomaly Detection | Analyze JMeter / k6 test output to identify threshold violations and response time anomalies | Claude, Google Gemini, Kimi Chat |
| Self-healing test execution | Agentic | Generate fixes for broken test steps and update automation scripts | Kiro, Claude Code, GitHub Copilot |

---

## How to Use This Mapping

1. **Find your testing activity** in one of the three sections (Planning, Development, Execution)
2. **Identify the AI technology type** — understand what kind of AI will help
3. **Choose a tool** from the "AI Applications" column based on availability and capability
4. **Remember:** AI drafts, human decides — every output requires human review
