# Stand and Be Heard (Acoustic) — chord map

> **Status:** machine-generated draft (2026-10-24). Verify by ear before trusting.
> Stems + raw analysis: `C:\Work\Music\STEMS\stand-and-be-heard-acoustic\` (not in git).
> Source: Suno "Split from mix → Acoustic Guitar", V4. 48 kHz / 16-bit / stereo, 5:43.

## Summary

| | Value | Confidence |
|---|---|---|
| **Key** | **B♭ minor** (relative: D♭ major) | High: guitar and backing stems agree independently |
| **Tempo** | **139 BPM, 4/4** (from Suno Studio) | High: Suno's grid matches the audio (199 bars × 1.727 s = 5:43.6) |
| **Length** | 199 bars | High |
| **Tuning** | Guitar stem +9 cents (A ≈ 442 Hz); backing +2 cents | Medium: see below |
| **Harmonic rhythm** | 1 chord per bar; **2 bars per chord in the half-time section (bars 124–151)** | High in the strong sections |

Bar numbers match **Suno Studio's ruler** (bar 1 = 0:00). Set Studio's loop straight from this table.

## Core progressions

| Name | Chords | Function |
|---|---|---|
| **Loop A** | B♭m – G♭ – A♭ – B♭m | i – VI – VII – i |
| **Loop B** | B♭m – D♭ – G♭ – A♭ | i – III – VI – VII |
| **Turn** | E♭m – B♭m – E♭m – E♭ | iv – i – iv – IV |

## Song map (bars)

| Bars | Section (my label) | Chords | Confidence |
|---|---|---|---|
| 1–16 | Intro | Sparse; mostly D♭, A♭, G♭, E♭m colors | Low: quiet, check by ear |
| 17–48 | Verse 1 (sparse) | Mostly B♭m ↔ G♭, some A♭ / E♭ | Low–medium |
| 49–80 | Verse 2 / pre | **Loop A** ×8 (D♭ subs in bars 57, 69) | High |
| 81–89 | Build | G♭ – A♭ – B♭m (B♭m held 85–87) | Medium |
| 90–101 | **Chorus** | **Loop B** ×3 | High |
| 102–118 | Post-chorus | **Loop A** ×4 | High |
| 119–123 | Turn | **Turn** (iv – i – iv – IV) | Medium |
| 124–133 | Break | B♭m held (10 bars) | High |
| 134–151 | **Half-time** | G♭ G♭ A♭ A♭ \| B♭m B♭m D♭ D♭ \| G♭ G♭ A♭ A♭ \| B♭m ×4 \| G♭ G♭ | High |
| 152–156 | Transition | Unclear (Cm?/G♭/E♭m/A♭) | Low |
| 157–178 | **Final chorus** | **Loop B** ×5–6 | High |
| 179–199 | Outro | Loop A variations; ends G♭ – G♭ – E♭ – B♭ – B♭m | Medium |

Section names are guesses from the harmony alone; confirm against the lyrics. Bar-by-bar raw output (with a confidence margin per bar): `STEMS\stand-and-be-heard-acoustic\analysis-bars-139bpm-2026-10-24.txt`.

## How to play it on the AEG721

**Recommended: capo 1, play "A minor" shapes.**

| Sounds as | Shape (capo 1) |
|---|---|
| B♭m | Am |
| G♭ | F |
| A♭ | G |
| D♭ | C |
| E♭m | Dm |
| B♭ | A |

So the core loop is just **Am – F – G (– C)** with a capo on the 1st fret. That's almost certainly how a "solo acoustic singer-songwriter" part would be fingered.

- Strings 1–6 are standard tuning; the 7th string (B) isn't needed. Mute it or don't strum it.
- **Capo check:** the AEG721 nut is ~1.98" wide (vs ~1.69" on a 6-string). A standard 6-string capo may not clamp all 7 strings. Use a 7-string / wide-neck capo, or check that yours reaches.
- No-capo alternative: barre B♭m (1st fret, A-shape minor), G♭ (2nd fret, E-shape), A♭ (4th fret, E-shape), D♭ (4th fret, A-shape).

## Tuning note

The guitar stem measures ~9 cents sharp (A ≈ 442 Hz); the backing (mostly vocal, with vibrato, so a noisier measurement) measures ~2 cents. Start at **A440**. If sustained chords against the backing produce a slow "wobble" (beating), set the tuner reference to **442 Hz** and retune.

## Treat as suspect

- **Bars 1–48 and 152–156:** quiet or transitional; the analyzer is guessing.
- Odd single bars (E♭ major in bar 17, F in bars 21–22, "G♭m" around bars 24–36, Cm in bar 152) are likely detection errors, sus/add9 voicings, or passing chords the triad-only analyzer can't name.
- Occasional "B♭ major" (bars 41, 102, 181, 185, 198) may be a real major lift or a B♭m with a ringing open note. Check by ear.

## Method

librosa 0.11: `estimate_tuning` (tuning), `beat_track` (tempo), tuning-corrected `chroma_cqt` (pitch content); key by Krumhansl–Schmuckler profile correlation; chords by matching per-bar median chroma (139 BPM grid from Suno Studio, bar 1 = 0:00) to major/minor triad templates. Triads only: 7ths, sus and add chords get forced into the nearest triad.
