# SkyAnchor — SovereignSkies Observer Network

**Free, open-source aerial observation science tool for citizen sky observers.**

No accounts. No paywalls. No speculation laundering. Just physics.

---

## What It Does

SkyAnchor is a single-file HTML/JS application that turns a casual sky observation into a bounded physical measurement. Anyone with a phone can use it.

- **GPS anchor** — locks your position, autofills elevation
- **Weather autofill** — pulls live temperature and dew point from Open-Meteo (free, no API key)
- **Cloud base calculation** — standard LCL (Lifting Condensation Level) formula used by aviation worldwide
- **Triangulation** — single-observer trig + optional two-observer geometric baseline
- **Data quality dashboard** — per-metric confidence breakdown; you see exactly what is driving your estimate
- **Observer Portrait** — a live visual illustration of your observation that builds as you enter data; downloadable as PNG
- **Scientific report generator** — structured field report in plain text, downloadable
- **SovereignSkies tab** — anonymous observation submission; one submission unlocks the area cluster map

## The Physics

Cloud base height from surface thermodynamics:

```
H_agl (ft) = [(T_F − T_dF) / 4.4] × 1,000
H_agl (m)  = [(T_C − T_dC) / 2.5] × 1,000
```

Trigonometric altitude from elevation angle and horizontal range:

```
H_agl = D_horizontal × tan(θ_elevation)
```

Two-observer geometric triangulation (no range required):

```
H = B × [tan(α) × tan(β)] / [tan(α) + tan(β)]
```

## Privacy

- GPS coordinates are stored only in your browser
- Weather data is fetched from Open-Meteo directly from your device
- SovereignSkies observations are stored in `localStorage` only — nothing is transmitted without your action
- No tracking. No account. Anonymous by default.

## Usage

Open `index.html` in any modern browser. No build step. No dependencies. No server.

## The Sovereign Right

Citizens have a right to know what is in their skies. This tool exists because one careful observer — anchored to a GPS position, with a calibrated temperature/dew point reading — can constrain an aerial object's altitude to within a physical bracket. That is not anecdote. It is a bounded physical measurement. Aggregated across many observers, it becomes a distributed sensor network that no institution controls.

## Contributing

Fork it. Improve it. The sky belongs to everyone who looks up carefully.

## License

Public domain. No proprietary claims. Formulas sourced from standard aviation meteorology and basic trigonometry.

---

*SkyAnchor v2 · SovereignSkies Edition*
