---
permalink: /a2hd/
title: "For Students"
excerpt: "How to start research, set targets, track progress, and work effectively with Prof. Shen."
author_profile: true
---

📌 **New to the group?** Please read this page before your first meeting with Prof. Shen.  
📌 **Recruitment / admission:** <a href="/rpgadmission.html" target="_parent">Seeking self-motivated PhD students and postdoctoral fellows.</a>

---

# 0. One sentence: how we do research here
**Start from a clear target (venue + deadline + contribution), then work backward to today.**  
Every week, you should be able to answer: **(1) Where are we now? (2) What is the next bottleneck? (3) What evidence do we need for the target?**

---

# 1. Quick start (first 2–6 weeks)
## Week 0–1: Learn the area + pick an anchor
- Pick **1 anchor paper** (top venue, close to your interest).
- Reproduce or re-implement **one key figure/table** (even partially).
- Create a 1-page summary:
  - Problem + why it matters
  - Key idea
  - Experimental setup
  - What you think is weak / missing

## Week 2–3: Turn reading into a topic candidate
- Draft **3 topic candidates**, each with:
  - **Target venue** (e.g., INFOCOM / WWW / AAAI / UbiComp / etc.)
  - **One-sentence claim** (what will be new?)
  - **Baseline** (what must be beaten?)
  - **Data / system constraints** (what you can realistically run/collect)
- Choose 1 candidate to go deeper.

## Week 4–6: Produce “paper-shaped” evidence
- Deliver at least:
  - A working baseline,
  - One new idea (even small),
  - One strong figure/table that supports your claim,
  - A draft outline (titles for each section).

---

# 2. Selecting a research topic (practical checklist)
A good student topic is **not** “a cool technique”. It is a **well-defined problem + evaluation + target community**.

## 2.1 Topic selection rules (use all three)
### Rule A — Community fit
Ask: **Which research community will care?**
- Mobile/ubiquitous sensing & AIoT
- Networking / measurement / configuration
- Data mining / Web / IR
- Security & privacy
- AI / LLM / multimodal learning
- HCI / human-centered AI

### Rule B — Feasibility
Ask: **Can you finish the core evidence within 8–12 weeks of focused work?**
- If “no”, shrink the problem or scope.
- If “yes”, proceed.

### Rule C — Contribution type (be explicit)
Pick ONE primary contribution type:
- **System** (deployment / efficiency / robustness under constraints)
- **Method** (new model/algorithm)
- **Dataset/benchmark** (new data + protocol)
- **Measurement/insight** (new empirical finding)
- **Privacy/security guarantee** (threat model + protection)

---

## 2.2 The “Project Charter” (fill this before committing)
**Project title:**  
**Target venue & deadline:** (month/year)  
**Problem statement (2–3 lines):**  
**Why now / why important (1 paragraph):**  
**Your core claim (1 sentence):**  
**Evidence needed (bullets):**  
**Baselines to beat:**  
**Risks & mitigation:**  
**Week-by-week plan (next 4 weeks):**

Bring this to your meeting with Prof. Shen.

---

# 3. Target-driven planning: “Target → Backward plan → Today”
## 3.1 Set a clear target
A target should include:
- **Venue** (conference/journal)
- **Submission date** (or a realistic internal deadline)
- **Deliverable** (what “done” looks like: tables, ablations, writing)

## 3.2 Backward planning template (example for a conference submission)
Assume **T = submission date**:

- **T − 10 weeks:** problem fixed + baseline strong + pipeline stable  
- **T − 8 weeks:** main idea works + main table exists  
- **T − 6 weeks:** ablations + robustness checks + writing starts  
- **T − 4 weeks:** full draft v1 + internal review  
- **T − 2 weeks:** camera-ready quality draft + rebuttal prep  
- **T − 1 week:** freeze experiments; polish writing/figures  
- **T:** submit

**Key rule:** if you don’t know your target, you can’t plan; if you can’t plan, you can’t track progress.

---

# 4. Tracking progress (required in this group)
You are expected to maintain a lightweight “research operating system”.
This reduces confusion and makes meetings efficient.

## 4.1 After-meeting note (same day, ≤ 1 page)
Format:
- Decisions made
- Open questions
- Next actions (owner + due date)
- Risks / uncertainties

## 4.2 Weekly report (1–2 pages, every week)
Format:
- **This week’s goal** (1–2 sentences)
- **What I tried** (experiments/derivations; include links to code)
- **What happened** (numbers, plots, failures)
- **What I learned** (interpretation; what this rules out)
- **Problems / blockers** (be concrete)
- **Next week plan** (top 3 actions)
- **Critical path** (the single biggest bottleneck)

> Tip: Treat your weekly reports as future paper material (methods, results, and discussion drafts).

## 4.3 Reading template (turn papers into ideas)
For each key paper, answer:
1. **Claim:** what do they claim?
2. **Assumptions:** what must be true for it to work?
3. **Weak points:** where can it fail (data/model/setting/metrics)?
4. **Missing ablations:** what would convince you more?
5. **Your twist:** one change that fixes a weakness or expands scope.

## 4.4 “Claim → Evidence” table (use in every draft)
Make writing drive research planning:

| Claim you want to make | Evidence you already have | Evidence you still need |
|---|---|---|
| “Method improves X” | Main table | Add ablation + OOD test |
| “Method is efficient” | GPU time | Add CPU + memory + scaling |
| “Robust in the wild” | One dataset | Add new scenario / stress test |

## 4.5 Verification rule (avoid self-deception)
For each main result, produce **two independent sanity checks**:
- One “analysis-style” check (limits, bounds, simplified case, etc.)
- One “empirical-style” check (new seed/split, trivial baseline, ablation)

---

# 5. Meetings with Prof. Shen (how to make them productive)
## 5.1 Default expectations
Before the meeting (at least 24h earlier), send:
- Your **weekly report** (PDF or link)
- A 3-line agenda (what decisions you need)

During the meeting:
- Start with: **target → current status → bottleneck**
- Ask for decisions, not vague feedback:
  - “Which baseline is mandatory for the target venue?”
  - “Should we prioritize stronger experiments or clearer framing this week?”
  - “What is the fastest path to publishable evidence?”

After the meeting:
- Send the **after-meeting note** the same day.

## 5.2 If you are stuck
Come with:
- What you tried
- What failed
- Your best hypothesis why
- 2–3 options to unblock (ranked)

---

# 6. Target conferences & deadline tracking
## 6.1 Use CCFDDL to track deadlines (recommended)
Deadline trackers (pick one):
- https://ccfddl.github.io/  (main portal)
- https://ccfddl.top/       (tabular portal)

The CCFDDL project organizes conferences by category (examples):  
DS (Architecture/Storage), NW (Networks), SC (Security), SE (Software/OS), DB (DB/DM/IR), AI, HI (HCI/UbiComp), MX (Interdisciplinary).  
Always double-check the official CFP page for the final deadline.

## 6.2 Typical venues we often consider (examples, not exhaustive)
**Networking / Systems (NW):** INFOCOM, ICNP, IWQoS, SIGCOMM, IMC  
**Mobile / UbiComp / Sensing (HI):** MobiCom, MobiSys, SenSys, UbiComp/IMWUT, PerCom  
**Data Mining / Web / IR (DB):** WWW, KDD, WSDM, SIGIR, CIKM, ICDE  
**AI / ML / NLP (AI):** AAAI, IJCAI, NeurIPS, ICML, ACL, EMNLP  
**Security / Privacy (SC):** CCS, NDSS, USENIX Security, PETS

> Rule of thumb: pick **one primary venue** for a project early; it clarifies the paper style, baselines, and evaluation.

---

# 7. Credit / acknowledgement
Some of the workflow templates and research habits on this page (meeting notes, weekly reports, verification discipline, “critical path”, and “claims need evidence”, plus presentation-as-story) are inspired by **Prof. Dapeng Oliver Wu’s** public advice on research and communication:
- https://www.cs.cmu.edu/~dpwu/knowhow.html  
and were further summarized in:
- https://chatgpt.com/share/697475a5-1620-8009-b25d-1a8f0ace5f81  

We gratefully acknowledge Prof. Wu’s guidance and generosity in sharing these practices.

---

# 8. Final reminder
If you can’t answer these three questions clearly, you are not “on track” yet:
1) What is the target (venue + contribution)?  
2) What evidence is missing to reach the target?  
3) What will you do **this week** to close the biggest gap?
