# Forari 🏎️

A Claude toolkit that makes Ari faster at the parts of sales that eat the week.

It's a starter. Copy it once, make it yours, and forget this repo exists. There's
nothing to pull or keep in sync.

## What's inside

| Skill | What it does |
|---|---|
| **presenter** | Builds decks (PowerPoint or PDF) in your brand: your template, fonts, colors and slide rules. |
| **voice** | Writes emails, follow-ups and posts the way you write. Gets better every time you correct it. |
| **reviewer** | Reads your email, deck or proposal as the buyer would, and tells you what to fix before you send it. |

## Set it up (about 20 minutes, once)

1. **Download it.** On GitHub: green **Code** button > **Download ZIP**. Unzip it
   somewhere you'll find it, like `Documents/Forari`.
2. **Open that folder in Cowork** and paste this:

   > Set up the Forari plugin in this folder. Read README.md and every SKILL.md,
   > then walk me through filling in everything marked `{{FILL}}`. I'll give you
   > my deck template, brand details and writing samples as we go. Put files
   > where the skills expect them. When we're done, tell me if anything is still
   > blank.

3. **Hand it what it asks for.** Mainly:
   - your PowerPoint template (`.pptx` or `.potx`) and logo
   - your fonts and colors, and what you hate seeing on a slide
   - 10 to 15 things you wrote that sound like you (emails, follow-ups, posts)
4. **Zip the folder.** In Finder, right-click the folder > **Compress**.
5. **Install it.** In Claude: **Customize > Plugins > Add > Upload plugin**, and pick the zip.
6. **Check it.** Start a chat and ask "which skills do you have from Forari?"

## Using it

Just ask for things normally. "Make a 6-slide deck for Acme's renewal",
"draft a follow-up to this call", "review this before I send it". Claude picks
the right skill. You can also type `/` to pick one.

## Making it better over time

When something's off, say so: "too formal", "I never say 'circle back'",
"title slides never have a subtitle". The skill will turn that into a rule.

To save rules into the plugin, open **Customize > Plugins > Forari > Customize**
and say "add these rules to the voice skill" (or presenter). That opens a task
where Claude edits the plugin for you. Your copy is yours, so change anything.

## Adding more skills

Each skill is a folder in `skills/` with a `SKILL.md`. In the Customize task,
describe what you want ("a skill that writes my pre-call brief from the
calendar invite and LinkedIn") and Claude will add it.
