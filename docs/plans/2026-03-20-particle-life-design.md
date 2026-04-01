# Particle Life — MyTagSpot Editie

## Doel
Eigen implementatie van Particle Life simulatie. Eén HTML-bestand, zero dependencies. Pure wiskunde, geen AI. Beter dan het origineel (hunar4321/particle-life, MIT).

## Verbeteringen t.o.v. origineel
- Zero dependencies (geen lil-gui)
- Eigen UI panel met brand kleuren (#269dc1, #361283)
- Trail-effecten via alpha fade
- Mobiel-vriendelijk (touch, responsive, overlay panel)
- Presets (Organisme, Sterrenevel, Chaos, Symbiose, Zwerm)
- Visuele interactiematrix (klikbaar grid)
- Nederlandse UI
- "Pure Wiskunde — Geen AI" badge
- Fullscreen toggle
- Pauze/Play

## Architectuur
- Eén `index.html`, alles inline
- Canvas 2D rendering met requestAnimationFrame
- Physics: F = g / d, velocity damping, boundary bounce
- Trail: canvas clear met rgba(0,0,0,alpha)
- Deeltjeskleuren: cyan, magenta, lime, oranje
- Brand: Inter font, MyTagSpot / StΔrDüst21

## Layout
- Desktop: canvas links, panel rechts (300px)
- Mobiel: fullscreen canvas + slide-in panel overlay
- Header: titel + "Pure Wiskunde" badge
- Footer: branding

## Controls
- Presets dropdown
- Deeltjesaantal slider
- Snelheid slider
- Trail-intensiteit slider
- Viscositeit slider
- Interactiematrix (visueel grid, klik om waarde te wijzigen)
- Randomize, Symmetrie, Reset, Pauze, Fullscreen knoppen
