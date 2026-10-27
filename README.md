# Nachtflug -- Night Flight

**English** · [Deutsch](README.de.md)

A demo by Hans Schnorrenberger, written in
[Drachenhauch](https://github.com/HasoSchno70/Drachenhauch): uplifting trance
from A minor to C major, about four and a half minutes. A journey from the
sea at night over the mountains, through a tunnel of light into space to a
galaxy -- and back home: earthrise in orbit, re-entry, above the clouds with
a skein of wild geese, past a coast with a lighthouse, until the sun rises
over the sea. Every scene has its own sounds -- sea, wind, rumble, geese,
surf, gulls, a foghorn. Music, sounds and pictures are all made by the
program itself: there is not a single sound or image file in it.

**▶ Watch it in your browser: https://hasoschno70.github.io/Nachtflug/**

Click once to start (browsers only play sound after a click), put on
headphones, ⛶ for full screen. The first load is about 20 MB.

![Earthrise in orbit](bilder/06_erde.jpg)

## The journey

| | |
|---|---|
| ![Ocean at night](bilder/01_ozean.jpg) | ![Low flight](bilder/02_tiefflug.jpg) |
| **Ocean at night** -- northern lights, moonlight on the water, shooting stars | **Low flight** through a valley, a river of light, snow falling |
| ![Tunnel of light](bilder/03_tunnel.jpg) | ![Star nebula](bilder/04_nebel.jpg) |
| **Tunnel of light** -- neon rings racing past on the beat | **Star nebula** -- the breakdown, a voice: "close your eyes" |
| ![Galaxy](bilder/05_galaxie.jpg) | ![Earthrise](bilder/06_erde.jpg) |
| **Galaxy** of 2,600 light trails, a comet, the key change | **Earthrise** -- city lights, the glowing rim of the atmosphere, the sun rising over the edge of the Earth |
| ![Re-entry](bilder/07_wiedereintritt.jpg) | ![Above the clouds](bilder/08_wolken.jpg) |
| **Re-entry** -- plasma glowing with the kick drum | **Above the clouds** -- a sea of clouds, wild geese heading for the sun |
| ![Coast](bilder/09_kueste.jpg) | ![Daybreak](bilder/10_tagesanbruch.jpg) |
| **Coast** -- cliffs, surf, a lighthouse turning in time | **Daybreak** over the sea, where it all began; a swarm of sparks writes "Drachenhauch" |

## How it is made

* **Music:** synthesised note by note (`AUDIO_NOTE`, `AUDIO_SFX`) and played
  on an audio clock: supersaw lead, piano, a choir built from overtones and
  formants, pads that pump under the kick, a trance gate, a key change in the
  finale, and on the way home the harmony brightens from A minor to C major.
  The voice comes from the system's speech output and is layered and echoed.
* **Sounds:** filtered noise and notes -- the goose call, for example, is
  built like the choir: overtones weighted by nasal formants, with a fast
  rasp in the voice.
* **Pictures:** every scene is a fragment shader (raymarching through
  terrain, clouds as a volume, cliffs and a lighthouse as distance fields);
  the galaxy is a real 3D scene drawn with one instanced draw call.
* **Everything follows the music:** what pulses, pulses with the kick drum,
  what flashes, flashes with the melody, the colours follow the chords, and
  the scenes change through light.

## What is in this repository

The browser version: the Drachenhauch runtime `dhrt` compiled to WebAssembly
(`dhrt.wasm`, `dhrt.js`, `dhrt.data` with the shaders) and the source
`program.dh`, which is compiled in the browser when the page starts. To try
it locally, serve the folder with any static web server, e.g.
`python -m http.server`, and open the page.

The licences of the libraries contained in `dhrt.wasm` are listed in
[THIRD-PARTY-NOTICES.txt](THIRD-PARTY-NOTICES.txt).
