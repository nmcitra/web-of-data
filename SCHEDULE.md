# Schedule

The archive keeps two kinds of time: a **release cadence** for the archive as a whole, and a **lifecycle** for each essay. Both live here so the dates are a record, not a memory.

---

## Release cadence

**Annual, every November 4th** — the anniversary of *Web of Data* (2024), the ur-text this archive is named for. Each release is a tagged, dated state of the whole archive: what was added, what was revised, what was newly captured from a platform.

| Release | Date | Focus |
|---|---|---|
| next | 2026-11-04 | Back-catalogue by hand (oldest obligations first) |

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

**Essays enter this archive when they are published.**

**Series.** An essay in a series carries `series: "<Name> — Part N of M"` (or the bare name when issues are unnumbered, as with Digital Gravity). kinetic-trust-protocol.net/writing reads `series`, `title`, `subtitle`, the dates, `platforms` and `cover` from every meta.yml (scripts/sync-writing-from-wod.mjs in the site repo), so a change here reaches the site on its next sync.

---

## Standing jobs

1. **Every published essay gets a canonical copy here.** Newly published pieces are captured close to publication; the back catalogue is moved by hand, oldest obligations first, not in bulk (see `README.md`).
2. **Backfill the lifecycle dates** on the pre-existing entries as they are next touched — `date_revised` and `date_edited` were added to the schema on 2026-09-19 and are not yet populated across the full back catalogue.
3. **Cut the November release** each year: review the pipeline above, capture what published since the last tag, tag the frozen state.
