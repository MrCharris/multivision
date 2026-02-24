# MULTIVISION
### Minute to Midnight Edition

A real time audio visualizer with six visualization modes. Cassette futurism aesthetic.

🔗 **Live Demo:** [minutetomidnight.netlify.app](https://minutetomidnight.netlify.app)

![MULTIVISION Screenshot](screenshot.png)

---

## What It Does

**Six Visualization Modes:**
- **Spectrum Analyzer** — Frequency bars with hover to inspect (shows Hz and dB)
- **Spectrogram** — Scrolling frequency heat map with adjustable speed
- **Oscilloscope** — Dual channel waveform display with trigger controls, split or overlay layouts, timebase and voltage scaling
- **Vectorscope** — Stereo phase visualization with adjustable gain, rotation, persistence, and intensity
- **Stereometer** — Polar stereo field display with correlation meter
- **Meter** — Three analog gauge style dials (RMS, Peak, LUFS) with sweeping red needles

**Controls:**
- Waveform scrubber with click to seek
- Play, pause, stop, and reset transport
- Draggable knob controls for each mode's parameters
- Doomsday clock loading animation

**Design:**
- Forest green (#194729) and cottage white (#fffff7) with deep red (#8B0000) accents
- Pressure gauge style meters that sweep from 8 o'clock to 4 o'clock over the top
- Rotary knobs with drag interaction

---

## Technical Details

Built with React, Web Audio API, and Canvas.

The audio analysis includes FFT frequency data for spectrum and spectrogram modes, time domain waveform data for oscilloscope and vectorscope, stereo channel separation using ChannelSplitterNode, and RMS, peak, and LUFS calculations for the meter mode.

The oscilloscope has configurable timebase from 0.5ms to 10ms per division, voltage scaling, trigger system with rising and falling edge detection, and channel selection with split or overlay display options.

---

## Run It Yourself

Open `index.html` in any browser. No build step, no dependencies.

---

## Why I Built This

I've spent 8+ years running events where if the AV fails, the whole room is just staring at you. I've been the guy checking phase correlation on a vectorscope five minutes before a livestream goes live, watching meters to make sure we're not clipping into broadcast, troubleshooting why the confidence monitor is showing the wrong feed while 200 people are finding their seats.

I know what these tools look like when they're doing their job. I've used the professional versions under pressure, not in a classroom.

So this was kind of an experiment. Could I build one of these tools myself, not by learning to code from the ground up, but by directing the project like I'd direct a production? Like being the TD who knows exactly what the show needs but isn't the one running cables.

Coding is a real skill that takes years to develop. I respect that. But I wanted to see what happens when you know a domain well enough to direct something even if you can't build it yourself. Not as a replacement for actually learning, but as a stepping stone. Build something real, figure out what you don't know along the way.

Turns out I learned more than I expected, and not just about the tool.

---

## What I Actually Did Here

**Working with what's actually there**

Most people either trust AI output uncritically or dismiss it entirely. I tried to do neither. Claude has known failure modes, confabulates details, slips into agreeability, loses calibration over long conversations. So you learn how to work with that instead of pretending it's not there.

Shorter questions instead of giant prompts. Pushing back when something's wrong instead of accepting the first answer. Uploading actual documents instead of hoping it remembers correctly. Checking everything against what I already know about the domain. The visualizer exists because I kept catching problems and saying "that's not right, try again," not because the first version worked.

**Learning by doing, not by the binary result**

This project went through 25+ versions. Audio wasn't playing. Dots were drawing as lines instead of scattered points. Needles were sweeping the wrong direction. The layout had this awkward gap that drove me crazy.

Every problem was the same loop: figure out how to describe what's broken, get a fix, check if the fix actually worked or just created a new problem. That's where the learning happened. Not in getting a clean answer on the first try.

You find new shapes by sketching. You find new tricks by just flicking a board and seeing what happens. I like to learn by doing, and this was a lot of doing.

**Actually shipping the thing**

Getting this from "cool demo in a chat window" to "actual URL you can visit" was its own thing. npm permission errors on my Mac, TypeScript yelling at me, file formats I'd never heard of, deployment pipelines. I didn't know what I was doing but I figured it out because the goal was to actually ship something, not just have a neat artifact sitting in a conversation.

Most people skip that part. Having the idea is easy, pushing through the annoying stuff until something actually exists is the harder thing.

---

## How This Connects to What I Do

At GP Strategies I coordinated events for 16,000 engineers across 8 divisions, including a biannual conference with 3,000+ attendees and 20 global keynote speakers. That job was basically being a router. Executive wants this, production needs that, vendor can do this other thing, figure out how all of it talks to each other and make sure nothing falls through the cracks.

At Chariot Group I was on the installation side. Extron, Biamp, Zoom room integration, control systems in government buildings and event venues. So I know the technical layer too, not just the planning and coordination layer.

Through Changing Lanes I've run 100+ events from the initial concept all the way through breakdown. Venue relationships, budgets, run of show documents, day of troubleshooting when something inevitably goes wrong.

This project was the same muscle pointed at something new. The domain was different but the process felt familiar.

The way I work is basically: freestyle something, see what sticks, figure out why the stuff that didn't work didn't work, then go again with that information. That's how the visualizer got built. Try a thing, it breaks, figure out how to describe what's broken, get it closer, check it against what I know it should actually look like. Twenty five versions of that loop is how you get from "audio isn't playing" to a working six mode visualizer with oscilloscope triggers and a vectorscope I'd actually trust to check phase.

That's also just how I learn. Not by reading about something first and then doing it, but by doing it and finding the edges and then understanding what I'm looking at. The messy version teaches you more than the clean version, because you have to actually engage with why something went wrong instead of just accepting the first answer.

If you're reading this and wondering whether I can manage technical projects and work across teams that don't speak the same language, this is what that looks like when I point it at something outside my usual lane.

---

## License

MIT

---

*Built by Chris Harris • Built with Claude • 2025*
