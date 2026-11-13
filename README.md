# All Day Anatomy

An annotated sample-timeline player for Girl Talk's *All Day* (2010) — the seamless 71-minute mashup album built from hundreds of samples — rebuilt in November 2026 after all three of the original fan-made visualizers died:

- **AllDaySamples** (Travis McLeskey) — the domain lapsed and is parked.
- **Mashup Breakdown** (Benjamin Rahn) — unreachable.
- **All Day, Annotated** (Matt Adereth) — the page still stands, but its SoundCloud audio source was removed, so it renders and plays nothing.

All Day Anatomy is a tribute to those three and a repair of what they did: it iterates on their interfaces rather than cloning any of them.

**Live page:** https://muse.ai/s/all-day-anatomy-xhs6yxjdtxyamx0/6Vp1OmuBh-RTjiMzveXW2hAmddewtA0zroIMYyXDf8s

## What it does

Press play and the album streams while every sample lights up at the moment it sounds:

- **The braid** — each sample is a strand on a chart whose vertical axis is the *source recording's year*, so you can watch the decades stack up inside a passage. Samples are color-coded by decade.
- **Right Now panel** — a crate-card listing of everything active at the playhead, with per-sample progress.
- **Spotlight** — click any sample (its strand, its Right Now card, or its list row) to spotlight it while the rest of the braid ghosts around it; click it again to release.
- **Artist search** — type a name and jump to any moment they appear.
- **Synced list view** — all timed samples in album order, grouped by the album's 12 segments, following playback.
- **Decade filters** — the legend chips double as filters.
- **Timestamp deep links** — `?t=MM:SS` links (and a "Share this moment" button) cue the player to an exact second.

## Audio

The album itself is not hosted here. The player streams the seamless single-file version from the Internet Archive item [GirlTalk-AllDay](https://archive.org/details/GirlTalk-AllDay). *All Day* was released by Illegal Art under a Creative Commons Attribution-NonCommercial license (CC BY-NC); this project is non-commercial and follows that lane — the page exists to listen and learn, not to sell anything.

## Data and credits

- The sample *identity* list is the one published by Illegal Art for the album's release.
- The per-sample *timings* come from the community breakdown assembled across the three predecessor sites. Credit to **Travis McLeskey** (AllDaySamples), **Benjamin Rahn** (Mashup Breakdown), and **Matt Adereth** (All Day, Annotated).
- Adereth's GitHub project carried no license file, so his timings were used as *facts* only — none of his code or page design was used. This player's code and design are original.
- **Honest gap:** 354 of the 372 documented sampled songs carry community timings. The page says so itself rather than papering over the missing 18.

## Tech

One self-contained `index.html`. No build step, no dependencies, nothing else to install — open it in a browser and it runs. The only external request the page makes is the audio stream from the Internet Archive, a deliberate anti-rot choice: the originals died by depending on outside widgets, so this one depends on almost nothing.
