# Clari Revenue Leak Assessment — User Guide

A single-page tool (`clari-insights.html`, open it in any browser — no install needed) for turning Clari screenshots into a revenue leak diagnostic and client-ready deck. It has four tabs: **Create**, **Convert**, **Close**, and **Recommendations**.

## 1. Setup

Click the gear icon (top right) and enter your Anthropic API key. This is required to auto-extract data from screenshots and to generate AI insights/recommendations. The key is stored only in your browser's localStorage and is sent directly to the Anthropic API — never to any other server. Pick a model (Sonnet 4.6 is recommended; Opus 4.7 for max quality; Haiku 4.5 for speed).

You can skip the API key entirely and use **Enter Manually** mode on every panel instead of uploading screenshots.

## 2. Create tab

Diagnoses pipeline coverage and top-of-funnel health.

- **Pulse — Next Quarter Upload**: drop a Clari Pulse NQ screenshot (PNG/JPG/PDF/CSV) or switch to Enter Manually to type in Suggested Coverage, Current NQ, and Stage Gap directly. Enter a Team Name/Leader, then click Analyze Pulse (or Add to Results in manual mode).
- **Funnel — Conversion by Lead Source** (optional): manually enter win rate and opportunities created per lead source for a team, then Add to Results.

Results populate two tables (Coverage Ratios, Win Rate by Lead Source) plus an AI Insights panel. Use Export PDF / Export PPT to pull just this tab's results, or Clear All to reset.

## 3. Convert tab

Diagnoses stage-by-stage conversion and loss reasons.

- **Funnel — Conversion Upload**: upload a Clari Funnel screenshot or manually enter Early→Mid, Mid→Late, Late→Close conversion rates, Win Rate, and Biggest Leak Stage.
- **Loss Reason Upload**: upload a Clari loss-reason breakdown screenshot or manually enter top loss reasons. Use the same Team Name as the Funnel panel so rows match up.

Results appear in a combined conversion + top-loss-reasons table with AI Insights below it.

## 4. Close tab

Diagnoses forecast category conversion using a Clari Trend Day 30 screenshot.

- First time, define **Stages to Analyze** (e.g. Commit, Best Case) — New and Pulled In are always included automatically. Once set, stages lock in; click **Edit Stages** to change them later.
- Upload a Trend Day 30 screenshot or use Enter Manually (Total Projected Pipeline + per-category % and $ amount; leave % blank on categories like New/Pulled In to auto-calculate).

Results show forecast category conversion by team, with AI Insights.

## 5. Recommendations tab

Combines everything into a client-ready assessment.

- **Assessment Setup**: enter Company/Customer Name and Customer Segment (Large Enterprise, Small Enterprise, or Commercial) to enable benchmarking and full-deck export.
- **Revenue Leak Level**: auto-calculated against segment benchmarks (needs data from all three tabs).
- **Org-Level Top Insights** and **By Leader — Combined Insights**: synthesized findings across Create/Convert/Close.
- **Presentation Content**: click Generate with AI to draft Recommendations to Reduce Leak and Next Steps, or type your own.
- **Export Full Assessment Deck**: Export Full Deck PDF or PPT for the complete client deliverable.

Also on this tab:
- **Export Session** / **Import Session**: save all entered data as a JSON file, or reload a previous session.
- **Load Demo Data**: populate the tool with sample data to see how it works.

## Tips

- Every upload panel has an Enter Manually toggle if you don't have a screenshot or don't want to use the API.
- Data persists automatically in your browser (localStorage) between visits — use Export Session if you want a portable backup or want to hand off work to someone else.
- Use the same Team Name/Leader spelling across tabs so Recommendations can combine per-leader data correctly.
