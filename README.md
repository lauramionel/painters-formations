# formations

ten painters. each one moves and sounds different.

**[live →](https://lauramionel.github.io/painters-formations/)**

---

started after seeing [a patternseeing reel](https://www.instagram.com/reel/DXSa8wbiAZU/) — wanted something in the same spirit but online and that you could touch. then i started adding sound (one voice per painter), which took longer than the visuals tbh

each preset = palette + particle shape + motion engine + procedural tone.js voice. ten so far:

1. **van gogh** — multiple swirl centers, dash strokes, c minor pentatonic pad
2. **monet** — soft brush dabs (halo + core), d pentatonic AM bells
3. **mondrian** — particles snap to a grid lattice, primary-color chords on click
4. **pollock** — particles thrown from rect edges with momentum + drag, drip widths vary a LOT, distorted drum + horn
5. **klimt** — counter-rotating elliptical mosaic rings, gold-bell ostinato in F major
6. **schiele** — meandering raw earthy lines, sparse FM cello
7. **matisse** — big slow flat color blobs, warm AM sax pad
8. **kandinsky** — many small lyrical orbits + streak shape, whole-tone chime arpeggio
9. **frida kahlo** — particles bloom outward from the center in spiraling vines, nylon guitar in A phrygian
10. **dalí** — gravity bias pulls everything down (melt), theremin with 1.8s portamento

## controls

click anywhere to drop a vortex (+ chord). drag to stir. ◀▶ or arrow keys to change painter. **M** toggles sound (it only inits on first click — browser policy). **F** fullscreen, **H** hide ui, **R** reset.

## stack

one html file. no build, no node modules.

- p5.js for canvas + particles
- tone.js for audio (PolySynth, AMSynth, FMSynth, MetalSynth, PluckSynth, MonoSynth, MembraneSynth — different one per painter)
- a chunk of hand-css for the retrofuturist selector at the bottom — brushed-metal radial gradients, recessed CRT readout, glowing LEDs. probably the part i spent the most time on after the motion engines tbh

~1500 particles, each updated each frame by one of the motion engines (flowfield / multiswirl / dab / drip / mosaic / meander / bloom / grid / polygon / pulse). monet was the hardest to land — too still and it's nothing, too lively and it stops feeling impressionist.

things that didn't make it:
- a 3d sphere version (looked cool but lost the painting feel)
- picasso, hokusai, riley, rothko, kusama, basquiat, lee ufan, soulages — kept some, killed some, motion ended up too similar across a few of them
- a "compose your own" mode where you mix engines

## run it

```
git clone https://github.com/lauramionel/painters-formations
cd painters-formations
open index.html
```

that's it.

## license

MIT. take it apart, add painters, change the sounds. would love to see what you make
