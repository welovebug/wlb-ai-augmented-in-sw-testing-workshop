# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## What This Repository Is

A workshop materials scaffold for **WLB26: AI-Augmented in Software Testing** — a 2-day workshop covering AI-assisted test design, test execution, defect reporting, and test reporting. The repo ships to participants as an empty scaffold; they fill it in during and after the workshop.

There is no application code, build system, or test runner. All content is Markdown documents and prompt templates.

## Repository Structure

```
workshop/
├── day-1/   AI Landscape (00), Prompt Engineering (01), Test Analysis & Planning (02),
│            Test Cases BVA/EP (03), Decision Table (04), State Transition (05)
└── day-2/   Day-1 Review (00), E2E Test Scenarios (01), Test Data Generation (02),
             Test Development (03), Defect Report (04), Defect Analysis (05),
             Test Report (06), AI Testing Playbook (07)

templates/
├── prompts/    Reusable prompt templates per testing activity
└── documents/  Output document templates (test scenario, defect report, test report)
```

Each numbered directory currently contains only a `.gitkeep`. Workshop content (Markdown files, prompt templates, examples) goes directly inside these directories.

## Workshop Concepts to Keep in Mind

**Autonomy Spectrum** — the framework used throughout to classify AI workflows by human involvement:
- **HITL** (Human-in-the-Loop): human participates at every step
- **HOTL** (Human-on-the-Loop): AI runs autonomously, human monitors and intervenes
- **HAbL** (Human-above-the-Loop): human sets goal/constraints upfront, reviews final output
- **HBtL** (Human-behind-the-Loop): fully autonomous AI, human consulted only on uncertainty

**Core principles applied across all materials:**
- *AI Drafts, Human Decides* — every AI output requires a human review step
- *Context is King* — better context → more usable output
- *PDPA Awareness* — no real customer data or confidential information goes into AI tools

## Adding Content

- Drop `.md` files into the relevant `workshop/day-N/NN-topic/` directory
- Prompt templates belong in `templates/prompts/<activity>/`
- Document templates (fillable structures) belong in `templates/documents/<type>/`
- Remove the `.gitkeep` in a directory once real content is added
