# We Love Bug 2026 | AI-Augmented in Software Testing

ยินดีต้อนรับสู่ชุดการฝึก **AI-Augmented in Software Testing**

Repository นี้รวบรวม Workshop Material และ Prompt Templates สำหรับผู้เข้าร่วม Workshop ทุกท่าน

---

## สิ่งที่อยู่ใน Repository นี้

```
workshop/
├── day-1/          (00) AI Landscape
│                   (01) Prompt Engineering
│                   (02) Test Analysis & Planning
│                   (03) Test Cases Design — BVA/EP
│                   (04) Decision Table
│                   (05) State Transition
│
└── day-2/          (00) Day-1 Review
                    (01) E2E Test Scenarios
                    (02) Test Data Generation
                    (03) Test Development
                    (04) Defect Report
                    (05) Defect Analysis
                    (06) Test Report
                    (07) My AI Testing Playbook

templates/
├── prompts/        Prompt Templates สำหรับแต่ละ Testing Activity
└── documents/      Output Templates (Test Scenario, Defect Report, Test Report)

Wiki/               Reference Material
├── AI Applications Reference          — Tool pricing & capabilities by vendor
├── AI Technology Types                — AI technology classification
└── AI Technology Mapping              — ISTQB v4.0 activities → AI technologies
                                         (See: https://github.com/welovebug/wlb-ai-augmented-in-sw-testing-workshop/wiki)
```

---

## AI Capability Levels

ผู้เรียนจะได้เรียนรู้ AI ในสามระดับตามโครงสร้าง **[agentskills.io](https://agentskills.io/home)**:

| Level | ชื่อ | ลักษณะ | Autonomy | Use Case in Testing |
|-------|------|--------|----------|----------------------|
| **Level 1** | **Prompts** | Conversational, one-off interactions | HITL (Human-in-the-Loop) | Ad-hoc test planning, quick analysis |
| **Level 2** | **SKILL** | Structured, reusable instruction systems | HOTL (Human-on-the-Loop) | Repeatable test case generation, standardized analysis |
| **Level 3** | **Agents** | Autonomous multi-step execution | HAbL/HBtL (Human-above/behind-Loop) | End-to-end test workflows, automated decision-making |

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

## AI Applications & Technology Reference

Learn how different AI vendors approach testing workflows, and map ISTQB activities to the right AI technologies and tools.

See the **[Wiki](https://github.com/welovebug/wlb-ai-augmented-in-sw-testing-workshop/wiki)** for detailed reference material:

- **[AI Applications Reference](https://github.com/welovebug/wlb-ai-augmented-in-sw-testing-workshop/wiki/AI-Applications-Reference)** — Detailed pricing, models, and capabilities (Anthropic, Microsoft, Google, Alibaba, Moonshot, AWS, Open Source)
- **[AI Technology Types](https://github.com/welovebug/wlb-ai-augmented-in-sw-testing-workshop/wiki/AI-Technology-Types)** — Classification of AI technologies (Generative, Predictive, Diagnostic, Agentic, etc.)
- **[AI Technology Mapping](https://github.com/welovebug/wlb-ai-augmented-in-sw-testing-workshop/wiki/AI-Technology-Mapping)** — ISTQB v4.0 activities mapped to AI technology types and workshop tools

**Key takeaway:** Different vendors have different strengths. Tool comparison is a core principle — choose the best tool for each testing task, not just one tool for everything.

---

## License

Copyright © Siam Chamnankit Co., Ltd., Shu Ha Ri Co., Ltd. & We Love Bug Co., Ltd.

Workshop material นี้เผยแพร่ภายใต้ [Creative Commons Attribution-NonCommercial-NoDerivatives 4.0 International (CC BY-NC-ND 4.0)](LICENSE.md)

- **อนุญาต:** นำไปแชร์และใช้เพื่อวัตถุประสงค์ที่ไม่ใช่เชิงพาณิชย์ โดยต้องระบุแหล่งที่มา
- **ไม่อนุญาต:** ดัดแปลง ปรับเปลี่ยน หรือนำไปใช้เชิงพาณิชย์
