# Nanowatt Humidity Sensor for Smart Food Packaging

A 0.4 V, ultra-low-power humidity-sensor readout for compostable food packaging. A printed graphene-oxide chemiresistor forms a divider whose output drives two 6-transistor CMOS Schmitt triggers, giving a two-level alarm (caution at about 60% RH, danger at about 75% RH) with 73–133 nW static power.

Designed and simulated in Cadence Virtuoso (Spectre, gpdk045, L = 45 nm), with layouts in Virtuoso Layout XL and Microwind.

**Live site:** `https://<your-username>.github.io/<repo-name>/`

## Highlights

| | |
|---|---|
| Supply | 0.4 V (subthreshold CMOS) |
| Thresholds | 242 mV (≈60% RH) and 275 mV (≈75% RH) |
| Static power | 72.96 nW / 80.38 nW / 133.35 nW by output state |
| Switching window | about 6 mV of input change |
| Power source (proposed) | Resonant RF coil, read on demand by a phone or reader |

## Repository layout

```
index.html        the project page (single file, no build step)
assets/           schematics, simulation plots and layouts from the design
.nojekyll         tells GitHub Pages to serve files as they are
```

## Publish on GitHub Pages

1. Create a new public repository on GitHub, for example `humidity-sensor`.
2. Upload everything in this folder to the repository root: **Add file → Upload files**, drag in `index.html`, `README.md`, `.nojekyll` and the `assets` folder, then **Commit changes**.
3. Open **Settings → Pages**. Under **Build and deployment**, set **Source** to *Deploy from a branch*, choose branch `main` and folder `/ (root)`, then **Save**.
4. After about a minute the site is live at `https://<your-username>.github.io/humidity-sensor/`.

Using git instead:

```bash
cd humidity-sensor
git init -b main
git add .
git commit -m "Add humidity sensor project site"
git remote add origin https://github.com/<your-username>/humidity-sensor.git
git push -u origin main
```

## Team

Md Wahiduzzaman, Elmul Soad Swopno, Md Rahib-bin-Hossain. EEE 4861 VLSI Design, Islamic University of Technology (IUT), supervised by Dr. Md Masum Billah.
