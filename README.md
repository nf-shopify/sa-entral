# SA-entral

**Rules of Engagement for Enterprise Solutions Architects**

A single-page internal site for the SA Enterprise Large team at Shopify. Built for [Quick](https://quick.shopify.io/) — Shopify's internal static site hosting platform.

**Live:** `sa-entral.quick.shopify.io`

---

## What is this?

SA-entral is the canonical reference for how SEs, AEs, and the broader sales org should engage Solutions Architects. It covers:

- **Who we are** — team roster, disciplines, leadership (NORAM + EMEA)
- **What we do** — subject matter expertise, strategic engagement, best practices, product bridge
- **When to engage** — complexity, technical depth, stakeholder alignment triggers
- **How to engage** — Ask-an-Architect channel vs. Salesforce Case Request
- **DOs and DON'Ts** — rules of engagement
- **Real examples** — scenario-based engagement patterns
- **Resources** — Architecture Diagram Library, SA Call Coaches, Solutions Architect Hub

---

## File Structure

```
sa-entral/
  index.html          ← Site (HTML + CSS + JS, renders from quick.db)
  request-sa-sf.mp4   ← Walkthrough video for Salesforce case request
  AGENTS.md           ← Quick platform API reference
  README.md           ← This file
```

---

## Data

All content lives in **quick.db** (two collections):

- **`site_config`** — one document with hero, stats, disciplines, rules, resources, etc.
- **`people`** — one document per SA with profile data (career, skills, notable deal wins)

There is no `data.json` — the site fetches everything from quick.db on load.

---

## Profile Editing

Each SA can edit their own resume brief directly on the site:

- **Identity** — Quick automatically identifies users via their Shopify Google login
- **Editable fields** — Career history, Skills, Notable Deal Wins (brand + URL + discipline tags)
- **Access** — SAs can only edit their own profile
- **Admin access** — Neilson Flemming and Will Clack can edit any team member's profile via a person-picker dropdown

The **✏️ Edit My Profile** button appears in the nav for anyone on the SA roster.

---

## Deployment

```bash
quick deploy . sa-entral
```

Confirm overwrite when prompted.

### Local preview

```bash
quick serve
```

> Note: `quick.db` and `quick.id` are only available when deployed to Quick or running via `quick serve`. The site will not load data from a plain file server.

---

## Team

**NORAM** (Neilson Flemming): Aubrey Taylor, Christian Moore, Jeannine Mizne, Richad Abuani, Ryan Pakyam, Sean Orfila

**EMEA** (Will Clack): Christian Mackie, Simon Flaherty, Mike Watt, Peter Walker, Pablo Ruiz Garcia
