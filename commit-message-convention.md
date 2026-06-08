# Commit Message Convention — WLB AI-Augmented Testing

---

## 1. Purpose

เอกสารนี้กำหนดข้อตกลงการเขียน Commit Message สำหรับ Repository นี้ ซึ่งเป็น source of truth สำหรับ:

- **Workshop Material** — เนื้อหา, แบบฝึกหัด, และตัวอย่างสำหรับ Workshop ทั้ง Public และ Private
- **Prompt Templates** — Template พร้อมใช้สำหรับแต่ละ Testing Activity
- **Document Templates** — โครงสร้าง document สำหรับ Test Scenario, Defect Report, Test Report

เป้าหมายของ convention นี้:

- ทำให้ History อ่านแล้วเข้าใจได้ว่า Content เปลี่ยนไปเพราะอะไร
- แยกแยะสาเหตุ (ข้อมูลผิด vs. tool/process เปลี่ยน vs. restructure)
- ใช้ History ในการ track ว่า Workshop edition ไหนเปลี่ยนอะไร

---

## 2. Versioning

Repository นี้ใช้ **Calendar Versioning (CalVer)** รูปแบบ `YYYY.MM`:

- Version ถูก tag ใน Git เมื่อ Workshop Edition พร้อม หรือมีการเปลี่ยนแปลง Content ครั้งใหญ่
- ตัวอย่าง: `2026.06` = June 2026 edition
- ไม่ใช้ SemVer เพราะ Repository นี้ไม่มี API ที่ต้อง backward-compatible — สิ่งที่สำคัญคือ **ความเป็นปัจจุบัน** ของ content ไม่ใช่ compatibility

---

## 3. Commit Message Format

```
[Tag]: <scope> — <สรุปสิ่งที่เปลี่ยน + เหตุผลถ้าชัดจาก subject>

<body: optional — เพิ่มเมื่อ "why" ไม่ชัดจาก subject line>
```

### กฎทั่วไป

- ขึ้นต้นด้วย `[Tag]` เสมอ
- ระบุ **scope** — ชื่อ folder, section, หรือ content area ไม่ต้องเป็น full path เสมอ
  - ตัวอย่าง scope: `workshop/day-1/01-prompt-engineering`, `workshop/day-2/04-defect-report`, `templates/prompts/test-cases`, `templates/documents/test-report`, `workshop/handouts`
- เขียน Thai หรือ English ก็ได้ แต่ technical terms ให้ใช้ภาษาอังกฤษ
- เพิ่ม **body** เมื่อ subject line ยังไม่ชัดว่า "ทำไมถึงเปลี่ยน" — ดูรายละเอียดใน Section 5

---

## 4. Tags Reference

| Tag | ใช้เมื่อ | Root Cause |
|-----|---------|------------|
| `[Created]` | สร้าง file/document ใหม่ | — |
| `[Added]` | เพิ่ม section, example, หรือ content ใน document ที่มีอยู่แล้ว | — |
| `[Edited]` | Restructure หรือ reformat โดยความหมายของ content ไม่เปลี่ยน | — |
| `[Fixed]` | แก้ข้อมูลที่ผิดหรือ misleading | Content Error |
| `[Updated]` | ปรับ content เพราะ tool, model, process, หรือ framework ภายนอกเปลี่ยน | External Change |
| `[Deleted]` | ลบ file หรือ section ที่ outdated/deprecated | — |
| `[Config]` | แก้ไข repo tooling, CI, configuration | — |

### การแยกความแตกต่างระหว่าง `[Edited]`, `[Fixed]`, และ `[Updated]`

ทั้งสาม tags นี้เกี่ยวกับการแก้ไข content ที่มีอยู่แล้ว แต่ **สาเหตุต่างกัน**:

- **`[Edited]`** — Content ยังถูกต้อง แค่ restructure/reformat เช่น ปรับ heading, เรียง section ใหม่, ลด duplication
- **`[Fixed]`** — Content เดิมผิดหรือ misleading ต้องแก้ให้ถูก
- **`[Updated]`** — Content เดิมถูก แต่ tool/model/process ที่อ้างถึงเปลี่ยนไปแล้ว ต้องปรับตาม

> **สำคัญ:** การแยก `[Fixed]` กับ `[Updated]` ทำให้ track ได้ว่า Workshop เปลี่ยนเพราะ content ของเรามีข้อผิดพลาด หรือเพราะ external landscape เปลี่ยน ซึ่งมีประโยชน์ในการประเมิน maintenance effort ของแต่ละ edition

---

## 5. When to Use a Body

เพิ่ม body (เว้นบรรทัดว่าง 1 บรรทัด แล้วตามด้วยรายละเอียด) เมื่อ:

- **`[Fixed]`** — ระบุว่าข้อมูลเดิมผิดอย่างไร และถูกต้องควรเป็นอย่างไร
- **`[Updated]`** — ระบุ tool/model/process เวอร์ชันหรือ change ที่เป็นสาเหตุ
- Subject line อ่านแล้วยังไม่ชัดว่า "ทำไมถึงเปลี่ยน"

ไม่ต้องมี body เมื่อ subject line อธิบาย what + why ได้ครบแล้ว

---

## 6. Examples

### `[Created]` — สร้าง document/file ใหม่

```
[Created]: workshop/day-1/01-prompt-engineering — เพิ่มเนื้อหา Prompt Engineering พร้อม exercise และตัวอย่าง
```

```
[Created]: templates/prompts/test-cases — เพิ่ม prompt template สำหรับ BVA/EP test case generation
```

### `[Added]` — เพิ่ม content ใน document ที่มีอยู่แล้ว

```
[Added]: workshop/day-1/03-test-cases-bva-ep — เพิ่ม exercise BVA สำหรับ registration form พร้อม sample output
```

```
[Added]: workshop/day-2/01-e2e-test-scenarios — เพิ่มตัวอย่าง E2E scenario สำหรับ checkout flow แบบ HAbL workflow
```

### `[Edited]` — Restructure โดย content ไม่เปลี่ยน

```
[Edited]: workshop/day-1/02-test-analysis-planning — ปรับ structure ให้ Autonomy Spectrum อยู่ก่อน exercise เพื่อให้อ่านไหลกว่าเดิม
```

### `[Fixed]` — แก้ content ที่ผิด

```
[Fixed]: workshop/day-1/00-ai-landscape — แก้คำอธิบาย Human-on-the-Loop ที่ระบุ human role ผิด

เดิมระบุว่า human approve ทุก action แต่ HOTL หมายถึง human monitor และ intervene เมื่อจำเป็น ไม่ใช่ approve ทุกขั้นตอน
```

### `[Updated]` — ปรับตาม external change

```
[Updated]: templates/prompts/test-cases — ปรับ prompt template หลัง Claude Sonnet 4.6 เปลี่ยน behavior การ format output

เดิม prompt ระบุ format แบบ numbered list ปรับเป็น structured JSON เพื่อให้ได้ output ที่ consistent กว่าเดิม
```

```
[Updated]: workshop/day-2/03-test-development — ปรับ exercise ตาม Playwright 1.45 ที่ deprecate waitForTimeout แนะนำ waitForSelector แทน
```

### `[Deleted]` — ลบ content ที่ outdated

```
[Deleted]: workshop/handouts — ลบ handout ที่อ้างอิง ChatGPT plugins เนื่องจาก deprecated แล้ว เนื้อหาที่ยังใช้ได้รวมไว้ใน day-1 เรียบร้อย
```

### `[Config]` — แก้ repo configuration

```
[Config]: เพิ่ม .gitignore สำหรับ .DS_Store และ workshop output files
```

---

## 7. Commit Guidelines

> **หลักการ:** หนึ่ง commit ควรมี tag เดียวเท่านั้น หากต้องใช้หลาย tag ให้แยกเป็นหลาย commits เช่น ถ้าทั้ง fix content และเพิ่ม section ใหม่ ให้แยกเป็น `[Fixed]` commit หนึ่ง และ `[Added]` อีก commit หนึ่ง

---

## 8. Quick Reference Card

```
[Created]: <scope> — สร้าง document/file ใหม่สำหรับ...
[Added]:   <scope> — เพิ่ม section/content ใน...
[Edited]:  <scope> — Restructure/reformat... (meaning ไม่เปลี่ยน)
[Fixed]:   <scope> — แก้ content ที่ผิด... (+ body อธิบายว่าผิดอย่างไร)
[Updated]: <scope> — ปรับตาม tool/model/process change... (+ body ระบุ change)
[Deleted]: <scope> — ลบ... เนื่องจาก...
[Config]:  แก้ไข repo config/tooling...
```

**ทุก commit ต้องระบุ:** scope + สรุปสิ่งที่เปลี่ยน + เหตุผล (ถ้าไม่ชัดจาก subject ให้เพิ่ม body)
