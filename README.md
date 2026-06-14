# The Egress Enabler — Live Egressibility Assessor

A browser-native, single-file rebuild of the Smedberg et al. (2023) egressibility instrument. Mark each environmental barrier **compliant** or **non-compliant** and watch the Egress Enabler Score (EES) recompute live across all 14 functional limitations, then switch to **Impact mode** to see how design changes move egressibility relative to a saved baseline.

> ⚠️ This is a \*\*demonstration rebuild\*\*, not the official tool, and may differ from the published application. See \[Licensing](#licensing) and \[Disclaimer](#disclaimer).

## Features

* **Live scoring** — total EES out of the published 1314 maximum, with a per–functional-limitation breakdown and a 0–4★ rating.
* **Impact mode** — save a design as a baseline, then see the change in EES per functional limitation (greener = more egressible, redder = less).
* **Sub-scales** — add building components (e.g. "North stair, Level 2"); same-type sub-scales are weighted to sum to 1 so buildings of differing complexity stay comparable.
* **Worked example** — one click loads a populated example.
* **Export** — CSV export and Print / PDF.
* **No build, no dependencies, no server** — everything is in one HTML file. Fonts load from Google Fonts; otherwise it runs fully client-side with no tracking or data leaving the browser.

## Usage

Open `egress\_enabler\_app\_3.html` in any modern browser. That's it.

### Hosting on GitHub Pages

1. Push this repo to GitHub.
2. (Optional but tidy) rename the file to `index.html` so the tool loads at the root URL.
3. Go to **Settings → Pages**, set **Source** to your default branch and the **/(root)** folder, and save.
4. Your tool will be live at `https://<username>.github.io/<repo>/`.

## How scoring works

Each barrier item carries a 14-value scoring pattern (severity 0–4) — one value per functional limitation (A–M). Marking an item non-compliant adds its pattern to the running score for each limitation. The star rating reflects EES ÷ the published per-limitation maximum (0 issues = 4★; ≥75% of max = 0★). The 14 functional limitations classify *where* egressibility issues fall rather than describing any one individual.

## Attribution

**Rebuild by Luke de Schot.**

**Method / original instrument:** Smedberg, Slaug, Carlsson, Gefenaite, Schmidt \& Ronchi. *Disability and Health Journal* 16 (2023) 101396. The instrument (spreadsheet + user guide) is deposited on Zenodo ([10.5281/zenodo.7075501](https://doi.org/10.5281/zenodo.7075501)) under **CC BY 4.0**.

## Licensing

The original Egress Enabler instrument is deposited on Zenodo under **CC BY 4.0** (Creative Commons Attribution 4.0 International). That licence permits redistribution, reuse, and **derivative works** — including a rebuild like this one — provided the original creators are appropriately credited.

This rebuild meets that condition: the method authors are credited both in this README and in the tool's on-screen credit line. No further permission is required to host or share it.

Two minor notes:

* The **journal article** describing the instrument (the *Disability and Health Journal* paper) is open access under a Creative Commons licence that may differ from the instrument's CC BY 4.0. This rebuild reconstructs the **instrument** (the Zenodo software deposit), not the paper text, so CC BY 4.0 is the governing licence.



This README and the rebuild code are provided for demonstration and educational purposes.

## Disclaimer

Per the original authors: this instrument is intended only to supplement the informed judgment of users competent in human behaviour in fire, fire safety, human functioning, and accessibility. All results require evaluation by an informed user. This rebuild is for demonstration and may differ from the official application.

