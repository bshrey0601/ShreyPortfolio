# Shrey Bhatt: portfolio

Personal portfolio for Shrey Bhatt, MS Business Analytics (FinTech) candidate at Washington University in St. Louis, graduating December 2026.

**Live site:** https://bshrey0601.github.io/ShreyPortfolio/

## What is on the site

| Section | Contents |
|---|---|
| Home | Headline, focus areas, and an evidence ledger of six figures with their sources |
| About | Background, and four career directions with the work that backs each one |
| Experience | Four roles on a timeline, each with a Situation, Task, Action, Result write-up |
| Projects | Three featured projects, a filterable and searchable list of all seven, and a case study page for each |
| Skills | Six groups. A skill with a count filters the project list to the projects that use it |
| Education | Washington University in St. Louis and KSV University |
| Contact | Email, LinkedIn, GitHub, phone, and the resume as a download |

Every headline number carries a source mark:

- **Repo**: reproducible from a public repository
- **Report**: taken from a written paper or report
- **Stated**: from the resume, with no public file to check

## Projects and their sources

| Project | Code | Live demo |
|---|---|---|
| Cloud Cost Analyst | [Cloud-Cost-Analysis](https://github.com/bshrey0601/Cloud-Cost-Analysis) | [Streamlit app](https://cloud-cost-analysis-asrlr3y69dxzjzdfvifvhn.streamlit.app/) |
| M&A Deal Cracker | [M-A-deal-cracker](https://github.com/bshrey0601/M-A-deal-cracker) | [Render app](https://m-a-deal-cracker.onrender.com/) |
| Who Bears the Cost When a Bridge Fails? | Not public | None |
| Digital Payments Adoption Study | Not public | None |
| Equity Valuation: Reliance Industries | [Equity-Valuation](https://github.com/bshrey0601/Equity-Valuation) | None |
| Portfolio Risk and Performance Analysis | [Portfolio-performance-risk-analysis](https://github.com/bshrey0601/Portfolio-performance-risk-analysis) | None |
| LA Crime Analytics Dashboard | Not public | None |

## How the site is built

The site is one React page styled with Tailwind CSS. There is no framework and no server.

| File | Purpose |
|---|---|
| `source.html` | The file to edit. Holds the styles, the content and the components. |
| `index.html` | The page visitors load. Generated from `source.html`, so do not edit it by hand. |
| `build.mjs` | Compiles the JSX and the Tailwind CSS into `index.html`. |
| `404.html` | Shown by GitHub Pages for an address that does not exist. |
| `assets/` | Resume PDF, portrait, font, project screenshots and the social preview image. |

### Changing the content

All text and numbers live in the block marked `1. CONTENT` near the top of the script in `source.html`: `LINKS`, `LEDGER`, `FOCUS`, `EXPERIENCE`, `PROJECTS`, `SKILLS` and `EDUCATION`. Edit that block and rebuild.

To add a project, copy an entry in `PROJECTS`, give it a new `id`, and set `source` to `repo`, `report` or `stated`. Its case study page is created automatically at `#/projects/<id>`.

To replace the resume, overwrite `assets/Shrey_Bhatt_Resume.pdf` with the new file under the same name.

### Building

```bash
npm install
npm run build
```

Then open `index.html` in a browser, or serve the folder:

```bash
python3 -m http.server 8000
```

### Deploying

GitHub Pages serves the `main` branch. When `source.html` changes on `main`, the workflow in `.github/workflows/build.yml` rebuilds `index.html` and commits it.

## Accessibility and motion

- Works with the keyboard alone, with a visible focus ring and a skip link.
- Respects the "reduce motion" system setting: all animation is switched off.
- Charts carry a text description and a table for screen readers.

## Credits

Type is set in [Archivo](https://github.com/Omnibus-Type/Archivo), used under the SIL Open Font License 1.1.

## Contact

- Email: bshrey@wustl.edu
- LinkedIn: https://www.linkedin.com/in/shreybhatt0601
- GitHub: https://github.com/bshrey0601
