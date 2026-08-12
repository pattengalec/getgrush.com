# The Grush core contract

*Extracted from one deployment wearing two costumes, not designed in advance.*

Grush overlays a management system onto a business that already exists,
the same way `GRUSH-TOOL-CONTRACT.md` overlays computed tools onto a
site's own pages. This document does the equivalent job for data: what
belongs in every deployment regardless of what the business does, and
what gets designed fresh each time.

**Read this alongside `GRUSH-TOOL-CONTRACT.md`, not instead of it.** That
document defines what a *tool* is. This one defines what a *table* is.

---

## Where this came from, and what it hasn't proven yet

Every table below is drawn directly from `lfg_*`, the Lancer Farms
schema. Desert Fog Mycology's `fgf_*` tables are structurally identical
to them — same columns, same types, same shapes. That agreement looks
like proof the split is universal. It is not, yet.

Both examples are growing operations. One grows vegetables, one grows
mushrooms, and neither has ever had to answer whether "an area" still
means the same thing to a mechanic shop's service bay or a construction
site's phase. The tool contract's own rule applies here with more force,
not less: **two is the minimum honest sample, and both samples currently
agree by resemblance, not by having been tested against something
different.**

Treat the six tables below as a strong hypothesis, confirmed once a
deployment that isn't a growing operation actually needs them. Until
then, this document describes what has held, not what has been proven.

---

## 1. The six tables that don't know what business they're in

Every deployment gets these, prefixed with its own site code —
`lfg_log`, `fgf_log`, and so on, matching the `SITE` value in that
deployment's config file. Nothing in any of these six tables assumes a
plant, a part, or a patient.

### `{site}_areas`
A place, station, or subdivision of the business. `name`, `area_type`,
`zone`, `manager`, `description`, `code`, `lat`/`lng`, `sort_order`,
`created_at`, `archived_at`.

**What's deliberately not here:** `width_ft`, `length_ft`,
`soil_depth_in`, `sun_exposure` — physical bed measurements, correct for
a farm, meaningless for a mechanic's bay. `blessing`/`blessing_ref` —
Lancer Farms' own addition, not a Grush-wide convention. Both stay out of
the template and get added back per deployment as that site's own
columns, the same way `growing_areas` already carries them today without
this contract needing to know about it.

### `{site}_log`
What happened, where, and who said so. `area_id`, `location_label`,
`note`, `logged_by`, `logged_at`, `approval_status`, `submitted_by`,
`group_id`. Already fully generic — a mechanic's "replaced brake pads on
bay 3" and a farmer's "watered bed 12" are the same row shape.

### `{site}_tasks` / `{site}_task_completions`
A recurring or one-off thing that needs doing, and the record that it
was done. `title`, `instructions`, `area_id`, `recurrence_type`,
`recurrence_days`, `recurrence_interval`, `due_date`, `priority`,
`is_core`, `color`, `howto_id(s)` on the task; `completed_by`,
`completed_at`, `visit_date`, `notes` on the completion. `season_start`/
`season_end` on the current table lean agricultural in name only — the
concept ("active window") is universal even if the column name was
chosen for a farm first.

### `{site}_inventory`
Stock on hand. `item_name`, `category`, `quantity`, `unit`, `par_level`,
`notes`, `image_url`, `updated_at`. This table needed no changes at all
to read as generic — it already is one.

### `{site}_photos`
Documentation, with consent handled as a first-class concern rather than
an afterthought. `area_id`, `caption`, `cloudinary_url`, `thumbnail_url`,
`uploaded_by`, `approval_status`, `subject_type`, `consent_public`,
`consent_recorded_by`, `consent_recorded_at`. `subject_type` is the seam
where a domain plugs in — it already exists to say what kind of thing a
photo depicts, without the table needing to know the full list.

---

## 2. The one table every business type designs for itself

Every deployment needs a **catalog**: the reference list of the things
the business works with. For a farm that's `master_plants`. For a
mechanic shop it might be `master_parts`. For a construction site,
`master_materials`. This table is never copied between deployments —
it's the one piece actually being designed each time.

### The header, which *is* shared

Looking at `master_plants` closely, most of its columns aren't about
plants at all — they're about **how an entry got into the catalog**:

```
id, category, created_at, summary, stock_image_url, source_url,
submitted_by, autofilled_at, approved_at, approval_status
```

That's the autofill-then-approve workflow from the LEARN/DO pipeline,
and it has nothing to do with botany. Every new catalog table should
start with this header, unchanged.

### The payload, which is the actual design work

Everything else in `master_plants` — `botanical_name`, `planting_windows`,
`watering_plans`, `transplant_timing`, `stage_timeline` (jsonb) — is the
part that's genuinely about plants. A parts catalog's payload would be
things like `part_number`, `compatible_models`, `install_time_est`,
`torque_spec`. A materials catalog's payload might be `unit_cost`,
`lead_time_days`, `supplier`, `spec_sheet_url`.

**This is the actual work of adding a new business type.** Everything in
§1 is reuse. This is design, and it deserves the same care
`master_plants` already got — real columns for real questions the
business asks, not a generic JSONB bucket standing in for thought.

---

## 3. Deliberately undefined

**Whether the catalog header in §2 is actually complete**, or whether a
third domain reveals a workflow field farms and mushrooms both happened
to share by coincidence. It gets adjusted the first time a real
non-growing deployment needs something the header doesn't have — not
before, and not by guessing now what that might be.

**Whether `{site}_areas`'s farm-shaped columns generalize to anything**,
or whether "physical measurements of a place" turns out to be
domain-specific in the same way the catalog payload is, just smaller.
One data point either way isn't enough to decide.

---

## Conformance checklist

A new deployment's schema conforms when:

- [ ] All six §1 tables exist, prefixed with the deployment's site code
- [ ] None of the six carry domain-specific columns beyond what's listed
      here — those go on a separate table or a deployment-specific
      addition, not baked into the shared shape
- [ ] Exactly one catalog table exists, named for what it catalogs
- [ ] The catalog's header matches §2 exactly; only the payload is new
- [ ] `SITE` in that deployment's config file matches the table prefix
      everywhere, including `grush_operators` and `grush_people` scoping
