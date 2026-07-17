# Grush — Structure

Canonical structure for the Grush umbrella and every venture nested under it.
This document is the source of truth. The site mirrors it. If something cannot
be placed in this structure, it is not ready to be built.

**Status:** structure locked · map live · intro live · function deferred
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
│       ├── Lancer Farms — deployment                            ◆ Panel
│       │      owner → Chad · site → Lancer Farms & Gardens (CBU)
│       │      status: live
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

## Spheres and the membrane

The web has a **boundary**. Not everything on the map is Grush.

```
        CBU's sphere of control    ┊         Grush
                                   ┊
   ▪ CBU ───── ▪ Lancer Farms      ┊   ● Lancer Farms ──── ● Grush software
     owner       & Gardens         ┊     deployment
                 the garden · site ┊     live
                                   ┊
                              membrane
                          ←── exchange ──→
```

**Lancer Farms is two nodes, not one.** Collapsing them repeats the owner/site
conflation at the level of the picture:

| Node | Sphere | What it is |
|---|---|---|
| **Lancer Farms & Gardens** | CBU's | the physical garden. Beds, plants, dirt. Theirs. |
| **Lancer Farms** (deployment) | Grush | the software instance running there. Chad's. |

**CBU owns Lancer Farms & Gardens and nothing else.** CBU does not own the Grush
software instance running there.

### The arbuscule — and how it is drawn

The exchange cord — garden ↔ deployment — is the **only** cord that crosses the
membrane. This is not decoration. It is what an arbuscular mycorrhiza actually is:

> The fungal hypha penetrates the root cell wall and branches inside the cell,
> but the plant's membrane **invaginates around it without breaking** — the
> periarbuscular membrane. The two organisms interpenetrate and never fuse.
> Nothing passes except what is traded across the interface.

Grush software goes inside CBU's daily operation. CBU stays CBU. Grush stays
Grush. Only value crosses.

**THE RULE: never draw the two entities merging, fusing, or entwining into one.**
Interpenetration without fusion is the whole point. The rule survives any change
of metaphor.

**The site draws this as a handshake** (built 2026-07-16), not as a cell. Grush's
hand descends in bone-white; CBU's rises in steel — the colours those entities
already wear on the map. They take hold, and gold filaments weave between the
fingers.

*Interlaced fingers do not violate the rule — they restate it.* Two hands weave
together, exchange grip, and remain two hands. You can always let go. It is the
periarbuscular membrane said in a way a stranger understands in half a second,
with no cell biology required. **They must never become one mass.**

---

## Edges

Cords have **state**, the same way nodes do.

| State | Meaning | Renders as |
|---|---|---|
| **actual** | the connection exists now | solid hypha |
| **exchange** | actual, and crosses the membrane | solid, gold — the arbuscule |
| **potential** | reaching, not yet formed | stops short of the node — a visible gap |
| **dormant** | structurally real, not active | faint dashed |

**A potential cord must not touch its node.** The gap is the honesty. It closes
only when the relationship is real.

### Current edges

| Edge | State |
|---|---|
| Grush → each venture | actual |
| fungAI ↔ Fun Guy Fungi ↔ Grush software (the loop) | actual |
| Grush software → Lancer Farms deployment | actual |
| CBU → Lancer Farms & Gardens | actual (inside CBU's own sphere) |
| **Lancer Farms & Gardens ↔ Lancer Farms deployment** | **exchange** |
| **fungAI → CBU** | **potential** |
| all three ventures → Cottages | dormant |

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

### ✓ Framing correction — done 2026-07-16

The getgrush.com repo previously asserted that Grush *is* the GC-DPS/cottages
project. `index.html` has been replaced; getgrush.com now presents the four-branch
structure and nothing links to the cottages material.

This was a **demotion, not a relocation.** `showcase.html`, `bulkhead.html`,
`offer.html`, `lab.html`, `vre/`, the narration MP3s and the badge all remain in
the repo — unlinked, unreachable unless the URL is typed directly, and recoverable
when Cottages activates. The previous `index.html` is in git history.

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
Every **first-order branch** carries one. **It is called "About" everywhere** —
not "What it is", not "About the business". Settled 2026-07-16.
Applies to: Grush software · Fun Guy Fungi · fungAI · Cottages (on waking)

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

### ◆ Gold and silver
Colour carries meaning; it is not decoration.

| Tone | Means |
|---|---|
| **gold** (`--spore`) | live. this opens a site. |
| **silver** (`--steel`) | outside Grush. no link supplied. |
| **bone** (`--mycelium`) | Grush's own. scrolls within the page. |

**Silver marks where an external owner has not handed over a link.** CBU has
supplied none, so CBU and the garden are inert — not clickable, not in the tab
order. The absence is the accurate state of the relationship, not an omission.
If CBU ever supplies a URL, that node turns gold and the map shows the
relationship change.

Corollary: **nothing self-links.** A heading that scrolls to itself is noise.
fungAI, Grush software and Cottages are plain text — none has a site of its own.

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

### The CBU angle — settled 2026-07-16

The potential fungAI ↔ CBU relationship is **AMF-assisted phytoremediation**:
arbuscular mycorrhizal fungi colonizing host plants to change how those plants
take up, stabilize, or tolerate contaminants. Established field with decades of
literature. *(Confident it exists; current state of that literature not verified
as of this writing.)*

**Hosted in CBU's garden. Not in Fun Guy Fungi's container.** This is not a
preference — biology enforces it:

- **AMF are obligate biotrophs.** No free-living stage. They cannot complete a
  life cycle without a living host root. There is no substrate block, no grain
  spawn, no fruiting chamber. Production means trap culture (living host plants
  grown for months; the roots and media *are* the inoculum) or sterile in-vitro
  root organ culture.
- **AMF work requires living plants in soil.** That is a garden. CBU has one.
- **Nobody eats AMF.** It is a soil inoculant — colonized root fragments and
  spores in a carrier. There is no food grade because there is no culinary use.
- **Edible mycorrhizal mushrooms** (porcini, matsutake, chanterelle, truffle) are
  *ecto*mycorrhizal, need living trees, and are famously near-uncultivable. Also
  not a container.

**Why this matters:** it closes the seam. None of Fun Guy Fungi's species are
mycorrhizal — oyster, lion's mane and reishi are all saprotrophic decomposers. If
the CBU work were saprotrophic remediation, the arbuscular framing on the site
would be a metaphor sitting next to organisms that don't do it. Aimed at AMF
instead, fungAI would be *doing* arbuscular symbiosis while the business
structure *is* one. The metaphor stops being a metaphor.

The separation of Fun Guy Fungi from the CBU relationship is therefore free.
Nothing about AMF work wants to be in the container. The map already draws this
correctly: the reach goes fungAI → CBU and never passes through FGF.

**Ectomycorrhizal is the wrong association** for this project: ecto partners with
trees via a sheath and a Hartig net *between* cells, never entering them. Wrong
for a garden, wrong shape for what Grush does.

---

## Open decisions

Parked deliberately. None of these change the structure — they are function,
hosting, or policy questions.

| # | Decision | Kind |
|---|---|---|
| 1 | **Cinematic intro sequence** — see spec below | build |
| 2 | Repo/domain: one repo vs. federated vs. multi-domain host (Cloudflare candidate) | hosting |
| 3 | Discount-for-testimonial as a deployment attribute | model |
| 4 | Contribution/permission rights for external owners | governance |
| 5 | Align About naming across branches ("What it is" / "About the business" / "About") | naming |
| 6 | MycoSoil public-disclosure limits (keep high-level/roadmap only) | IP |
| 7 | Research: categories vs. projects | function |
| 8 | When Cottages activates, does it get the same conventions? | structure |

### Spec — cinematic intro sequence

The map presents as a **mycorrhizal network that grows itself into the map**,
with a **skip control**. Where a boundary is crossed, the camera pushes in on a
simulated colonization.

**Two accurate scenes, matching the two cord states:**

| Scene | Cord | Biology |
|---|---|---|
| **The reach** | fungAI → CBU (potential) | Pre-symbiotic signaling. Host exudes strigolactones; fungus grows chemotropically toward the signal; fungus answers with Myc factors. **Contact has not happened.** |
| **The membrane** | garden ↔ deployment (exchange) | Colonization. Hypha presses into the cell; host membrane invaginates around it; arbuscule branches inside an unbroken wall. |

**Only one boundary is actually crossed** — the exchange cord. The reach
deliberately does not cross.

**Hard constraint: no fusion.** See "The arbuscule" above. Two entities entwining
into one would be the only lie on the page.

**Build requirements:** skip control; `prefers-reduced-motion` path; must not
wreck the page on a phone. Deserves its own session.

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
