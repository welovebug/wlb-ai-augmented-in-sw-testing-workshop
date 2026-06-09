# AI Applications Reference

Detailed breakdown of AI applications and tools used in the workshop. Learn how different vendors approach AI capabilities (Prompt, SKILL, Agent) and pricing models.

## Capability Columns

- **Prompt** — conversational prompting ทั่วไป (one-off)
- **SKILL** — รองรับ structured / reusable instruction system: Claude Projects + SKILL.md · GitHub Copilot Instructions · Gemini Gems · Kiro Steering Files · Ollama Modelfile
- **Agent** — autonomous multi-step execution: file operations, code execution, web actions, tool calling

---

## Anthropic

| AI Application | Foundation Model | Package | Prompt | SKILL | Agent |
|----------------|-----------------|---------|:------:|:-----:|:-----:|
| **Claude** (web / desktop / mobile) | Sonnet 4.x / Opus 4.x | Free · Pro $20/mo · Max $100–200/mo · Team $25/seat/mo | ✓ | ✓ | ✓ |
| **Claude Code** (CLI — agentic coding) | Sonnet 4.x / Opus 4.x | Pro ($20/mo) ขึ้นไป · API pay-per-token | ✓ | ✓ | ✓ |
| **Cowork** (desktop automation — beta) | Claude Sonnet 4.x | รวมใน Pro ขึ้นไป (beta) | ✓ | ✓ | ✓ |

---

## Microsoft

| AI Application | Foundation Model | Package | Prompt | SKILL | Agent |
|----------------|-----------------|---------|:------:|:-----:|:-----:|
| **Microsoft Copilot** (web / M365) | GPT-4o (OpenAI) | Free · Pro $20/mo · Microsoft 365 Copilot ~$30/seat/mo | ✓ | ✓ | ✓ |
| **GitHub Copilot** (IDE) | Multi-model: GPT-4o, Claude, Gemini | Free (2,000 completions/mo) · Pro $10/mo · Business $19/seat/mo · Enterprise $39/seat/mo | ✓ | ✓ | ✓ |

---

## Google

| AI Application | Foundation Model | Package | Prompt | SKILL | Agent |
|----------------|-----------------|---------|:------:|:-----:|:-----:|
| **Google Gemini** (web / mobile) | Gemini 2.5 Pro / 2.0 Flash | Free · Advanced $19.99/mo (Google One AI Premium) | ✓ | ✓ | ✓ |
| **Gemini Code Assist** (IDE) | Gemini 2.5 Pro | Free (individual) · Standard $22.80/seat/mo · Enterprise $54/seat/mo | ✓ | ✓ | ✓ |
| **Gemini API / AI Studio** | Gemini 2.5 Pro / Flash | Free tier · API pay-per-token | ✓ | ✓ | ✓ |

---

## Alibaba Cloud

| AI Application | Foundation Model | Package | Prompt | SKILL | Agent |
|----------------|-----------------|---------|:------:|:-----:|:-----:|
| **Qwen Chat** (web / mobile) — qwen.ai | Qwen3.7 Max / Qwen3.6-Plus | Free · Paid plans available | ✓ | — | ✓ |
| **Model Studio** (API) — alibabacloud.com | Qwen3.7 Max / Qwen3.6-Plus | API pay-per-token · Open-weight (Hugging Face) | ✓ | ✓ | ✓ |

---

## Moonshot AI

| AI Application | Foundation Model | Package | Prompt | SKILL | Agent |
|----------------|-----------------|---------|:------:|:-----:|:-----:|
| **Kimi Chat** (web / mobile) — kimi.ai | Kimi K2.6 — 1T MoE, 262K context | Free · Kimi Plus (paid) ¹ | ✓ | — | ✓ |
| **Kimi API** — platform.moonshot.ai | Kimi K2.6 | API pay-per-token · Open-weight (Hugging Face) ¹ | ✓ | ✓ | ✓ |

---

## AWS

| AI Application | Foundation Model | Package | Prompt | SKILL | Agent |
|----------------|-----------------|---------|:------:|:-----:|:-----:|
| **Kiro** (IDE) — kiro.dev | Claude Sonnet 4.x / Opus 4.x (via AWS Bedrock) | Free 50 credits/mo · Pro $20/mo · Pro+ $40/mo · Power $200/mo | ✓ | ✓ | ✓ |

---

## Open Source / Self-Hosted

| AI Application | Foundation Model | Package | Prompt | SKILL | Agent |
|----------------|-----------------|---------|:------:|:-----:|:-----:|
| **Ollama** (local runtime) — ollama.com | Open-weight: Llama 3, Qwen3, Kimi K2, Mistral, Gemma, DeepSeek | Free (self-hosted — ไม่มีค่ารายเดือน) | ✓ | ✓ | ✓ |

---

## Notes

> ¹ **Kimi enterprise note:** API requests are processed on servers in China. For sensitive or confidential data, self-hosted deployment is recommended — model weights available on Hugging Face under Modified MIT License (free commercial use below 100M MAU).

**Key takeaway:** Different vendors have different strengths. Tool comparison is a core principle — choose the best tool for each specific testing task, not just one tool for everything.
