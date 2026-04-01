# Particle Life — Full Physics Lab Design

## Doel
6 wiskundige modellen implementeren als schakelbaar "wetenschappelijk laboratorium". Globale model-selector, dynamische parameters per model, nieuwe presets.

## Modellen

1. **Lennard-Jones** (bestaand): F = α·[(σ/r)⁶ - (σ/r)³]
2. **Morse**: F = α·2a·D·(1-e^(-a(r-r₀)))·e^(-a(r-r₀)) — zachter, organisch
3. **Yukawa**: F = α·g·e^(-μr)·(μr+1)/r² — uitdovende kracht, clustering
4. **Coulomb (afgeschermd)**: F = α·q/r²·e^(-r/λ) — plasma
5. **Vortex**: F_tang = α/r, F_rad = β/r² — draaikolken
6. **Spring-Damper**: F = -k·(r-r₀) - c·v_rad — elastisch

## UI Wijzigingen
- Model-dropdown bovenaan (naast preset-dropdown)
- Formule-display update per model
- Dynamische parameter-sliders per model
- Nieuwe presets per model

## Architectuur
- Eén `index.html`, alles inline
- Physics functies als aparte functies, geschakeld via model-selector
- Bestaande features blijven intact
