# We Love Bug | AI-Augmented in Software Testing

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

## License

Copyright © Siam Chamnankit Co., Ltd., Shu Ha Ri Co., Ltd. & We Love Bug Co., Ltd.

Workshop material นี้เผยแพร่ภายใต้ [Creative Commons Attribution-NonCommercial-NoDerivatives 4.0 International (CC BY-NC-ND 4.0)](LICENSE.md)

- **อนุญาต:** นำไปแชร์และใช้เพื่อวัตถุประสงค์ที่ไม่ใช่เชิงพาณิชย์ โดยต้องระบุแหล่งที่มา
- **ไม่อนุญาต:** ดัดแปลง ปรับเปลี่ยน หรือนำไปใช้เชิงพาณิชย์
