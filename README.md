# ServUO Documentation Archive

> A community-driven, AI-assisted documentation archive for the [ServUO](https://github.com/ServUO/ServUO) Ultima Online server emulator.

---

## What This Is

This repo is a growing reference archive covering ServUO systems, scripts, commands, items, mobiles, regions, skills, gumps, and more.

New pages are written automatically on a daily schedule — one missing page per day — using an AI-assisted pipeline that reads the manifest and fills in gaps over time.

---

## Structure

```
servuo-documentation-archive/
├── README.md                    <- You are here
├── docs/
│   ├── index.md                 <- Master doc index
│   ├── systems/                 <- Core server systems
│   ├── commands/                <- Player and staff commands
│   ├── items/                   <- Item types and base classes
│   ├── mobiles/                 <- NPC and creature classes
│   ├── gumps/                   <- Gump UI systems
│   ├── regions/                 <- Region types and usage
│   ├── skills/                  <- Skill systems and handlers
│   └── misc/                    <- Everything else
├── meta/
│   ├── manifest.json            <- Master page list and status tracker
│   ├── style-guide.md           <- Page format and writing rules
│   └── prompt-contract.md      <- Daily task prompt instructions
└── .github/
    └── workflows/
        └── daily-doc.yml        <- Scheduled automation workflow
```

---

## How the Daily Pipeline Works

1. A scheduled Perplexity Task runs once per day.
2. The task reads `meta/manifest.json` to find a page with `status: "missing"`.
3. It picks one entry, writes a full Markdown documentation page for it.
4. The result is committed to the appropriate `docs/` subfolder.
5. The manifest entry is updated to `status: "done"`.
6. Repeat tomorrow.

---

## Page Status

See [`meta/manifest.json`](meta/manifest.json) for the full list of pages and their current status.

| Status | Meaning |
|---|---|
| `missing` | Page not yet written |
| `done` | Page written and committed |
| `stub` | Placeholder exists, needs expansion |

---

## Contributing

Pull requests welcome. Follow the rules in [`meta/style-guide.md`](meta/style-guide.md) when writing or editing pages.

---

## Related

- [ServUO GitHub](https://github.com/ServUO/ServUO)
- [ServUO Forums](https://www.servuo.com/)
- [Ultima Online Wikipedia](https://uo.com)
