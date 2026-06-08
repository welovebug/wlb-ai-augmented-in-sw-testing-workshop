# We Love Bug 2026 | AI-Augmented in Software Testing

ยินดีต้อนรับสู่ Workshop **AI-Augmented in Software Testing**

Repository นี้รวบรวม Workshop Material และ Prompt Templates สำหรับผู้เข้าร่วม Workshop ทุกท่าน

---

## สิ่งที่อยู่ใน Repository นี้

```
workshop/
├── day-1/          AI Landscape, Prompt Engineering, Test Analysis & Planning,
│                   Test Cases Design (BVA, EP, Decision Table, State Transition)
└── day-2/          E2E Test Scenarios, Test Data, Test Development,
                    Defect Report, Defect Analysis, Test Report,
                    My AI Testing Playbook

templates/
├── prompts/        Prompt Templates สำหรับแต่ละ Testing Activity
└── documents/      Document Templates (Test Scenario, Defect Report, Test Report)
```

---

## Autonomy Spectrum

Framework ที่ใช้ตลอด Workshop เพื่อจัดกลุ่ม Workflow ตามระดับการมีส่วนร่วมของ Human:

| Level | ชื่อย่อ | Human Role |
|-------|--------|-----------|
| Human-in-the-Loop | HITL | Human มีส่วนร่วมในทุกขั้นตอน AI ช่วยแต่ไม่ตัดสินใจเอง |
| Human-on-the-Loop | HOTL | AI ทำงานอัตโนมัติ Human คอย monitor และ intervene เมื่อจำเป็น |
| Human-above-the-Loop | HAbL | Human กำหนด goal และ constraint ไว้ก่อน AI ทำงานจนจบ Human review ผลลัพธ์ |
| Human-behind-the-Loop | HBtL | AI ทำงานอัตโนมัติเต็มรูปแบบ Human จะถูก consult เมื่อ AI ไม่แน่ใจหรือเกิดปัญหา |

---

## หลักการสำคัญที่ใช้ตลอด Workshop

| หลักการ | คำอธิบาย |
|---------|---------|
| **AI Drafts, Human Decides** | ทุก Output ต้องมีขั้นตอน Human Review เสมอ เพราะ AI ไม่เคยถูก 100% |
| **Prompt Iteration** | Prompt แรกไม่จำเป็นต้องสมบูรณ์ ให้ปรับไปเรื่อย ๆ จนได้ Output ที่ต้องการ |
| **Tool Comparison** | AI ต่างตัวมีจุดแข็งต่างกัน ไม่ต้องยึดติดกับตัวใดตัวหนึ่ง |
| **Context is King** | ยิ่งให้ Context ดี ยิ่งได้ Output ที่ใช้งานได้จริง |
| **PDPA Awareness** | ห้ามใส่ข้อมูลจริงของลูกค้าหรือข้อมูลที่เป็นความลับเข้า AI |

---

## สิ่งที่ได้รับกลับไปหลัง Workshop

1. **AI Review Checklist** — รายการสิ่งที่ต้อง verify โดย Human หลังได้ Output จาก AI
2. **Prompt Template Collection** — Prompt Templates พร้อมใช้สำหรับทุก Testing Activity
3. **My AI Testing Playbook** — Workflow ส่วนบุคคลของผู้เรียนแต่ละท่าน
4. **Personal Action Plan** — 3 สิ่งที่จะนำกลับไปปรับใช้ในสัปดาห์แรก

---

## AI Applications ที่ใช้ในการฝึก

ผู้เรียนจะได้เห็นว่า LLM ต่างบริษัท ให้ผลลัพธ์ต่างกัน สำหรับ Prompt เดียวกัน ซึ่งเป็นบทเรียนสำคัญ: ไม่ต้องยึดติด AI ตัวใดตัวหนึ่ง แต่เลือกใช้ให้เหมาะกับงาน

| AI Application | LLM Model |
|----------------|-----------|
| Microsoft Copilot | GPT-4o (OpenAI) |
| Github Copilot | Multi-model support |
| Claude / Claude Code | Claude Sonnet / Opus (Anthropic) |
| Google Gemini | Gemini Pro / Ultra (Google DeepMind) |

---

## AI Technology Mapping — กับ Software Testing Activities

> อ้างอิง: ISTQB Foundation Level v4.0 (2023) · WLB AI Technology Classification  
> Human must remain in the loop for all AI-assisted activities.

### ประเภทของ AI Technology

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

### 1. Test Planning & Test Monitoring / Control

| ISTQB Activity (FL v4.0) | AI Technology | Application in Testing | Example Tools / Products |
|--------------------------|---------------|----------------------|--------------------------|
| Define test objectives & scope | Generative | Extract testable objectives from requirements, user stories, and acceptance criteria | Claude, GPT-4o, Microsoft Copilot |
| Identify & analyze risks (product & project) | Predictive | Predict defect-prone modules using code complexity metrics and historical defect data | SonarQube ML, IBM Rational, custom ML |
| Estimate test effort & schedule | Predictive | ML-based effort estimation from historical sprint, project, and team velocity data | LinearB, Jira Predictive, custom ML |
| Define test approach & entry/exit criteria | Generative | Generate test strategy and definition-of-done criteria from project context | Claude, GPT-4o, Google Gemini |
| Monitor test progress (metrics & trends) | Diagnostic ML | Detect trends and early warning signals in test execution metrics across sprint cycles | Grafana ML, TestRail Analytics, Zephyr |
| Test status reporting | NLG | Auto-generate test progress reports, executive summaries, and quality dashboards | Claude, GPT-4o, Google Gemini |
| Corrective action planning | Prescriptive | Recommend resource reallocation and risk response actions from real-time test trend data | Custom Prescriptive AI, Datadog Insights |

### 2. Test Development ⚠️

> ⚠️ *Test Development* is WLB's grouping of ISTQB FL v4.0 activities: **Test Analysis + Test Design + Test Implementation**

| ISTQB Activity (FL v4.0) | AI Technology | Application in Testing | Example Tools / Products |
|--------------------------|---------------|----------------------|--------------------------|
| Analyze test basis (requirements & specs) | Generative | Extract and structure test conditions from user stories, AC, and specifications | Claude, GPT-4o, GitHub Copilot |
| Identify testability issues in requirements | Diagnostic ML | Detect ambiguous, incomplete, or conflicting requirements using NLP classification | IBM Watson, custom NLP / spaCy |
| Design test cases (EP, BVA, DT, ST) | Generative | Generate test cases aligned to ISTQB test design techniques from test conditions | Claude, GPT-4o, Testim AI |
| Design BDD / Gherkin scenarios | NLG | Convert acceptance criteria to structured Given-When-Then feature files for ATDD/BDD | Claude, GitHub Copilot, Cursor |
| Test case prioritization | Recommender | Recommend execution order by risk level, code change impact, and historical failure rate | Launchable, Sealights, custom ML |
| Test data design & generation | Generative | Synthesize realistic, diverse, PII-compliant test datasets from schema or real examples | Mostly AI, Gretel, Faker, Claude |
| Implement automated test scripts | Code Gen | Generate Playwright / Robot Framework scripts directly from test cases or manual steps | GitHub Copilot, Cursor, Claude Code |
| Test script maintenance (locator repair) | Agentic | Autonomously detect and repair broken element selectors without manual intervention | Healenium, Testim, Mabl |

### 3. Test Execution

| ISTQB Activity (FL v4.0) | AI Technology | Application in Testing | Example Tools / Products |
|--------------------------|---------------|----------------------|--------------------------|
| Test suite selection (CI/CD pipeline) | Recommender | Recommend minimal effective test subset for changed code to optimize pipeline speed | Launchable, Diffblue, Sealights |
| Visual & functional result comparison | Diagnostic ML | Visual regression — detect UI layout and pixel-level differences across builds | Applitools, Percy, Chromatic |
| Log & result anomaly detection | Anomaly Detection | Detect unusual behavior patterns in system logs and test execution output | Elastic ML, Splunk MLTK, Dynatrace |
| Defect triage & classification | Diagnostic ML | Auto-classify defect type, severity, and affected component from failure evidence | Custom ML + Jira, Zephyr AI |
| Root cause analysis | Diagnostic ML | Cluster failure patterns to identify systemic defect root causes across test runs | ELK Stack + ML, Dynatrace AI |
| Defect report generation | NLG | Auto-generate structured defect descriptions from failure screenshots and log evidence | Claude, GPT-4o, Google Gemini |
| Performance anomaly detection | Anomaly Detection | Detect performance regressions and SLA threshold violations across test runs | Dynatrace, Datadog ML, k6 + AI |
| Self-healing test execution | Agentic | Autonomously recover from broken steps and adapt to UI changes at runtime | Testim, Mabl, Healenium |

---

## License

Copyright © Siam Chamnankit Co., Ltd., Shu Ha Ri Co., Ltd. & We Love Bug Co., Ltd.

Workshop material นี้เผยแพร่ภายใต้ [Creative Commons Attribution-NonCommercial-NoDerivatives 4.0 International (CC BY-NC-ND 4.0)](LICENSE.md)

- **อนุญาต:** นำไปแชร์และใช้เพื่อวัตถุประสงค์ที่ไม่ใช่เชิงพาณิชย์ โดยต้องระบุแหล่งที่มา
- **ไม่อนุญาต:** ดัดแปลง ปรับเปลี่ยน หรือนำไปใช้เชิงพาณิชย์
