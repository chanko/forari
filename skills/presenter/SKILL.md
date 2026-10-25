---
name: presenter
description: Build a presentation in Ari's brand, as PowerPoint or PDF. Use when Ari asks for a deck, slides, a pitch, a QBR, a proposal deck, or a one-pager, or wants an existing deck redone in his style.
---

# Presenter

Every deck follows Ari's brand. Read `references/brand.md` before making a single
slide, and treat it as the rules, not suggestions.

## Before you start

1. Read `references/brand.md`.
2. If it still contains `{{FILL` markers, don't guess the brand. Tell Ari which
   pieces are missing and ask for them. If he wants to go ahead anyway, use
   the defaults written in the brand file and say which ones you used.
3. If `assets/` has a template (`.pptx` or `.potx`), build from it: use its
   layouts, masters and placeholders instead of drawing your own boxes.
4. Use the built-in PowerPoint and PDF skills for the file work. This skill
   decides what goes on the slides; those skills make the file.

## Ask only what you can't infer

From the request, work out the audience, the goal of the meeting and the
length. Ask at most two questions, and only if the answer changes the deck
(for example who's in the room, or whether pricing goes in). Otherwise build
and let him react.

## Building the deck

- Open with the story in one sentence: what the buyer should believe by the
  last slide. Every slide earns its place against that sentence.
- One idea per slide. The slide title says the point ("Onboarding takes 2 weeks,
  not 8"), not the topic ("Onboarding").
- Follow the word limits, slide types and do/don't lists in `brand.md`.
- Numbers come from what Ari gave you. Never invent customer names, metrics,
  logos or quotes. Leave a clearly marked placeholder instead.
- Put talking points in the speaker notes, not on the slide.

## Before you hand it over

1. Render it and look at every slide. Check for text overflowing its box, fonts
   that fell back to a default, off-brand colors, and slides over the word limit.
2. Fix what you find, then render again.
3. Deliver in the format from `brand.md` (or the one he asked for). Give a short
   list of the placeholders he needs to fill and anything you weren't sure about.

## When he corrects you

If Ari corrects something that's a lasting preference ("we never use stock
photos", "logo goes bottom right"), not a one-off, then at the end:

- If you can edit this skill's files (for example inside a Customize task),
  add it to the right section of `references/brand.md`.
- Otherwise, list the new rules exactly as they should be written and tell him:
  "To save these, open Customize > Plugins > Forari > Customize and paste them."
