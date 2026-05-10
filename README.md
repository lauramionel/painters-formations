# Formations

An interactive generative art piece where each of 10 painters gets their own particle motion engine and procedural sound.

**[Live demo →](https://lauramionel.github.io/painters-formations/)**

## What it is

Ten painters, each with a hand-tuned bundle of:

- **Color palette** drawn from their work
- **Particle shape** (dot · streak · dash · glow · square · petal · triangle · smear · softbrush)
- **Motion engine** (flowfield · multiswirl · dab · drip · mosaic · meander · bloom · grid · pulse)
- **Procedural audio voice** in [Tone.js](https://tonejs.github.io/) with painter-specific scale, instrument, and ambient pulse

| #  | Painter      | Motion                                | Sound                                 |
|----|--------------|---------------------------------------|---------------------------------------|
| 1  | Van Gogh     | multiple co-existing swirls           | C minor pentatonic pad                |
| 2  | Monet        | soft impressionist brush dabs         | D pentatonic AM bells                 |
| 3  | Mondrian     | grid-snap primary squares             | triangle-wave marimba pulses          |
| 4  | Pollock      | ballistic drips, varied widths        | distorted membrane drum + FM horn     |
| 5  | Klimt        | counter-rotating mosaic ellipses      | gold-bell ostinato in F major         |
| 6  | Schiele      | meandering raw earthy lines           | sparse FM cello                       |
| 7  | Matisse      | big slow flat color blobs             | warm AM sax pad                       |
| 8  | Kandinsky    | many small lyrical orbits             | whole-tone FM chime arpeggio          |
| 9  | Frida Kahlo  | spiraling vines blooming outward      | nylon guitar in A phrygian            |
| 10 | Dalí         | melting downward gravity drips        | theremin with 1.8s portamento         |

## Controls

- **Click / tap** the canvas — drop a vortex (and trigger a chord)
- **Drag** — stir the currents (occasional accent notes)
- **◀ / ▶** or **arrow keys** — change painter
- **♪** or **M** — toggle sound (audio enables on first user gesture)
- **F** — fullscreen
- **H** — hide UI
- **R** — reset

## Tech

A single self-contained `index.html` (~1300 lines, no build step) using:

- **[p5.js](https://p5js.org/)** for 2D canvas particle rendering
- **[Tone.js](https://tonejs.github.io/)** for procedural audio (PolySynth / AMSynth / FMSynth / MetalSynth / PluckSynth / MonoSynth / MembraneSynth wired through reverb / distortion / filter chains)
- Hand-CSS retrofuturist selector — brushed-metal radial gradients, recessed CRT-style readout, glowing LED indicators
- VT323 + Share Tech Mono via Google Fonts

Each of ~1500 particles is updated each frame by one of ~10 motion engines blending Perlin noise vector fields, tangential circulation, polar lattice attraction, gravity bias, and ballistic momentum.

## Run it locally

```bash
git clone https://github.com/lauramionel/painters-formations.git
cd painters-formations
open index.html
```

No install, no build, no server.

## License

MIT
