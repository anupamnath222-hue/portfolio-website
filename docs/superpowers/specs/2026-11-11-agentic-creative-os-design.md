# Design Document: Agentic Creative Operating System Section

**Date:** 2026-11-11  
**Project:** Anupam Nath - Creative Strategist Portfolio  
**Target:** `index.html`  

---

## 1. Intent & Why
To position Anupam Nath as an AI-native Creative Director who directs autonomous agent workflows to produce direct-response creative at 10x agency velocity. Prospective DTC founders and CMOs need to see how Anupam leverages multi-agent pipelines for deep consumer research, hook ideation, and storyboarding.

---

## 2. Goals, Non-Goals, and Anti-Goals
- **Goals:**
  - Add a dedicated, interactive "Agentic Creative Operating System" section directly below the Strategic Framework.
  - Present a 3-stage agent pipeline:
    1. `Agent 01: VOC & Unvoiced Friction Mining` (Reddit, TikTok, Amazon reviews)
    2. `Agent 02: Hook & Angle Synthesis` (50+ DR angles mapped to psychological archetypes)
    3. `Agent 03: Precision Storyboard & Briefing` (Frame-by-frame creator briefs with visual pacing)
  - Allow visitors to click and inspect each agent loop to view sample agent directives, reasoning traces, and real deliverables.
  - Adhere strictly to the studio white aesthetic (`#FFFFFF` background, `#F6F7F9` cards, `#E4E7EB` borders, `#0F172A` text).
- **Non-Goals:**
  - Building a live LLM backend or requiring visitors to input API keys.
  - Creating separate multi-page routes.
- **Anti-Goals:**
  - Dark cyberpunk / neon terminal UI that breaks the premium Behance studio look.
  - Vague AI buzzwords or fictional claims.

---

## 3. Approaches Considered & Trade-offs
1. **Approach 1 (Selected):** Interactive 3-Stage Visual Pipeline Section directly on the homepage. High visibility, instant credibility, responsive, studio aesthetic.
2. **Approach 2 (Rejected):** Live Interactive Terminal Widget. Too developer-centric; risks alienating non-technical CMOs.
3. **Approach 3 (Rejected):** Standalone Vault Card. Easily overlooked by visitors skimming the top half of the portfolio.

---

## 4. Architecture & Implementation Specifics
- **Location:** Placed in `index.html` immediately following `#framework` and before `#vault`.
- **UI Components:**
  - Section Header: `AGENTIC CREATIVE OPERATING SYSTEM` + Subheading: `Autonomous agent swarms directing high-velocity direct-response creative.`
  - Pipeline Track: 3 cards showing Step Number, Agent Name, Core Directive, and Metric Lift.
  - Interactive Inspector Drawer: Clicking any card expands a live inspection drawer with 3 tabs (`Prompt & Directive`, `Subagent Trace`, `Deliverable Output`).
  - Mobile Responsiveness: Flex/Grid auto-stack with touch-friendly tap targets.
- **Code Impact:** Surgical injection of ~120 lines of HTML, ~150 lines of scoped CSS, and ~40 lines of accessible tab-switching JavaScript into `index.html`.

---

## 5. Verification Plan
1. Validate responsive layout on mobile (375px) and desktop (1440px).
2. Test tab toggling and interactive expansion across all 3 agent steps.
3. Verify zero console errors, zero broken styles, and clean HTML structure.
4. Verify Vercel deployment returns 200 OK with no styling regressions.
