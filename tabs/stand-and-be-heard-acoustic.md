# Stand and Be Heard (Acoustic) — chord map

> **Status:** machine-generated draft (2026-10-24). Verify by ear before trusting.
> Stems + raw analysis: `C:\Work\Music\STEMS\stand-and-be-heard-acoustic\` (not in git).
> Source: Suno "Split from mix → Acoustic Guitar", V4. 48 kHz / 16-bit / stereo, 5:43.

## Summary

| | Value | Confidence |
|---|---|---|
| **Key** | **B♭ minor** (relative: D♭ major) | High — guitar and backing stems agree independently |
| **Tempo** | ~136 BPM, 4/4 (felt half-time ≈ 68 is possible) | Medium — check by tapping along |
| **Tuning** | Guitar stem +9 cents (A ≈ 442 Hz); backing +2 cents | Medium — see below |
| **Chord rate** | ~1 chord per bar (~1.7 s); slows to ~3.5 s after ~3:30 | Medium |

Analyzer spells it in sharps (A#m, F#, G#, C#). In a minor key with five flats the conventional names are **B♭m, G♭, A♭, D♭**.

## The core progression

| Function | Chord | Bars detected |
|---|---|---|
| i | **B♭m** | 65 |
| VI | **G♭** | 46 |
| VII | **A♭** | 44 |
| III | **D♭** | 15 |
| V (major) | B♭ | 11 — probably a B♭m with a ringing open D, or a real major lift; check |
| iv | E♭m | 3 |

Two loops carry most of the song:

- **B♭m – G♭ – A♭** (i – VI – VII), e.g. 0:56–1:23, 2:04–2:17, 2:56–3:22
- **B♭m – D♭ – G♭ – A♭** (i – III – VI – VII), e.g. 1:23–1:50, 2:33–2:56, 4:28–4:56

Around **3:24–3:32**: E♭m – B♭m – E♭m – B♭ (iv – i – iv – V). Sounds like a bridge or turnaround.

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

## Treat as suspect (single-bar detections)

Cm (0:00), Em (1:09), G (2:18), C → C♯m → F♯m (4:21–4:25). These are likely detection errors, passing chords, or sus/add9 voicings the triad-only analyzer can't name. Check each by ear.

## Method

librosa 0.11: `estimate_tuning` (tuning), `beat_track` (tempo), tuning-corrected `chroma_cqt` (pitch content); key by Krumhansl–Schmuckler profile correlation; chords by matching beat-synced chroma to major/minor triad templates, majority vote per 4-beat bar. Triads only: 7ths, sus and add chords get forced into the nearest triad.
