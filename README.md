# 🛡️ NEATLABS™ CHECKPOINT
### CMMC Level 2 Controls Reference — All 110. One File. No Excuses.

> *The CMMC Title 48 Rule took effect November 10, 2025. DoD contracts are now incorporating DFARS 252.204-7021. If you handle CUI, your clock is running.*

**CHECKPOINT** is a free, standalone HTML tool covering all 110 NIST SP 800-171 Rev.2 controls — the exact assessment baseline for CMMC Level 2. Every control has a plain-English explanation, the common failure points assessors actually flag, and the key evidence you need to collect. Track your implementation status, watch your SPRS readiness score build in real time, and export a full HTML + TXT readiness report.

No backend. No login. No SaaS subscription. One file, open and go.

![NEATLABS CHECKPOINT](https://img.shields.io/badge/NEATLABS™-CHECKPOINT-c8a84b?style=for-the-badge&labelColor=070c07)
![License](https://img.shields.io/badge/License-MIT-6fcf47?style=for-the-badge&labelColor=070c07)
![Controls](https://img.shields.io/badge/Controls-110%20%2F%20110-4a9c2f?style=for-the-badge&labelColor=070c07)
![Domains](https://img.shields.io/badge/Domains-14-c8a84b?style=for-the-badge&labelColor=070c07)
![SDVOSB](https://img.shields.io/badge/SDVOSB-Security%20360%2C%20LLC-a855f7?style=for-the-badge&labelColor=070c07)
![No Dependencies](https://img.shields.io/badge/Dependencies-None-06b6d4?style=for-the-badge&labelColor=070c07)

---

## 🔥 Why This Exists

Every CMMC resource on the internet either costs money, requires a login, lives in a PDF you have to cross-reference manually, or exists to sell you something.

Meanwhile, 80,000+ defense contractors need to demonstrate NIST SP 800-171 compliance — and most of them are navigating it with a spreadsheet, a government PDF, and a prayer.

CHECKPOINT changes that.

This tool is built by a practitioner with 28 years of federal cybersecurity experience, serving defense contractors daily. It reflects what actually gets contractors failed during C3PAO assessments — not just what the controls say, but what assessors look for, what documentation gaps kill scores, and what evidence maps to each requirement.

> *The most expensive CMMC gap is the one you didn't know you had. CHECKPOINT makes sure you know.*

---

## ✨ Features

**Controls & Coverage**
- All **110 controls** from NIST SP 800-171 Rev.2 — the current C3PAO assessment baseline
- All **14 domains** covered with accurate control distribution (AC:22, SC:16, IA:11...)
- **Plain-English descriptions** — what the control actually requires, not bureaucratic restatement
- **Common failure points** for every control — what assessors actually find during audits
- **Key evidence to collect** — exactly what a C3PAO wants to see for each control

**Tracking**
- **4-state status per control** — Implemented ✅ / In Progress 🔄 / Gap ❌ / N/A ⬜
- **Live SPRS readiness score** — updates as you mark controls; color shifts red → amber → green
- **Domain-level progress bars** — see at a glance where your weakest domains are
- **Sidebar domain nav** with per-domain completion percentages
- Progress **saved automatically** via `localStorage` — close and reopen without losing your work

**Filtering & Search**
- **Filter by domain** — focus on AC, SC, IA or any of the 14 domains individually
- **Filter by status** — show only gaps, only in-progress, or only completed controls
- **Filter by difficulty** — tackle Easy controls for quick wins, or focus on Hard gaps first
- **Live full-text search** — search by control ID, title, failure point, evidence type, or any keyword

**Export**
- **HTML report** — full styled readiness report with domain summary table, gap cards with failure points and evidence, complete 110-control status table, color-coded by status and difficulty
- **TXT report** — plain-text version for ticketing systems, email attachments, or record-keeping
- Both files download simultaneously with a single click
- Reports are **print-ready** (HTML report includes `@media print` CSS for clean PDF output via browser)
- **Timestamped filenames** — `neatlabs-checkpoint-cmmc-l2-YYYY-MM-DD.html`

**UX**
- **Collapse/expand domain sections** individually or all at once
- **Difficulty badges** on every control — Easy / Medium / Hard
- **NIST 800-171 Rev.2 reference** shown on every card
- Dark intelligence-dossier aesthetic with scan-line overlay and coordinate grid
- **Zero dependencies** — no npm, no build step, no internet required after initial load
- **Works completely offline** once opened

---

## 🗂️ The 14 CMMC Level 2 Domains

CMMC Level 2 = NIST SP 800-171 Rev.2. The 14 domains are identical to the 14 NIST control families.

| Code | Domain | Controls | Weight |
|---|---|:---:|---|
| **AC** | Access Control | 22 | Highest — most controls, most common gaps |
| **SC** | System & Communications Protection | 16 | High — encryption, network architecture |
| **IA** | Identification & Authentication | 11 | High — MFA requirements critical |
| **AU** | Audit & Accountability | 9 | Medium-High — logging often underdone |
| **CM** | Configuration Management | 9 | Medium-High — baselines & hardening |
| **MP** | Media Protection | 9 | Medium — encryption + sanitization |
| **MA** | Maintenance | 6 | Medium — remote maintenance MFA |
| **PE** | Physical Protection | 6 | Medium — often overlooked by IT teams |
| **CA** | Security Assessment | 4 | High impact — SSP + POA&M required |
| **SI** | System & Info Integrity | 7 | High — AV, patching, monitoring |
| **IR** | Incident Response | 3 | Medium — must be tested, not just written |
| **RA** | Risk Assessment | 3 | High — must be performed and documented |
| **PS** | Personnel Security | 2 | Easy — screening + offboarding |
| **AT** | Awareness & Training | 3 | Easy — records are the key evidence |

---

## 🚀 Quick Start

**One file. Download and open.**

```bash
# Clone the repo
git clone https://github.com/yourusername/neatlabs-checkpoint.git

# Open the tool
open neatlabs-checkpoint/neatlabs-checkpoint.html
```

Or download `neatlabs-checkpoint.html` directly and double-click it. No installation, no npm, no internet required after the Google Fonts load.

---

## 📋 How to Use CHECKPOINT for Your CMMC Assessment

### Step 1 — Understand your scope
Before marking anything, confirm which systems are in scope. CHECKPOINT covers all 110 controls but your CMMC Assessment Scope may not include every system. Use the CMMC Scoping Guide (available at dodcio.defense.gov) to define your boundary.

### Step 2 — Start with the Hard controls
Hard controls require the most lead time — documentation, tooling, process change, and organizational buy-in. Use the **Difficulty: Hard** filter to surface these first. The most common hard-control gaps:

- **3.3.3** — Audit log review processes (SIEM + active review)
- **3.5.3 / 3.5.4** — MFA for privileged AND non-privileged remote access
- **3.11.1 / 3.11.2 / 3.11.3** — Risk assessment, vulnerability scanning, remediation SLAs
- **3.12.1 / 3.12.2 / 3.12.3 / 3.12.4** — Security assessment + SSP + POA&M + continuous monitoring
- **3.13.10 / 3.13.11** — Key management + FIPS-validated cryptography
- **3.13.16** — CUI at-rest encryption

### Step 3 — Work through by domain
Use the domain sidebar to work through each family systematically. As you review each control, set status to:
- ✅ **Implemented** — control is fully in place with documented evidence
- 🔄 **In Progress** — you've started but it's not complete or documented yet
- ❌ **Gap** — not implemented; needs to go on your POA&M
- ⬜ **N/A** — genuinely not applicable to your environment (document your rationale)

### Step 4 — Collect evidence as you go
Every control card shows **Key Evidence to Collect** when you expand it. These are the artifacts a C3PAO assessor will ask for. Start collecting them now — don't wait for your assessment to discover they don't exist.

### Step 5 — Export your report
When you have a working picture of your posture, click **Export Report**. You'll get:
- An **HTML report** — domain summary table, gap cards organized by priority, full 110-control status table. Share with your CISO, your prime contractor, or your C3PAO for pre-assessment discussion.
- A **TXT report** — for ticketing systems, email threads, or record-keeping.

### Step 6 — Build your POA&M from the gaps
The HTML report's **Priority Gaps** section organizes your unimplemented Hard controls with their failure points and evidence requirements. This is the raw material for your Plan of Action & Milestones (POA&M) — required for CMMC certification.

### Step 7 — Come back quarterly
This is not a one-time activity. Your SPRS score must be updated annually. Security controls drift. Staff changes. New systems get added. Set a quarterly calendar reminder and re-run CHECKPOINT.

---

## 📤 Export Report Details

The HTML export is a full styled readiness document — not a basic dump. It includes:

### Executive Header
- SPRS readiness score with color-coded bar (red < 40%, amber < 70%, green ≥ 70%)
- Implemented / In Progress / Gap / N/A counts
- Assessment basis, enforcement date, DFARS clause reference
- Timestamped and labeled for sharing

### Domain Summary Table
All 14 domains in one scannable table showing total controls, implemented count, in-progress, gap count, and an inline progress bar per domain. Designed for executive briefings and prime contractor status reports.

### Priority Gap Cards — Hard Controls
Each unimplemented Hard control shown as a card with:
- Control ID and title
- Top 3 common failure points
- Top 3 key evidence items to collect
This section is your POA&M starting point.

### Open Gap Cards — Medium Controls
Same format, abbreviated. One failure point, one evidence item.

### Full Control Status Table
All 110 controls, organized by domain. Each control shows:
- Control ID (color-coded by domain)
- Title
- Difficulty badge
- Status badge (green/amber/red)
- For non-implemented controls: top 2 failure points and evidence items inline

### Print-Ready
The HTML report includes `@media print` CSS. Open the report, press Ctrl+P / Cmd+P, print to PDF — clean output for filing or sharing with your contracting officer.

---

## ⚡ 2025 CMMC Status — What You Need to Know

| Item | Status |
|---|---|
| CMMC Title 48 Rule | ✅ Effective November 10, 2025 |
| Required Assessment Baseline | NIST SP 800-171 **Rev.2** (not Rev.3) |
| DFARS Clause | 252.204-7021 (now in active contracts) |
| Rev.3 Requirement | Expected 2026–2027 (prepare now, don't implement yet) |
| SPRS Score Submission | Required — DFARS 252.204-7019 |
| C3PAO Assessments | Active — Cyber AB marketplace |
| Conditional Certification | Available at ≥80% score + 180-day POA&M closeout |

**Rev.2 vs Rev.3 — What to do right now:**
- CMMC Level 2 assessors benchmark against **Rev.2** — full stop
- Rev.3 (released May 2024) reorganizes controls from 110 to 97, adds 3 new families, expands ODPs
- Build your SPRS score and SSP on Rev.2; create a Rev.3 overlay for transition planning
- Do not shift your compliance program to Rev.3 before DoD formally updates CMMC — you risk failing a Rev.2 assessment

---

## 🎯 SPRS Score — What It Means

Your SPRS (Supplier Performance Risk System) score runs from **-203 to +110**.

- **+110** = all 110 controls fully implemented
- **0** = starting point with no implementation
- **Negative scores** = calculated by subtracting weighted point values for unimplemented controls
- **DoD threshold** = no hard floor published, but scores below 70 create significant contract risk
- **Conditional certification** = requires ≥80% + active POA&M

CHECKPOINT's "SPRS Readiness Score" shows how many controls you have marked as Implemented — it's a readiness indicator, not a formal SPRS score. Your official score must be calculated using the DoD Assessment Methodology (v1.2.1) and submitted via the SPRS portal by a qualified assessor or your senior official for self-assessment paths.

---

## 📁 File Structure

```
neatlabs-checkpoint/
├── neatlabs-checkpoint.html    # The entire tool — one file
└── README.md                   # This file
```

One HTML file. Everything runs in your browser locally. No dependencies, no build step, no server.

---

## 🏗️ Technical Notes

**Data accuracy:** All 110 controls are sourced from NIST SP 800-171 Rev.2. Control IDs, domain assignments, and control counts match the official publication exactly:

```
AC:22 · AT:3 · AU:9 · CM:9 · IA:11 · IR:3 · MA:6
MP:9  · PS:2 · PE:6 · RA:3 · CA:4  · SC:16 · SI:7
Total: 110
```

**Storage:** Status selections persist via `localStorage` under the key `ckpt-status`. Clearing your browser data will reset progress. For shared or team use, export your report before clearing browser storage.

**Offline use:** After the initial page load (which fetches Google Fonts), CHECKPOINT works with no internet connection. For fully air-gapped use, replace the Google Fonts `<link>` with locally hosted font files.

**Browser support:** Any modern browser (Chrome, Firefox, Safari, Edge). No IE support.

---

## 🤝 Contributing

CHECKPOINT is designed to be accurate, current, and practitioner-grade. Contributions that improve accuracy or add value are welcome.

**To contribute a control update:**

1. Fork the repo
2. Find the control in the `CONTROLS` array in `neatlabs-checkpoint.html`
3. Update the relevant field:

```javascript
{
  id: '3.x.x',              // NIST SP 800-171 Rev.2 control ID — do not change
  domain: 'XX',             // Two-letter domain code — do not change
  title: 'Control Title',   // Short plain-English title
  diff: 'easy',             // 'easy' | 'medium' | 'hard'
  desc: 'What this control requires in plain English...',
  failures: [
    'Specific failure pattern assessors find',
    'Another common gap',
    'Third failure mode',
    'Fourth failure mode (optional)',
  ],
  evidence: [
    'Specific artifact that satisfies this control',
    'Second evidence type',
    'Third evidence type',
  ]
}
```

4. Submit a pull request with a note on what you changed and why

**Contribution guidelines:**
- `failures` entries must describe real-world audit findings — not theoretical gaps
- `evidence` entries must be specific artifacts (policy name, configuration type, log type) — not generic descriptions
- `diff` ratings: Easy = documentation/config that most orgs can do in days, Medium = requires process or tooling change, Hard = requires significant architectural change, specialized tooling, or organizational commitment
- No changes to control IDs or domain assignments — these are fixed by NIST
- If a control's plain-English description is inaccurate, cite the NIST SP 800-171 Rev.2 text in your PR

**What we need most:**
- Updated failure points based on recent C3PAO assessment findings
- Additional evidence examples for hard controls
- Rev.3 crosswalk data (for future Rev.3 transition planning features)

---

## 🌐 More from NEATLABS™

CHECKPOINT is part of the NEATLABS™ free tool suite. All tools are single-file HTML, no login, no tracking.

**→ [neatlabs.ai](https://neatlabs.ai)**

| Tool | Description |
|---|---|
| **CHECKPOINT** | This tool — CMMC Level 2 controls reference and readiness tracker |
| **DATABROKER ATLAS** | 35+ data broker opt-out directory with verified links and progress tracker |
| **VANTAGE** | Expert intelligence discovery — the right cybersecurity people to follow on LinkedIn |
| **Blast Radius** | Comprehensive data broker exposure analysis |
| **ToS/Policy Analyzer** | AI-powered analysis of privacy policies and terms of service |
| **SSP Manager Professional** | System Security Plan documentation and management |
| **CMMC Compliance Suite** | Full CMMC Level 2 compliance platforms for defense contractors |

---

## 📚 Additional Resources

**Official CMMC & NIST:**
- **CMMC Model Overview v2.0** — [dodcio.defense.gov](https://dodcio.defense.gov/CMMC/)
- **NIST SP 800-171 Rev.2 PDF** — [csrc.nist.gov](https://csrc.nist.gov/pubs/sp/800/171/r2/upd1/final)
- **CMMC Assessment Guide Level 2** — dodcio.defense.gov/Portals/0/Documents/CMMC/AssessmentGuideL2v2.pdf
- **SPRS Portal** — [sprs.csd.disa.mil](https://sprs.csd.disa.mil)
- **Cyber AB C3PAO Marketplace** — [cyberab.org](https://cyberab.org)

**Assessment Methodology:**
- **DoD Assessment Methodology v1.2.1** — Required for calculating official SPRS scores
- **CMMC Scoping Guide Level 2** — For defining your assessment boundary
- **NIST SP 800-171A** — Assessment procedures for evaluating control implementation

**Planning:**
- **NIST SP 800-171 Rev.3** — May 2024 final version (not yet required for CMMC; plan for transition)
- **NIST SP 800-172** — Enhanced requirements used for CMMC Level 3

---

## ⚠️ Disclaimer

NEATLABS™ CHECKPOINT is provided by **Security 360, LLC** for informational and educational purposes only.

- This tool is based on NIST SP 800-171 Revision 2. Control descriptions are plain-English interpretations and **do not replace** the official NIST SP 800-171 publication or the CMMC Assessment Guide Level 2.
- **The SPRS readiness score shown is an internal indicator only.** It is not a formal SPRS score and does not constitute a CMMC assessment result. Your official SPRS score must be calculated using the DoD Assessment Methodology (v1.2.1) and submitted via the SPRS portal.
- **This tool is not legal or compliance advice.** CMMC compliance has legal and contractual implications. Consult qualified legal counsel, a Registered Practitioner (RP), or an accredited C3PAO for your specific situation.
- NEATLABS™ is not affiliated with the Department of Defense, NIST, the Cyber AB, or any C3PAO.
- Control requirements and enforcement status may change as DoD updates CMMC rules. Always verify current requirements at [dodcio.defense.gov](https://dodcio.defense.gov/CMMC/).

---

## 📄 License

MIT — free to use, fork, modify, and redistribute. Attribution appreciated but not required.

If CHECKPOINT helped you find gaps before your assessor did, consider starring the repo. It helps other defense contractors find it.

---

## 🏢 About NEATLABS™ / Security 360, LLC

**NEATLABS™** is the innovation brand of **Security 360, LLC**, a Service-Disabled Veteran-Owned Small Business (SDVOSB) with a Top Secret Facility Clearance, specializing in:

- **CMMC compliance** — Level 2 and Level 3 preparation, C3PAO-ready documentation, SSP and POA&M development
- **Fractional CISO services** — for defense contractors who need executive security leadership without a full-time hire
- **Cybersecurity architecture** — zero-trust implementation, network segmentation, FIPS-validated cryptography
- **Supply chain risk management** — vendor vetting, subcontractor CMMC flow-down requirements
- **AI-powered security tooling** — custom compliance platforms, OSINT tools, threat intelligence systems
- **Federal contracting cybersecurity** — DFARS compliance, CDI/CUI scoping, SPRS score development

With 28+ years of federal cybersecurity experience, Security 360 brings practitioner-grade expertise to every engagement — and builds free tools like this one because every contractor in the DIB deserves a fair shot at compliance.

**→ [neatlabs.ai](https://neatlabs.ai)** for tools, consulting, and professional services.  
**→ Security 360, LLC · VOSB **

---

*Built by practitioners, for practitioners.*  
*No ads. No tracking. No upsell. Just signal.*

**[⭐ Star this repo if CHECKPOINT helped you find a gap before your C3PAO did]**
