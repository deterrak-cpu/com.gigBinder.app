# GigBinder

**A set-list, chord chart, and metronome companion for gigging musicians.**

GigBinder is an Android app for playing live. It holds your whole repertoire — chord/lyric charts, sheet-music PDFs, and scanned pages — organizes it into gigs and sets, and gives you the tools a band actually uses on stage: a per-song metronome, backing tracks, MIDI control, chord transposition, and a way to keep the whole band on the same page. It works fully offline; your library lives in one folder on the device or an SD card.

## Features

**Charts and library**
- Chord/lyric charts, PDFs, and photographed pages, with automatic chord recognition and alignment.
- Transpose the whole song — chart, chord diagrams, and any backing track shift together — in letter names or the Nashville Number System.
- Chord diagrams and voicings for guitar, ukulele, mandolin, banjo, and piano.
- Generate a clean one-page print "arrangement" from a chord/lyric chart.
- Side-by-side two-page view in landscape, with smart splitting of a long single page.
- Organize as **Gigs → Sets → Song Books**: a Song Book is a library of related material, and each set pulls its songs from one book, so unrelated repertoire (say a church set and a rock band's) stays apart.

**Performance**
- Per-song metronome with custom drum patterns, kits, count-in, and named rhythm sections.
- Audio and MIDI backing tracks, with transpose, fine-tune, tempo, and per-instrument MIDI channel mixing; MIDI plays through a bundled SoundFont synth.
- **MIDI in** — turn pages and fire pedal actions from a MIDI keyboard, controller, or foot switch you teach it.
- **MIDI out** — send a patch to your keyboard, pedalboard, or rig (Kemper, Helix, Boss, Fractal, and more) when a song opens.
- Pedal page-turner, annotations, and break music between sets.

**Band sync**
- Play together with no venue Wi-Fi and no internet: the leader's device becomes the band's own network, and everyone else follows the leader's song, page, and transpose. Any member can take over if the leader drops.

**Look-ups**
- **Find song details** — look a song up online to fetch its original key, tempo, and time signature, confirm the match, and keep them as reference alongside your own. Data provided by [GetSongBPM](https://getsongbpm.com).
- Find a tempo, find a MIDI backing track, and import chords/lyrics from the web through an in-app browser.

**Practical**
- Fully offline; one-folder library on device or SD card, with backups.
- Setlist PDF export.
- Available in 12 languages.

## Building

GigBinder is written in Kotlin with Jetpack Compose.

- Android Studio, `minSdk 24` (Android 7.0), `targetSdk 37`.
- Build the app the usual way: `./gradlew :app:assembleDebug`.
- The **Find song details** feature needs a free [GetSongBPM API key](https://getsongbpm.com/api). Keep it out of the repo by setting it as a Gradle property — add `GETSONGBPM_API_KEY=yourkey` to `~/.gradle/gradle.properties` (or pass `-PGETSONGBPM_API_KEY=...`). Without a key the feature stays inert; the build still succeeds.

## Credits

- Song key, tempo, and time-signature data is provided by **[GetSongBPM](https://getsongbpm.com)**.
- MIDI backing tracks are synthesized with [FluidSynth](https://www.fluidsynth.org/) (LGPL-2.1), playing the FluidR3 GM SoundFont (© Frank Wen, MIT) and the GeneralUser GS SoundFont (© S. Christian Collins).

## License

© 2026 GigBinder. All rights reserved.
