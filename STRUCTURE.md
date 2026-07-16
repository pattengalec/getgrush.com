# Grush — Structure

Canonical structure for the Grush umbrella and every venture nested under it.
This document is the source of truth. The site mirrors it. If something cannot
be placed in this structure, it is not ready to be built.

**Status:** structure locked · function deferred
**Last updated:** 2026-07-16

---

## The web

Grush is a **web**, not a tree. Nodes appear in more than one place on purpose.
Cross-references are the design, not a defect to be normalized away.

```
Grush
│
├── Grush software                          owner → Chad
│   ├── About                               ◆ About
│   └── Deployments  (growing index)
│       ├── Lancer Farms — CBU campus garden                    ◆ Panel
│       │      owner → CBU · site → CBU campus · status: live
│       └── Fun Guy Fungi  ──────────────┐                      ◆ Panel
│              owner → Chad · site → none yet · status: in development
│                                        │
├── Fun Guy Fungi  ←─────────────────────┘  owner → Chad
│   ├── About the business                  ◆ About
│   │   ├── About FGF — what it is · what it offers · contact
│   │   └── About the owner                 ◆ Owner block
│   │       ├── Owner
│   │       └── Index of other ventures  ──┐
│   └── Grush status panel → getgrush.com   │                   ◆ Panel
│                                           │
├── fungAI  ←────────────────────────────── ┘  owner → Chad
│   ├── About                               ◆ About
│   └── Research
│       ├── Fungi as a sensor
│       ├── Fungi as an environmental remediator
│       └── Fungi as a consumable
│           ├── Culinary
│           ├── Cosmetic
│           └── Pharmaceutical
│
└── Cottages (GC-DPS)                       owner → Chad
    └── ⏸ DORMANT — see "Fourth branch" below
```

### Cords back to the top

Three links return to the umbrella. They are what make this a web:

| From | To | Mechanism |
|---|---|---|
| Grush software → Deployments | Fun Guy Fungi | the venture is also an instance |
| Any venture → owner block | Index of other ventures | the person connects them |
| Any deployment → status panel | getgrush.com | the software advertises itself |

---

## First order

Set in stone. Three active branches, three different kinds of thing.

| Branch | What it is | Role in the loop |
|---|---|---|
| **Grush software** | the product | reads and records what the organism does |
| **Fun Guy Fungi** | the operating business | grows the organism, pays the bills |
| **fungAI** | the research umbrella | generates the knowledge |

The three are a **loop**, not parallel columns:
research needs biomass → biomass gets instrumented → instrumentation produces
data → data feeds research.

---

## Fourth branch — Cottages (GC-DPS) · DORMANT

A future venture. Back burner, long term, activated when time permits.

**What it is:** a line of specialized container buildings, designed by applying
the other ventures to the buildings themselves.

**Why it is not in the loop:** the three active branches feed each other.
Cottages is **downstream of all three** — it consumes them rather than
contributing to them. It cannot be meaningfully built until the loop produces
something worth applying. This is why it can sit dormant without blocking
anything.

```
   Grush software ─┐
   Fun Guy Fungi  ─┼──→  Cottages   (applies the loop's output)
   fungAI         ─┘
```

**Existing assets — vital, do not discard:**
- Provisional patent #64/093,343 (filed 2026-06-18 · utility deadline 2027-06-18)
- Common Cottage Chassis, complete at v031
- Bulkhead design record (v032) + six open items
- UHC design, cost-build workbook, BOM
- Showcase and bulkhead explainer videos

### ⚠ Framing correction required

The **getgrush.com repo currently asserts that Grush *is* the GC-DPS/cottages
project.** That is no longer true. Grush is the umbrella; Cottages is one dormant
branch of it.

This is a **demotion, not a relocation.** The content is correct and stays where
it is. What changes is the framing above it — from *"Grush is the cottages
project"* to *"Cottages is one dormant branch of Grush."* Nothing needs to move
repos.

Until that reframing happens, the repo contains two contradictory definitions of
Grush. New structure work stays on an isolated branch until `main` is corrected.

---

## Node types

Two types fell out of the structure on their own. Type determines which
conventions a node inherits. Every new node gets tested against this.

| Type | Definition | Examples |
|---|---|---|
| **Venture** | a business under the Grush umbrella | Grush software · Fun Guy Fungi · fungAI · Cottages (dormant) |
| **Deployment** | a live instance of Grush software | Lancer Farms · Fun Guy Fungi |

A node can be both. **Fun Guy Fungi is both.** Lancer Farms is only a deployment
— it is CBU's garden, not a Grush venture — which is why it carries a Panel but
no Owner block.

---

## Conventions

Three repeating rules, three different scopes. Scope is the whole point — get it
wrong and nodes inherit blocks they should not have.

### ◆ About
Every **first-order branch** carries one.
Applies to: Grush software · Fun Guy Fungi · fungAI

### ◆ Owner block
Every **venture** carries one. Renders from the `owner` attribute — it is a slot,
not a static bio. Contains the owner, plus an index of their other ventures under
the Grush concept.
Applies to: every venture

### ◆ Panel
Every **deployment** carries a Grush-branded, near-real-time status panel that
links to getgrush.com. The farm sells the software; the software proves the farm.
The panel *is* the testimonial, running live.
Applies to: every deployment

Every deployment also carries `owner`, `site`, and `status`.

---

## Attributes

### `owner`
A **first-class entity**, not a text field. Owns the venture or deployment itself.

- May point **inward** to a node in the web (Chad)
- May point **outward** past the boundary (CBU, partners, customers)
- External owners have **permission to supply their own links** to their business
  environment, site, etc.

This gives the web a deliberate boundary: edges that leave it on purpose.

### `site`
The **physical location**. Separate from `owner` — they are not the same thing
and must not be collapsed.

A venture can exist with **no site**. Fun Guy Fungi is a mobile container garden
business awaiting a home: real business, real owner, no place yet.

> **Why the split matters:** at Fun Guy Fungi, owner and site would be the same
> person if a site existed — which is exactly why the two concepts look like one.
> At Lancer Farms they separate: CBU owns the garden. Every future customer
> deployment will separate them too.

### `status`
Applies to **deployments**. The Deployments index lists all deployments
regardless of state, each carrying its status.

| Value | Meaning |
|---|---|
| **live** | running on real ground |
| **in development** | built or building, not yet sited/operating |

> Fun Guy Fungi's software ran ahead of the farm — funguyfungi.org exists with
> zones and a floor plan for a container that is not yet physical. That is
> *proof before land, bench before container*, showing up in the structure.

### Current values

| Node | owner | site | status |
|---|---|---|---|
| Grush software | Chad | — | — |
| Fun Guy Fungi | Chad | none yet | in development |
| fungAI | Chad | — | — |
| Cottages | Chad | — | dormant |
| Lancer Farms *(deployment)* | CBU | CBU campus garden | live |

**CBU owns Lancer Farms & Gardens and nothing else.** CBU does not own the Grush
software instance running there — Chad built it. Ownership of the software is
always Chad's; `owner` on a deployment refers to the deployment's own owner.

---

## fungAI — scope

The research branch. Covers all experimental fungal research, including:

- Fungi as **organic sensors**
- Visual interpretation of signals fungi propagate through the environment
- Monitoring **mycorrhizal networks** across large geographic areas in response
  to stimulus
- Other mycological research topics

Research nests by **function** — what fungi *does*.

> **Note:** the mycelial impedance experiment is a **fungAI** project, not a Fun
> Guy Fungi one. FGF grows the organism it runs on. One project touches three
> nodes: it is a *sensor*, running on a *culinary* blue oyster, aimed at
> *remediation* monitoring.

---

## Open decisions

Parked deliberately. None of these change the structure — they are function,
hosting, or policy questions.

| # | Decision | Kind |
|---|---|---|
| 1 | Repo/domain: one repo vs. federated repos vs. multi-domain host | hosting |
| 2 | getgrush.com rendering — how the structure becomes pages | rendering |
| 3 | Discount-for-testimonial as a deployment attribute | model |
| 4 | Contribution/permission rights for external owners | governance |
| 5 | Align About naming across branches | naming |
| 6 | MycoSoil public-disclosure limits (keep high-level/roadmap only) | IP |
| 7 | Research: categories vs. projects | function |
| 8 | Reframe getgrush.com `main` — demote GC-DPS from "Grush is this" to dormant fourth branch | framing |
| 9 | When Cottages activates, does it get the same conventions (About / Owner block)? | structure |

### Known constraint
GitHub Pages binds **one custom domain per repo**. funguyfungi.org and
lancerfarms.com currently live in their own repos on their own domains. Folding
everything into one repo means those domains redirect into paths, or are dropped.
Hosts that allow multiple custom domains per project may dissolve this tradeoff —
**unverified, check current docs before committing.**

### Known requirement
The `owner` attribute is a **templating requirement** — the Owner block renders
differently per owner. GitHub Pages does not template natively beyond Jekyll.
If external owners edit their own content directly, that needs a CMS or
database-backed layer (Supabase is already in the stack). If Chad authors
everything from links they hand him, static files are sufficient.

---

## Rules of use

1. **Structure first, function later.** Do not let content decisions reshape the tree.
2. **New node?** Determine its type (venture / deployment / both). Conventions follow from type.
3. **Cannot place it?** It is not ready. Do not bolt it on.
4. **Repetition is fine.** This is a web. A node appearing twice is a cord, not an error.
