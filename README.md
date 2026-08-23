# CAST/FORM — Alloying bench

A self-contained, browser-only alloying calculator for a jewellery casting workshop, branded with the supplied **TJ Hand Crafted** logo.

## What is included

- Gold recipes for common UK / US / Australia / New Zealand carat and fineness families:
  - 9 ct / 375, 10K / 417, 14K / 585, 18 ct / 750, 22K / 916, 24 ct / 999
  - yellow, rose, palladium / nickel-free white, nickel white, green and a clearly marked purple speciality recipe
- Platinum families:
  - Pt950Co, Pt950Ru, Pt900Ir, Pt950Ir, Pt950Cu, Pt950Pd and Pt900Pd
- Batch calculations in grams, pennyweight and troy ounces
- Optional charge allowance, with a clear distinction between extra charge and purity correction
- An advanced process / assay guard:
  - enter effective element retention from stock assay and melt history
  - set a positive fineness-point guard above the nominal recipe
  - calculate raw charge weights that predict the guarded final composition after the assumed losses
  - distinguish a proportional charge allowance from a true assay / composition correction
- Editable compositions, custom house formulas, local saved recipes, copy-to-clipboard and print sheet
- Expected colour preview
- Process cards for:
  - in-machine crucible / Galloni G1-style gold workflow
  - Pt-capable Galloni Fusus-style centrifugal workflow with ceramic / quartz crucible and small button / ingot route
  - pre-alloying outside the casting cycle
  - torch / bench work
- Safety notes for zinc, nickel, cadmium, beryllium, platinum temperature, moisture and crucible segregation
- Data notes and source links

## Run it locally

Open `index.html` directly in a browser, or serve the folder:

```bash
python3 -m http.server 8000
```

The app has no build step, external JavaScript, external fonts or external CSS. The logo is embedded into `index.html` as a data URI so the main file remains portable. The original uploaded logo is also retained at `assets/TJ-Hand-Crafted-Logo.webp`.

## Publish with GitHub Pages

Yes — this can be run as a normal static GitHub Pages site:

1. Create a GitHub repository.
2. Upload `index.html`, `README.md` and the `assets/` folder.
3. Open **Settings → Pages**.
4. Under **Build and deployment**, choose **Deploy from a branch**, select `main` and the `/ (root)` folder, then save.
5. GitHub will provide a URL such as `https://yourname.github.io/repository-name/`.

Use the GitHub Pages URL rather than the `raw.githubusercontent.com` file URL. The saved-recipe library uses browser `localStorage`, so saved recipes are private to that browser and are not synchronised between devices. There is no backend or database.

## Important production note

The recipes are representative starting compositions, not certified commercial alloy specifications. Supplier formulas may use grain refiners, deoxidisers, master alloys and different Cu / Ag / Pd / Ni balances. Before saleable production, confirm the exact formula and casting programme with the alloy supplier, the machine manual and a suitable assay / quality-control process.

For platinum, use the correct Fusus / platinum-rated machine, ceramic or quartz crucible, investment, atmosphere and optical-pyrometer programme for the specific alloy. A standard gold-only Galloni G1 programme should not be treated as a platinum process. The UI intentionally flags this rather than giving a universal platinum temperature setting.
