# Neo Virtue - Galaxy Parameters

[Open Visualization](index.html)

## Galaxy Shape

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
