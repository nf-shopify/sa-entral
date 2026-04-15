# SA-entral

**Rules of Engagement for Enterprise Solutions Architects**

A single-page internal site for the SA Enterprise Large team at Shopify. Built for [Quick](https://quick.shopify.io/) — Shopify's internal static site hosting platform.

**Live:** `sa-entral.quick.shopify.io`

## What is this?

SA-entral is the canonical reference for how SEs, AEs, and the broader sales org should engage Solutions Architects. It covers:

- **Who we are** — team roster, disciplines, leadership (NORAM + EMEA)
- **What we do** — subject matter expertise, strategic engagement, best practices, product bridge
- **When to engage** — complexity, technical depth, stakeholder alignment triggers
- **How to engage** — Ask-an-Architect channel vs. Salesforce Case Request
- **DOs and DON'Ts** — rules of engagement
- **Real examples** — scenario-based engagement patterns
- **Resources** — Architecture Diagram Library, SA Call Coaches, Solutions Architect Hub

## File Structure

```
sa-entral-quick-site/
  index.html    ← Site template (HTML + CSS + JS, renders from data.json)
  data.json     ← All site content (team, disciplines, rules, resources, etc.)
  README.md     ← This file
```

## Updating Content

All content lives in `data.json`. To update the site, edit the JSON — no HTML changes needed.

**Add a team member:**
```json
// In team.noram or team.emea array:
{ "name": "New Person", "specialty": "Storefronts", "photo": "https://cdn.shopify.com/...", "location": "US · PT (Pacific)" }
```

**Add a discipline:**
```json
// In disciplines array:
{ "icon": "🔮", "name": "New Discipline", "description": "...", "members": [...] }
```

**Update stats, resources, examples, rules** — same pattern, edit the relevant JSON key.

## Deployment

### Quick CLI
```bash
npm i -g @shopify/quick
quick deploy . sa-entral
```

### Drag & Drop
1. Go to [quick.shopify.io](https://quick.shopify.io/)
2. Drag the `sa-entral-quick-site/` folder contents onto the drop zone
3. Set subdomain to `sa-entral`

Site goes live at `sa-entral.quick.shopify.io` (Google auth, Shopify employees only).

## Design

- Dark theme inspired by [jb-resumev1.quick.shopify.io](https://jb-resumev1.quick.shopify.io/)
- Shopify green (`#00C853`) accent on near-black (`#0B0F0D`)
- CSS grid background pattern, scroll-reveal animations, count-up stats
- Fully responsive (laptop + mobile)
- Zero dependencies — vanilla HTML/CSS/JS, no build step

## Source

Inspired by the [Working with Solutions Architects](https://docs.google.com/presentation/d/17yJhuugog3MWpYS04qrjPDV5Ck36sSzqzmxLqfizoCg) deck (Salim Odero, 2025).

## Team

**NORAM** (Neilson Flemming): Aubrey Taylor, Christian Moore, Jeannine Mizne, Richad Abuani, Ryan Pakyam, Sean Orfila

**EMEA** (Will Clack): Christian Mackie, Simon Flaherty, Mike Watt, Peter Walker, Pablo Ruiz Garcia
