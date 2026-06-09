# We Love Bug 2026 | AI-Augmented in Software Testing

ยินดีต้อนรับสู่ชุดการฝึก **AI-Augmented in Software Testing**

Repository นี้รวบรวม Workshop Material และ Prompt Templates สำหรับผู้เข้าร่วม Workshop ทุกท่าน

---
## สิ่งที่อยู่ใน Repository นี้

Workshop จัดโครงสร้างตามสามระดับของความสามารถ AI (Capability Levels) — ผู้เรียนจะเพิ่มพูนความสามารถขั้นต่อขั้น:

### 🎯 **Level 1: Prompts** — Conversational, One-Off Use

ผู้เรียนเรียนรู้วิธีใช้ AI ผ่านการสนทนา เพื่อวิเคราะห์ และร่างผลลัพธ์ได้ทันที

```
workshop/day-1/
├── 00-ai-landscape/           ← เข้าใจภูมิทัศน์ AI ปัจจุบัน
├── 01-prompt-engineering/     ← เรียนรู้วิธีเขียน Prompt ที่มีประสิทธิภาพ
├── 02-test-analysis-planning/ ← ใช้ Prompts วิเคราะห์ requirement
└── 03-test-cases-bva-ep/      ← ใช้ Prompts ร่างชุดทดสอบ
```

### 🔄 **Level 2: SKILL** — Structured, Reusable Systems

ผู้เรียนสร้างระบบคำสั่งที่มีโครงสร้าง (Instruction Systems) เพื่อใช้ซ้ำในงานมาตรฐาน

```
workshop/day-1/
├── 04-decision-table/         ← SKILL template สำหรับการออกแบบตามเทคนิค
└── 05-state-transition/       ← SKILL สำหรับการวิเคราะห์สถานะ

workshop/day-2/
├── 01-e2e-scenarios/          ← สร้าง Scenario ด้วย SKILL template
├── 02-test-data-generation/   ← เจนเนเรตข้อมูลทดสอบแบบเป็นระบบ
└── 03-test-development/       ← เขียน Test Script พร้อมใช้ซ้ำได้
```

### 🤖 **Level 3: Agents** — Autonomous Multi-Step Execution

ผู้เรียนสร้าง Agent เพื่อทำหลายขั้นตอนอัตโนมัติ พร้อมการตัดสินใจของ AI

```
workshop/day-2/
├── 04-defect-report/          ← Agent สำหรับแยกประเภท defect อัตโนมัติ
├── 05-defect-analysis/        ← Agent หา root cause ด้วยหลายขั้นตอน
├── 06-test-report/            ← Agent สร้างรายงาน executive summary
└── 07-my-ai-testing-playbook/ ← สังเคราะห์ Workflow ส่วนตัวจากการเรียน
```

---

### 📦 Templates & Reference

```
templates/
├── prompts/        Prompt Templates สำหรับแต่ละ Testing Activity
└── documents/      Output Templates (Test Scenario, Defect Report, Test Report)

Wiki/               Reference Material → https://github.com/welovebug/wlb-ai-augmented-in-sw-testing-workshop/wiki
├── AI Applications Reference   — Tool pricing & capabilities by vendor
├── AI Technology Types         — AI technology classification
└── AI Technology Mapping       — ISTQB v4.0 activities → AI technologies
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
