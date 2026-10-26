# Making a short promo video with Claude

How the StudioBloom video was made, and how to make your own. It's a guide,
not a skill: video takes a few rounds of you watching and giving notes, so
it doesn't fit in one request.

## What you get

A 60-second, 1080p MP4 with an animated story, a professional-sounding
voiceover, original music and sound effects. No stock footage, no editor, no
voice actor.

## What it took

- **About 3 days** of back and forth, 9 versions. Most of that was taste:
  changing the script, the voice, the look, until it felt right. A simpler
  video is a few hours.
- **$4.34 in AI costs**, against a $5 cap set at the start.
- **Claude Code, not Cowork.** Claude has to run programs on your computer
  (Python, ffmpeg to mix audio, a headless browser to render the frames and to
  screenshot the real app). Claude Code does that. Cowork is the wrong tool
  for this job.

## What does what

Everything AI goes through one [OpenRouter](https://openrouter.ai) account,
which gives you every model with one key and one bill.

| Job | Model | Cost |
|---|---|---|
| Voiceover | `openai/gpt-audio`, with voice auditions (marin won; coral and cedar also good) | cents per line |
| Music | `google/lyria-3-pro-preview` (needs streaming) | ~$0.08 a song |
| Images (paper cutout characters, props) | `google/gemini-3-pro-image` (`gemini-3.1-flash-image` for cheap drafts) | ~$0.14 an image |
| Judge (listens to takes and mixes, picks the better one) | `google/gemini-3.8-flash` | cents |
| Word timings, so visuals land on the words | Whisper, running on your computer | free |

## Set it up

1. Install [Claude Code](https://claude.com/claude-code) (the desktop app is
   easiest).
2. Make an OpenRouter account, add $10 of credit, and create an API key
   **with a spending limit** (start with $5).
3. Make an empty folder for the project and put the key in a file called
   `.env` inside it: `OPENROUTER_API_KEY=...`. Never paste the key into a chat.
4. Open the folder in Claude Code and paste the prompt below.

## Starter prompt

> I want a ~60 second 16:9 promo video for [what you're promoting], for
> [who it's for]. The feel: [warm / punchy / premium / funny]. Here's what
> it must say: [3 to 5 points]. Here's what to avoid: [competitors' names,
> prices, claims we can't back up].
>
> My OpenRouter key is in .env. Budget: $5 total. Log every API call's cost
> to spend.log and stop to ask me before going past $5.
>
> Work in this order and stop for my OK after each step:
> 1. Script (with timings) and a storyboard, one line per scene.
> 2. Voice: audition 3 voices on the first two lines with openai/gpt-audio.
>    I pick.
> 3. Music: 3 options with google/lyria-3-pro-preview. I pick.
> 4. Visual style: 2 or 3 test frames. I pick.
> 5. Build the animation as an HTML page (canvas + WebAudio), timed to
>    the voice with Whisper word timings, and render it to 1920x1080 MP4 with
>    a headless browser and ffmpeg.
> 6. Mix voice, music and sound effects, then judge the mix.
>
> Keep a PLAN.md with every decision I make and the spend so far, so we can
> pick up where we left off.

## What we learned

- **Make it ask you at every step.** Script, voice, music and look are taste
  calls. Picking from 3 options is fast; fixing a finished video isn't.
- **Use an AI judge for audio, but carefully.** Have it compare two takes and
  pick one, then ask again with the order swapped: it tends to favor whichever
  it heard first. Only trust a pick that wins both ways. Gemini Flash
  listens well; Gemini Pro made up things it hadn't heard.
- **Set the budget before starting** and have Claude log every call. Image
  generation is where the money goes.
- **Real screenshots beat generated ones** for showing a product. Claude can
  open your app or site in a browser and capture the screens.
- **Keep PLAN.md.** Over several days, it's what lets Claude remember what you
  already decided.
- **Music:** pick a track whose ending lands on a clear button (a final note)
  and have the video end on it.
