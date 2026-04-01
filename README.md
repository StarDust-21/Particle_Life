# Particle Life

Emergent behavior from simple mathematical interaction rules. A single-file physics simulation with 6 force models, zero dependencies.

**[Live Demo](https://mytagspot.nl/Particle%20Life/)** | Built by [StΔrDüst21](https://github.com/StarDust-21)

---

## What is this?

Particle Life simulates N particles divided into k species (colors). Each pair of species has an interaction strength α ∈ [-1, 1]. From these simple rules, complex patterns emerge spontaneously — organisms, galaxies, swarms — none of it programmed, all of it emergent.

## Features

- **6 Physics Models** — Lennard-Jones, Morse, Yukawa, Coulomb (screened), Vortex, Spring-Damper
- **Interactive Matrix** — Click to edit species interactions in real-time
- **8 Presets** — Organism, Nebula, Chaos, Symbiosis, Swarm, Galaxy, DNA, Supernova
- **Spatial Hashing** — O(n·k) instead of O(n²), ~20x faster
- **Multi-layer Canvas** — Background, simulation (trail effects), glow effects
- **Analysis Panel** — Temperature, kinetic energy, spatial entropy, cluster detection
- **Mouse Interaction** — Attract (left click), repel (right click), pulse (scroll)
- **Mobile Friendly** — Touch controls, responsive panel
- **Share** — URL-encoded state sharing
- **Export** — Screenshot (PNG) and data export (CSV)
- **Zero Dependencies** — Single HTML file, no libraries

## The Math

### Force Model (Lennard-Jones)

```
F(r) = α_ij · [(σ/r)^6 − (σ/r)^3]
```

- **r** — distance between particles
- **α_ij** — interaction strength between species i and j
- **σ** — equilibrium distance

### Velocity Update

```
v(t+1) = v(t) · γ + F · Δt
```

- **γ** — damping factor (viscosity)
- **Δt** — timestep

### Spatial Entropy

```
S = -Σ p_k · log₂(p_k)
```

High S (~6.0) = gas-like uniform distribution. Low S (~1-2) = clustered crystals or organisms.

## Keyboard Shortcuts

| Key | Action |
|-----|--------|
| `Space` | Pause / Play |
| `R` | Random rules |
| `F` | Fullscreen |
| `G` | Toggle glow |
| `H` | Toggle heatmap |

## Built With AI

This project was built with the help of **Claude Opus 4.6** (1M context) by Anthropic. The code, UI design, physics implementations, and optimizations were developed through human-AI collaboration. Being transparent about this because honesty matters.

## References

- Lennard-Jones, J.E. (1924). "On the Determination of Molecular Fields"
- Vicsek et al. (1995). "Novel Type of Phase Transition in a System of Self-Driven Particles"
- Reynolds, C. (1987). "Flocks, Herds, and Schools: A Distributed Behavioral Model"

---

MyTagSpot · StΔrDüst21
