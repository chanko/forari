---
name: onboarding
description: Set up or redo Forari for Ari by interviewing him. Use when Ari says "set up Forari", "onboard me", "redo my setup", or wants to add a skill for something he keeps doing by hand.
---

# Onboarding

Interview Ari and turn his answers into the files the other Forari skills
read. He's busy: one section at a time, a few questions per message, short
answers are fine, and he can skip anything and come back later.

Open with one line on what this is ("I'll check what you already have, then
ask about your week, your tools, your decks and how you write, about 15
minutes, and set everything up as we go"), then start.

## 0. What you already have

Forari fills gaps. It never replaces something that already works for him.

1. List the skills you can already use outside this folder (from his own
   plugins and skills), with one line on what each does. Ask whether there
   are others, or a folder where he keeps his prompts, templates and files.
2. For each Forari skill (presenter, voice, reviewer), decide with him:
   - **He already has one that does this:** keep his. Remove the Forari one
     from this folder so the two never compete for the same request. If
     his is missing something Forari's has (usually: saving his corrections
     as rules), offer to add just that piece to his, through
     Customize > Plugins > <his plugin> > Customize, and give him the exact
     text to paste.
   - **He has nothing for it:** keep the Forari one.
   - **He doesn't need it:** remove it.
3. If he has a folder with his material (templates, past decks, notes), point
   the kept skills at it instead of copying files in, and write its location
   into the skill's reference file. Tell him that only works where Claude can
   reach that folder (in Cowork, with that folder open).
4. Skip any later section whose skill was removed or is already covered by
   his own. For the sections left, don't ask what his existing skills or
   folder already answer.

## 1. Your week

Ask:
- What do you do by hand over and over that you wish just happened? Top 5,
  rough is fine.
- What does a normal week look like? Calls, emails, decks, CRM updates,
  prospecting, proposals?
- What do you already use Claude for, and where does it let you down?
- If Claude could take one thing off your plate tomorrow, what would it be?

Then pick the 2 or 3 tasks that come up most, that Claude can actually do
with his tools, and that none of his existing skills already handles. For each, propose a skill in one line ("**follow-up**: from
your call notes, writes the recap email in your voice and the CRM update")
and ask which ones he wants. Write the ones he picks as
`skills/<name>/SKILL.md`, following the shape of the existing skills: a
description that says when to use it, the steps, and what good output looks
like. Anything he writes for others uses the voice skill.

## 2. Your tools

Ask:
- Which CRM? (Salesforce, HubSpot, other)
- Gmail or Outlook? Which calendar?
- Where do your files live? (Google Drive, OneDrive, SharePoint, your laptop)
- Do you record or transcribe calls? With what?
- Which Claude plan are you on, and is it your own account or your company's?

For each tool, tell him whether Claude has a connector for it and where to
turn it on (Customize > Connectors). Don't claim a connector exists unless you
can see it in the list. If he's on a company account, say his admin may need
to allow plugins and connectors. Note the tools in the skills that use them.

## 3. Your decks

Ask:
- Do you have a PowerPoint template or brand guide? Drop it in.
- Fonts and colors you always use? Anything you hate seeing on a slide?
- Do you usually send decks as PowerPoint or PDF?
- 2 or 3 decks you're proud of?

Put files in `skills/presenter/assets/` (examples in `assets/examples/`).
Fill in `skills/presenter/references/brand.md`. Read fonts, colors and slide
types from his template and example decks yourself, and only ask him about
what you can't find there.

## 4. Your voice

Ask:
- 10 to 15 things you wrote that sound like you: emails, follow-ups, LinkedIn
  posts, messages to clients. Paste them or drop the files in.
- Words or phrases you'd never use?
- Does your tone change for a cold prospect vs. an existing client vs. an exec?

Save each sample as its own file in `skills/voice/references/samples/`, named
by type (see the README there). Then draft
`skills/voice/references/style-guide.md` from the samples and his answers,
show him the "in one line" summary and the habits, and fix what he says is
wrong.

Last, test it: write one short email he'd really send this week, in his voice,
and ask "does this sound like you?" Turn every correction into a rule in the
style guide.

## Wrapping up

1. Say what's in Forari now, what you removed because he already has it,
   and any text he still has to paste into his own skills.
2. List anything still marked `{{FILL` and which skill it affects. Those
   skills will ask for it when they need it, so it's fine to leave some.
3. If you've been editing a downloaded folder (not an installed plugin), tell
   him to install it: in Finder, right-click the Forari folder > Compress, then
   Customize > Plugins > Add > Upload plugin and pick the zip.
4. Tell him how to keep improving it: correct things as he goes, and save new
   rules through Customize > Plugins > Forari > Customize.
