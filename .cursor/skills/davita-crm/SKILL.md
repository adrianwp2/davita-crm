---
name: davita-crm
description: Guide work on the DaVita CRM email-template project in Salesforce Marketing Cloud. Use when the user mentions DaVita, CRM templates, Marketing Cloud, email blocks, journeys, Cabin, or continuing this project on another machine.
---

# DaVita CRM

This repo is the shared workspace for Cabin's DaVita CRM email-template work. The same checkout is used on more than one machine. Git is how both machines stay aligned.

## Before you start

1. Pull the latest `main`.
2. Read the PDFs in the repo root. When they disagree, follow the newest dated file.
3. Do not invent requirements the notes do not state. Say when a note is silent.

## Notes

- `2026.10.22 CRM Template Kickoff Alignment with Tessa.pdf` — kickoff with Tessa's team. Division of labor, template inventory, dark mode, and a playbook.
- `2026.10.29 CRM Design, Dev Journey Handoff.pdf` — design-system components before journey build. CKD, ESKD, and caregiver journeys. Finish development around the week of December 1, then testing.
- `2026.10.30 CRM Weekly Status.pdf` — walkthrough of the current Marketing Cloud templates and blocks.
- `2026.11.04 CRM Weekly Status.pdf` — latest decisions and next steps. Prefer this file for template scope.

## How the work is split

DaVita owns day-to-day email builds in Salesforce Marketing Cloud. Terri Anderson builds the emails. Joey Schottland leads the omnichannel side. Tessa Loughran is the DaVita lead.

Cabin (Chase Elliott, Corinne Miller, Graham Bischof) helps with template design, a playbook, and coding support for a fuller redesign. DaVita can recolor and resave existing blocks. New components that do not exist today need Cabin support.

## Template rules

- A template is a group of content blocks, not a single block.
- Terri regularly uses only 3–4 blocks. Bulleted and icon blocks are the most requested. Reduce multi-CTA and 3-column layouts.
- Keep old blocks in place during the transition. Do not delete them.
- Do not edit universal or global templates.
- Put new template work in a separate Marketing Cloud area so live campaigns are not overridden.
- Save new templates so they show up in the email catalog.
- Terri builds complex blocks in Dreamweaver, then brings them into Marketing Cloud.
- No net-new journeys until mid-Q1 at the earliest. Q1 is the rollout window. Using the new templates at the end of Q4 is optional.

## Assets

- Upload PNGs with transparent backgrounds.
- Prefer contained icons (an icon centered in a colored circle) over standalone icons.
- Terri resizes images in Photoshop. Rounded corners are coded in Salesforce, not pre-cropped into the file.
- Keep icon and crop source templates on SharePoint or MediaValet. Marketing Cloud cannot download those files back out.
- Reuse the web team's icon library inside Marketing Cloud.
- Current templates use three design elements: a hero image, smaller side images, and icons.

## Content strategy

Wait for DaVita's content-type breakdown before recommending module combinations. The two buckets are:

- Repeatable, always-on journeys
- Seasonal and ad hoc campaigns, such as open enrollment and flu

Cabin then audits the existing catalog, does light industry benchmarking, recommends blocks, and writes a playbook with assembly guidance. Keep competitive research short so it does not block template work. Stay inside normal email-client limits so deliverability does not suffer.

Emails should be shorter, with fewer calls to action, and should link out for long detail. They should match the website, including moving away from the current square blocks. Dark mode is an open problem: the Village Health logo disappears. DaVita and Village Health are separate branded areas inside Marketing Cloud.

## Journeys and the design system

For the CKD, ESKD, and caregiver journeys, put reusable components into the design system before engineering builds them. Document variants, minimum and maximum counts, and which elements are optional. One-off copy can stay out of the system. A change made in code has to be reflected in Figma. Stay async until a live sync is actually needed.

## Two machines

- Keep agent instructions in `.cursor/skills/` so the other machine gets them with the repo.
- Never commit `.env` files, credentials, tokens, or Salesforce exports that contain patient or subscriber data.
- Commit only when the user asks.
