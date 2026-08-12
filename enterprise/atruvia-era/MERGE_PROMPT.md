# Task: port specific elements from the incoming build

A second HTML render of this same document has been added to the project. It is an **alternative build of identical content** — same study, same words, different rendering decisions.

**This project's current document is the base. It stays as it is.** Take only the elements listed below from the incoming build.

Both files are React bundles. The document content lives inside a `<script type="__bundler/template">` block, and in the incoming build also inside an embedded `<script type="text/plain" id="study-source">` block. Both are JSON/HTML-escaped — decode before working with them, and re-encode identically when writing output.

---

## Do not change

Everything in the current document not explicitly listed under "Port" stays exactly as it is:

- Page layout, grid, spacing and margins
- Typography — families, sizes, weights, line heights
- Colour palette and the treatment of evidence labels
- Table styling and rendering
- Heading hierarchy and section-opening treatments
- All body prose

**Do not reformat, restructure, re-typeset or "improve" anything.** This is a port of specific elements, not a redesign.

---

## Port from the incoming build

### 1. Five figures — replace the current CSS versions with the incoming SVG versions

These five currently render as HTML/CSS constructions. The incoming build renders them as drawn SVG. Take the SVG, including its internal labels and annotations.

| Figure | Subject | Current | Incoming |
|---|---|---|---|
| 1 | Corporate group tree — ten operating entities | CSS | **SVG — port** |
| 2 | Ownership cascade — ~700 banks → three KGs → VR-FGI → Atruvia AG | CSS | **SVG — port** |
| 3 | DORA supervisory perimeter — IBM inside, Atruvia outside | CSS | **SVG — port** |
| 4 | Two-tier customer structure — member banks / end customers | CSS | **SVG — port** |
| 15 | The closing loop — success dissolving the customer base | CSS | **SVG — port** |

**Leave alone** — already SVG in both and identical: Figure 5 (consolidation), Figure 7 (outage timeline), Figure 12 (moat matrix).

**Leave as CSS** — CSS in both: Figures 6, 8, 9, 10, 11, 13, 14.

When porting, adapt only the SVG's colour tokens to match the current palette. Do not alter its geometry, labels or proportions.

### 2. Figure captions — adopt the incoming captions for all fifteen

The incoming captions carry analysis; the current ones describe. Replace every caption with its counterpart, including for figures whose graphic is not changing.

Examples of the difference:

- Figure 2 — current: *"~700 member banks → three regional holding KGs → VR-FGI → Atruvia AG."* → incoming: *"Economic ownership is fragmented across ~700 banks; voting control is concentrated by the pooling structure into a single 91.63% block."*
- Figure 14 — current: *"Fourteen risks from the Volume V register, plotted by probability and severity."* → incoming: *"The two most severe risks — a prolonged central outage and a cyber incident — …"*
- Figure 1 — incoming adds: *"The revenue is concentrated in Ratiodata; the headcount is spread far wider than the AG's own 5,847."*

### 3. Document subtitle

The incoming build carries a subtitle beneath the main title that the current document lacks:

> *"A utility owned by the ~700 cooperative banks it serves, standing between them and …"*

Port it, in the current title typography.

### 4. Part standfirsts

The incoming build opens each of the eleven top-level Parts with a one-line standfirst; the current document goes straight from heading to body. Port all eleven, styled to match the existing section-opening treatment.

Example — Part I: *"Who owns and controls Atruvia — and how a utility owned by its own customers is governed, contracted and supervised."*

### 5. Navigation depth

The current contents list has 157 entries; the incoming one has 205. Extend to that depth, keeping the **current navigation styling and behaviour** unchanged. Add entries only — do not restyle the component.

---

## Verify before returning

The merged file must satisfy every line. Report the actual counts.

| Check | Required |
|---|---|
| Body prose | ~41,000 words — no loss |
| Tables | 53 |
| Table rows | 1,020 |
| Top-level `h1` | 11 |
| Figures | 15, all captioned |
| SVG figures | **11** (currently 3) |
| Contents entries | ≥205 |
| `CONFIRMED FACT` | 88 |
| `ANALYTICAL INFERENCE` | 63 |
| `UNKNOWN` | 65 |
| Heading anchors | all headings, all levels |

**If any count falls below the current document's, content has been lost — stop and report rather than returning a lossy file.**

Open the result and confirm the five ported SVGs render correctly, are legible at body width, and use the current palette.

---

## Optional, only if straightforward

Three figures are CSS in both builds and would be better as drawn charts with plotted axes. Do this **only** if it does not risk the merge:

- **Figure 8** — Betriebsergebnis against Digitalisierungsumlage: 2023 €40.6m / €30m · 2024 €66.6m / €60m · 2025 €89.0m / €90m. Two series, same axis.
- **Figure 10** — where one euro of revenue goes: Materialaufwand 41.2% · Personalaufwand 34.1% · Abschreibungen 11.1% · sonstige 9.7% · Betriebsergebnis 4.6%.
- **Figure 11** — Atruvia vs Finanz Informatik revenue per employee: ~€218k Group / ~€324k AG vs ~€516k.

Priority order: complete the port first, verify the counts, then attempt these.
