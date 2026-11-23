# Curriculum — pre-reads and lecture scripts

Published course content. Each batch is a top-level folder (batch id from the INI sheet).

## Repository layout

```
├── README.md
├── templates/
│   ├── pre-read-template.md
│   └── lecture-script-template.md
├── <batch-id>/
│   ├── module-01-<topic>/
│   │   ├── lecture-01-<topic>/
│   │   │   ├── pre-read.md
│   │   │   ├── lecture-script.md
│   │   │   ├── data/          # optional
│   │   │   └── images/        # optional
│   │   └── ...
│   └── ...
└── ...
```

**Batches in this repo**

| Batch id |
|---|
| `IITMD-AIML-EN-I-2607` |
| `IITP-AAGI-EN-I-2611` |
| `IITP-AIDA-TA-III-2611` |
| `IITP-GAIPX-ACC-II-2610` |
| `IITP-GAIPX-TESS-II-2610` |

Module and lecture folders are created when pre-reads and lecture scripts are added.

**Folder naming (IITP-AIDA-TA-III-2611):** a lecture folder ends with `-IM` when an Industry Mentor teaches it and `-professor` when a Professor teaches it (masterclasses). Filler sessions sit under `module-00-filler-sessions/` and also end in `-IM`.

**Templates** under `templates/` are reference skeletons only.

## Curriculum CSV (local, not in this repo)

Authoring uses `.local/curricula/<batch-id>/curriculum.csv` from the INI export.
