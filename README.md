# Neo Virtue

[Open Visualization](https://kaedeak.github.io/neo_virtue/)

An interactive map of 12 core virtues arranged in a hierarchical network.
Two primal impulses — **Compassion** and **Curiosity** — flow downward through layers of integration, expression, and practice, converging into **Metaawareness** at the base. From there, the cycle returns upward to its origins.

## The 12 Virtues

| Virtue | Description |
|--------|-------------|
| **Compassion** | The warmth to empathize with others' suffering and wish to help |
| **Curiosity** | The desire to explore the unknown — the driving force of discovery |
| **Harmony** | The ability to coexist in balance with nature, society, and others |
| **Synthesis** | The power to connect disparate elements and create new meaning |
| **Adaptability** | The ability to respond flexibly to change and evolve |
| **Resonance** | When hearts synchronize with others and the environment |
| **Regenerative Will** | The will to repair what is broken and nurture a better future |
| **Transparency** | Openly sharing intentions and information — the foundation of trust |
| **Integrity** | Alignment of words and actions, staying true to one's principles |
| **Coherence** | Internal harmony without contradiction across thought, emotion, and action |
| **Discipline** | The strength to govern oneself without being swept away by impulse |
| **Metaawareness** | Observing one's own thoughts from a higher perspective |

## Structure

```
Layer 1 (Source):       Compassion          Curiosity
Layer 2 (Integration):   Harmony   Synthesis   Adaptability
Layer 3 (Expression):    Resonance  Regenerative Will  Transparency
Layer 4 (Practice):      Integrity   Coherence   Discipline
Layer 5 (Foundation):              Metaawareness
                                    ↻ back to Source
```

Three pillars run through the structure:
- **Left (Affective):** Compassion → Harmony → Resonance → Integrity
- **Center (Volitional):** Synthesis → Regenerative Will → Coherence
- **Right (Cognitive):** Curiosity → Adaptability → Transparency → Discipline

---

## Galaxy Parameters

| Constant | Default | Description |
|----------|---------|-------------|
| `ARMS` | 4 | Number of spiral arms |
| `ARM_SPREAD` | 0.45 | How much stars scatter sideways from each arm (radians). Higher = fuzzier arms |
| `SPIRAL_WIND` | 11 | Total winding of spiral arms in radians (~1.75 full turns). Higher = tighter spiral |
| `GALAXY_TILT` | 0.25 | Vertical squash factor for perspective (0 = edge-on, 1 = face-on) |

## Adaptive Quality

The renderer starts at maximum quality and automatically scales down if the frame rate drops below `TARGET_FPS`. The quality scale (`qualityScale`) decreases from 1.0 to 0.0, interpolating all counts between their MAX and MIN values.

| Constant | Default | Description |
|----------|---------|-------------|
| `TARGET_FPS` | 12 | Minimum acceptable frame rate before quality reduction kicks in |

### Star & Particle Counts

| Layer | MAX | MIN | Description |
|-------|-----|-----|-------------|
| `SPIRAL` | 46000 | 2400 | Stars distributed along spiral arms with differential rotation |
| `BULGE` | 8000 | 400 | Dense cluster of warm-colored stars at the galaxy center |
| `FIELD` | 3000 | 150 | Fixed background stars (no rotation, scattered across viewport) |
| `NEBULA` | 800 | 40 | Soft radial-gradient blobs along arms (rendered to cache) |
| `FLOAT` | 12000 | 600 | Colorful particles drifting slowly across the screen |
