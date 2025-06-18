# Generate a Gantt chart easily!

Visualise your timelines in publication‑ready Gantt chart! I used this for my Ph.D. and everyone is welcome to use for any project.

---

## Features

|                          | What it does                                                                 |
| ------------------------ | ---------------------------------------------------------------------------- |
| **Simple data model**    | Task list defined in loaded from a one‑line‑per‑task CSV file.               |
| **Auto date validation** | Raises a clear error if an end date precedes its start date.                 |
| **Milestone support**    | Zero‑length tasks become diamonds (or 1‑day bars) automatically.             |
| **Flexible palettes**    | Pass any Matplotlib colormap or hard‑coded hex/HTML colours.                 |
| **Big‑figure defaults**  | Large fonts and A4/letter‑friendly figure size out of the box.               |
| **Export anywhere**      | Save as PNG, PDF, SVG, or copy paste straight up                             |

## Defining Tasks

### All you need is a .csv file called "project_tasks.csv" (included here).
#### The structure should be task,start date,end date
#### Here is an example of what it should look like:

```csv
name,start,end
Submit Aim 2 paper to Cell Genomics,2025‑06‑26,2025‑07‑07
Aim 2 revisions and publication,2025‑07‑07,2025‑09‑29
Write Aim 3 paper,2025‑06‑26,2025‑07‑26
Submit Aim 3 paper to Genome Biology,2025‑07‑26,2025‑08‑10
Aim 3 paper revisions,2025‑09‑10,2026‑01‑10
LLM project execution and publication,2025‑10‑10,2026‑01‑10
Job Search,2026‑10‑10,2026‑04‑20
```

#### You can always (once repo is cloned) click "edit" and paste your own from Excel.

---

## Customisation Tips

| Need                           | How                                                                        |
| ------------------------------ | -------------------------------------------------------------------------- |
| **Different date granularity** | Change the locator: `mdates.MonthLocator()` or `DayLocator(interval=7)`.   |
| **Milestone symbol**           | In `gantt.py`, swap the `ax.scatter(... marker="D")` for any marker style. |
| **Fonts/colours**              | Edit the `FIG_OPTS` dict at the top of the script.                         |
| **Horizontal swim‑lanes**      | Group tasks by adding a `lane` field & plotting each lane on its own Axes. |

---

## Contributing

1. Fork the repo & create your feature branch (`git checkout -b feat/awesome`)
2. Commit your changes (`git commit -am 'Add awesome feature'`)
3. Push to the branch (`git push origin feat/awesome`)
4. Open a Pull Request!

All contributions—bug fixes, doc tweaks, or entirely new features—are welcome.

---

## ⚖️ License

BSL3, Adriana Ivich 2025
