# Schedule

The archive keeps two kinds of time: a **release cadence** for the archive as a whole, and a **lifecycle** for each essay. Both live here so the dates are a record, not a memory.

---

## Release cadence

**Annual, every November 4th** — the anniversary of *Web of Data* (2024), the ur-text this archive is named for. Each release is a tagged, dated state of the whole archive: what was added, what was revised, what was newly captured from a platform.

| Release | Date | Focus |
|---|---|---|
| next | 2026-11-04 | Back-catalogue by hand (oldest obligations first) + the forthcoming pipeline below, as each clears its gate |

Between releases the repository still moves — git history carries every change with its date. The November tag is the citable, frozen state.

---

## Per-essay lifecycle dates

Every `meta.yml` carries these. Any date that has not happened yet is `null`.

| field | meaning |
|---|---|
| `date_published` | first public appearance on any platform (the dir is named `YYYY-MM-DD-slug` by this date once it exists) |
| `date_revised` | last **substantive** change to the text after publication (new argument, cut section, corrected claim) |
| `date_edited` | last change of any kind, including this archive's own formatting/capture touch |
| `date_canonical` | when the essay was captured into this archive |

Git history is the fine-grained record — every commit dates a change and shows the diff. These fields are the coarse, human-readable schedule on top of it. Where a field and the git log disagree, the git log wins and the field is corrected.

**Unpublished but committed pieces** live in `forthcoming-<slug>/` with `status: forthcoming | held | planned | scheduled` and `date_published: null`. They rename to `YYYY-MM-DD-slug` on first publication. A `scheduled` piece also carries `date_scheduled`, the announced publication date; it may have no body until it ships.

**Series.** An essay in a series carries `series: "<Name> — Part N of M"` (or the bare name when issues are unnumbered, as with Digital Gravity). kinetic-trust-protocol.net/writing reads `series`, `title`, `subtitle`, the dates, `platforms` and `cover` from every meta.yml (scripts/sync-writing-from-wod.mjs in the site repo), so a change here reaches the site on its next sync.

---

## Forthcoming pipeline (committed, not yet published)

| status | essay | series | gate before publish |
|---|---|---|---|
| **scheduled · 2026-11-04** | The Loom | Different, and Held, Part 8 of 14 | publication on the anniversary |
| forthcoming | What Was Growing | Mycelium Triptych E1 | author's pass |
| planned | What It Costs | Mycelium Triptych E2 (with Denali Wilson) | drafting; co-author sign-off |
| planned | What Remains | Mycelium Triptych E3 | drafting |
| forthcoming | Softened Ground | Six Seven P2 | author's pass |
| forthcoming | What We Build | Six Seven P3 | author's pass |
| **held** | What We Plant | Six Seven P4 | **sensitivity read + upgraded cultural sources** (hózhó, Night Chant, la limpia, susto, Diné belief) — body withheld from the archive until cleared |
| forthcoming | The Cost of Exploitation Approaching Zero | standalone | author's pass |

---

## Standing jobs

1. **Every published essay gets a canonical copy here.** Newly published pieces are captured close to publication; the back catalogue is moved by hand, oldest obligations first, not in bulk (see `README.md`).
2. **Backfill the lifecycle dates** on the pre-existing entries as they are next touched — `date_revised` and `date_edited` were added to the schema on 2026-09-19 and are not yet populated across the full back catalogue.
3. **Cut the November release** each year: review the pipeline above, capture what published since the last tag, tag the frozen state.
