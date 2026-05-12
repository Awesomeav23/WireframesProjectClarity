# Project Clarity — SOW Wireframes

This repository hosts the interactive HTML wireframes for the Project Clarity SOW creation flow.

## Files

| File | Description | Live URL |
|------|-------------|----------|
| `CREATE_SOW.html` | Full 4-step SOW wizard (Create SOW → Create Resource Plan → Create Invoicing Plan → Statement of Work document) | [Open ↗](https://awesomeav23.github.io/WireframesProjectClarity/CREATE_SOW.html) |
| `CREATE_SOW_Step1.html` | Standalone Step 1 page used for review-link sharing | [Open ↗](https://awesomeav23.github.io/WireframesProjectClarity/CREATE_SOW_Step1.html) |

---

## Changes — Tuesday, May 12 2026

### Resource Plan spreadsheet (Step 2)

- **Renamed "Hrs / Week" column to "Allocation %"** — values now display as a percentage of full-time (40 hrs/week), so 40 hrs/week reads as 100%, 20 hrs/week as 50%, etc.
- **Added custom − and + stepper buttons** on either side of each Allocation cell — each click changes the value by 10%, capped between 0 and 100. Replaced the native browser number-input spinners which weren't reliable across browsers.
- **Added a Total Hours column** between Bill Rate and Total Fees — auto-calculated as Allocation × 40 × number of weeks, read-only.
- **FLC Rate cell is now read-only and grayed out** — auto-set by Role × Location only. No other field changes it. Hovering shows a tooltip explaining why it can't be edited.
- **Bill Rate is now a pure manual input** — no longer auto-updates when Role or Location changes. The user types the customer-negotiated price directly.

### Column alignment polish

- **Bill Rate header** centered above its column.
- **Total Fees header and values** centered.
- **Total Hours values** centered in the cell, with the header label kept left-aligned (as requested).

### Rate-card calculation modal

- Added a **"How are these calculated?"** button on the mock-rate-card banner. Clicking it opens a modal that explains:
  - **FLC Rate** — formula and worked example (Salary + Benefits + Taxes + Overhead) ÷ Annual Billable Hours.
  - **Bill Rate** — clarifies that it's a manually-entered number, not derived from any formula.
  - **Total Cost** — formula and worked example (Total Hours × FLC Rate).
  - **Total Fees** — formula and worked example (Total Hours × Bill Rate).
- Fixed the FLC example math so the breakdown adds up exactly to $90/hr instead of the previous "$98 rounded to $90" misleading shortcut.

### Step 3 — Create Invoicing Plan

- **Renamed from "Invoicing Plan" to "Create Invoicing Plan"** in both the stepper label and the page title.
- Step content already contained the five-section invoicing plan (SOW Summary, Cadence, Payment Terms, Customer Billing Details, Invoice Schedule Preview) — unchanged today.

### Repository cleanup

- **Removed seven older / superseded files** from the repo: `index.html`, `login-mockup.html`, `sow-type-mockup.html`, `change-sow.html`, `invoicing-plan.html`, `change-sow-invoicing.html`, `sow-wizard-full.html`.
- The repo now contains only the two canonical wireframes (`CREATE_SOW.html` and `CREATE_SOW_Step1.html`) plus this README.

---

## Sharing the wireframe with reviewers

Send the GitHub Pages link for whichever wireframe you want them to review:

- Full 4-step flow: <https://awesomeav23.github.io/WireframesProjectClarity/CREATE_SOW.html>
- Step 1 only (Create SOW review): <https://awesomeav23.github.io/WireframesProjectClarity/CREATE_SOW_Step1.html>

Both pages include no-cache headers so reviewers always see the latest version on page load.
