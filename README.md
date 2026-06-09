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

> **Capability columns**
> - **Prompt** — conversational prompting ทั่วไป (one-off)
> - **SKILL** — รองรับ structured / reusable instruction system: Claude Projects + SKILL.md · GitHub Copilot Instructions · Gemini Gems · Kiro Steering Files · Ollama Modelfile
> - **Agent** — autonomous multi-step execution: file operations, code execution, web actions, tool calling

---

### Anthropic

| AI Application | Foundation Model | Package | Prompt | SKILL | Agent |
|----------------|-----------------|---------|:------:|:-----:|:-----:|
| **Claude** (web / desktop / mobile) | Sonnet 4.x / Opus 4.x | Free · Pro $20/mo · Max $100–200/mo · Team $25/seat/mo | ✓ | ✓ | ✓ |
| **Claude Code** (CLI — agentic coding) | Sonnet 4.x / Opus 4.x | Pro ($20/mo) ขึ้นไป · API pay-per-token | ✓ | ✓ | ✓ |
| **Cowork** (desktop automation — beta) | Claude Sonnet 4.x | รวมใน Pro ขึ้นไป (beta) | ✓ | ✓ | ✓ |

### Microsoft

| AI Application | Foundation Model | Package | Prompt | SKILL | Agent |
|----------------|-----------------|---------|:------:|:-----:|:-----:|
| **Microsoft Copilot** (web / M365) | GPT-4o (OpenAI) | Free · Pro $20/mo · Microsoft 365 Copilot ~$30/seat/mo | ✓ | ✓ | ✓ |
| **GitHub Copilot** (IDE) | Multi-model: GPT-4o, Claude, Gemini | Free (2,000 completions/mo) · Pro $10/mo · Business $19/seat/mo · Enterprise $39/seat/mo | ✓ | ✓ | ✓ |

### Google

| AI Application | Foundation Model | Package | Prompt | SKILL | Agent |
|----------------|-----------------|---------|:------:|:-----:|:-----:|
| **Google Gemini** (web / mobile) | Gemini 2.5 Pro / 2.0 Flash | Free · Advanced $19.99/mo (Google One AI Premium) | ✓ | ✓ | ✓ |
| **Gemini Code Assist** (IDE) | Gemini 2.5 Pro | Free (individual) · Standard $22.80/seat/mo · Enterprise $54/seat/mo | ✓ | ✓ | ✓ |
| **Gemini API / AI Studio** | Gemini 2.5 Pro / Flash | Free tier · API pay-per-token | ✓ | ✓ | ✓ |

### Alibaba Cloud

| AI Application | Foundation Model | Package | Prompt | SKILL | Agent |
|----------------|-----------------|---------|:------:|:-----:|:-----:|
| **Qwen Chat** (web / mobile) — qwen.ai | Qwen3.7 Max / Qwen3.6-Plus | Free · Paid plans available | ✓ | — | ✓ |
| **Model Studio** (API) — alibabacloud.com | Qwen3.7 Max / Qwen3.6-Plus | API pay-per-token · Open-weight (Hugging Face) | ✓ | ✓ | ✓ |

### Moonshot AI

| AI Application | Foundation Model | Package | Prompt | SKILL | Agent |
|----------------|-----------------|---------|:------:|:-----:|:-----:|
| **Kimi Chat** (web / mobile) — kimi.ai | Kimi K2.6 — 1T MoE, 262K context | Free · Kimi Plus (paid) ¹ | ✓ | — | ✓ |
| **Kimi API** — platform.moonshot.ai | Kimi K2.6 | API pay-per-token · Open-weight (Hugging Face) ¹ | ✓ | ✓ | ✓ |

### AWS

| AI Application | Foundation Model | Package | Prompt | SKILL | Agent |
|----------------|-----------------|---------|:------:|:-----:|:-----:|
| **Kiro** (IDE) — kiro.dev | Claude Sonnet 4.x / Opus 4.x (via AWS Bedrock) | Free 50 credits/mo · Pro $20/mo · Pro+ $40/mo · Power $200/mo | ✓ | ✓ | ✓ |

### Open Source / Self-Hosted

| AI Application | Foundation Model | Package | Prompt | SKILL | Agent |
|----------------|-----------------|---------|:------:|:-----:|:-----:|
| **Ollama** (local runtime) — ollama.com | Open-weight: Llama 3, Qwen3, Kimi K2, Mistral, Gemma, DeepSeek | Free (self-hosted — ไม่มีค่ารายเดือน) | ✓ | ✓ | ✓ |

> ¹ **Kimi enterprise note:** API requests are processed on servers in China. For sensitive or confidential data, self-hosted deployment is recommended — model weights available on Hugging Face under Modified MIT License (free commercial use below 100M MAU).

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

| ISTQB Activity (FL v4.0) | AI Technology | Application in Testing | AI Applications (ที่ใช้ในการฝึก) |
|--------------------------|---------------|----------------------|----------------------------------|
| Define test objectives & scope | Generative | Extract testable objectives from requirements, user stories, and acceptance criteria | Claude, Microsoft Copilot, Google Gemini, Qwen Chat |
| Identify & analyze risks (product & project) | Predictive | Analyze requirements and test basis to surface risk indicators and high-risk areas | Claude, Kimi Chat, Google Gemini |
| Estimate test effort & schedule | Predictive | Assist effort estimation by analyzing scope, complexity, and comparable project context | Claude, Microsoft Copilot, Google Gemini |
| Define test approach & entry/exit criteria | Generative | Generate test strategy and definition-of-done criteria from project context | Claude, Microsoft Copilot, Google Gemini, Qwen Chat |
| Monitor test progress (metrics & trends) | Diagnostic ML | Analyze test execution summaries and metrics to identify trends and flag concerns | Claude, Kimi Chat, Google Gemini |
| Test status reporting | NLG | Auto-generate test progress reports, executive summaries, and quality dashboards | Claude, Microsoft Copilot, Google Gemini, Qwen Chat |
| Corrective action planning | Prescriptive | Recommend resource and priority adjustments based on test trend analysis | Claude, Microsoft Copilot, Google Gemini |

### 2. Test Development ⚠️

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

### 3. Test Execution

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

## License

Copyright © Siam Chamnankit Co., Ltd., Shu Ha Ri Co., Ltd. & We Love Bug Co., Ltd.

Workshop material นี้เผยแพร่ภายใต้ [Creative Commons Attribution-NonCommercial-NoDerivatives 4.0 International (CC BY-NC-ND 4.0)](LICENSE.md)

- **อนุญาต:** นำไปแชร์และใช้เพื่อวัตถุประสงค์ที่ไม่ใช่เชิงพาณิชย์ โดยต้องระบุแหล่งที่มา
- **ไม่อนุญาต:** ดัดแปลง ปรับเปลี่ยน หรือนำไปใช้เชิงพาณิชย์
