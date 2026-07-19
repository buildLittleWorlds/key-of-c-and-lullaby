# Rulebook vs. Vibes

A one-page "paper app" about where your ear gets its orders.

> "Stay in the key of C" is a **rule** you can write in one sentence.
> "Make it sound like a lullaby" is a **habit** soaked up from a thousand examples.
> Your ear runs both — which one is in charge?

This is the smallest working version of that question: a tiny melody maker with one keyboard and two ghosts behind it.

## What it does

The page shows a short row of keys and two modes. The same keys behave differently depending on which ghost is running them.

- **Rulebook mode** — a *hard rule*. Only the notes in the key of C exist. The off-key notes are struck out and won't play at all. There is no wrong note, because wrong notes have been removed.
- **Trained mode** — a *soft habit*. Every key plays, but the keys are shaded by how often that note tends to show up in lullabies. Nothing is forbidden; some notes are just likelier. You can break the mood here — in Rulebook you can't even find the door.

A **"Hear a lullaby phrase"** button plays one of three public-domain lullabies (Twinkle Twinkle, Brahms' Lullaby, Rock-a-bye Baby) on the same keys, lighting each key as its note sounds. Watching the tune land again and again on the bright keys shows where the shading comes from.

## What to try

1. Pick a mode and tap out a little tune — left to right, then wander back.
2. Switch modes and play the *same* path again.
3. Listen for what changed.

Then press **Hear a lullaby phrase** and watch which keys light up.

## Why some notes are shaded "lullaby notes"

The shading isn't random. Lullabies across many cultures share a few musical habits — descending melodic lines, a narrow pitch range, a strong pull toward the tonic and dominant notes (in C, that's C and G), and lots of repetition. Those tendencies are why the middle keys glow and the edges stay dim.

The app includes a short **"research behind the shading"** section with plain-language explanations and references, plus one honest complication: researchers have found that a lullaby's calming quality lives partly in *how it's sung* — softly, slowly, in a caregiver's voice — not only in which notes are used. A keyboard can only shade notes, so it captures a real slice of the idea, not the whole thing.

## The honest version of the punchline

Push far enough and the rule dissolves into the habit. "Only scale notes" is really just "these notes got full weight, the rest got zero" — the hardest possible version of a trained preference. **Law is habit with the volume turned all the way up.** Your ear runs the soft version constantly; the rulebook is the rare moment it goes rigid.

## Running it

It's a single self-contained `index.html`. No build step, no dependencies, no API keys, no network calls. Sound is generated in the browser with the Web Audio API.

- **Locally:** open `index.html` in any modern browser.
- **On GitHub Pages:** enable Pages for this repo (Settings → Pages → deploy from the `main` branch, root folder) and the page will be live at your Pages URL.

## Controls

- Tap the on-screen keys, or use the keyboard: **A S D F G H J K L**
- Switch modes with the buttons, or press **R** (rulebook) / **T** (trained)

## Notes and credits

The three melodies are short, hand-entered transcriptions of public-domain lullabies, meant to be representative rather than note-perfect. The trained weights were tallied to match those tunes and the broader tendencies described above.

Built as a teaching demo — a small artifact for thinking about the difference between rules and learned preference.
