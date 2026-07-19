# Rulebook vs. Vibes

A one-page "paper app" about where your ear gets its orders.

> "Stay in the key of C" is a **rule** you can write in one sentence.
> "Make it sound like a lullaby" is a **habit** soaked up from a thousand examples.
> Your ear runs both — which one is in charge?

This is the smallest working version of that question: a tiny melody maker with one keyboard and two ghosts behind it.

## What it does

The page shows a short row of keys and two modes. The same keys behave differently depending on which ghost is running them.

- **Rulebook mode** — a *hard constraint*. Only the notes in the key of C exist. The off-key notes are struck out and won't play at all. There is no wrong note, because wrong notes have been removed.
- **Trained mode** — a *soft weight*. Every key plays, but the keys are shaded by how often that note appears in a handful of lullabies. Nothing is forbidden; some notes are just likelier. You can break the mood here — in Rulebook you can't even find the door.

A **"Hear a lullaby phrase"** button plays one of three public-domain lullabies (Twinkle Twinkle, Brahms' Lullaby, Rock-a-bye Baby) on the same keys, lighting each key as its note sounds. Watching the tune land again and again on the bright keys shows where the shading comes from — the training set, made audible.

## What to try

1. Pick a mode and tap out a little tune, left to right, then wander back.
2. Switch modes and play the *same* path again.
3. Listen for what changed.

Then press **Hear a lullaby phrase** and watch which keys light up.

## What it honestly shows — and what it doesn't

**What it really shows:** the difference between a *hard constraint* (a note is removed) and a *soft weight* (a note is merely favored). That gap is real and you can hear it — the rulebook can never surprise you; the trained ear can.

**What it only suggests:** that this is how a "trained model" actually works. It isn't, quite. The weights here are just a tally — a count of how often each scale note shows up across the three lullabies, shaded onto the keys. That's a **histogram, not a network**. A real learned model weighs each note *in context* (what came just before), holds thousands of such odds at once, and would happily suggest an out-of-key note if its examples did. This toy has no memory of your last note at all.

**The punchline:** push far enough and the rule dissolves into the vibe. "Only scale notes" is really just "these notes got weight 1, the rest weight 0" — the hardest possible version of a trained preference. Law is habit with the volume turned all the way up.

## Running it

It's a single self-contained `index.html`. No build step, no dependencies, no API keys, no network calls. Sound is generated in the browser with the Web Audio API.

- **Locally:** open `index.html` in any modern browser.
- **On GitHub Pages:** enable Pages for this repo (Settings → Pages → deploy from the `main` branch, root folder) and the page will be live at your Pages URL.

## Controls

- Tap the on-screen keys, or use the keyboard: **A S D F G H J K L**
- Switch modes with the buttons, or press **R** (rulebook) / **T** (trained)

## Notes and credits

The three melodies are short, hand-entered transcriptions of public-domain lullabies, meant to be representative rather than note-perfect. The trained weights were tallied ahead of time to match those tunes.

Built as a teaching demo — a small artifact for thinking about the difference between rules and learned preference.
