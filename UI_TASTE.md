# Prachi's UI Taste — Stem Cell Design Philosophy

Distilled September 2026 from the sleep-tracker iteration rounds (30+ local previews in one feedback cycle), her stated rules, and standing notes. Nothing here is invented — every line traces to something she said, corrected, or approved on her iPhone.

## The one-line version

In her words: *"It's not about breathing I want CARDS. color variation. Also less scrolling."* And: *"I don't want too many words on the screen. We want sleek easy data."*

## What belongs on screen

**Cards, not whitespace.** Related content goes in distinct cards with visible surfaces and borders. Grouping by spacing alone reads as unfinished to her. Every card earns its place — when in doubt, cut rather than stack.

**Restrained color, never rainbow.** A small accent palette (3–5 accents per project), each accent assigned to a surface or function: one card periwinkle, one amber, one mauve. Accents signal meaning, never decoration. Categorical color must be stable and meaningful — color by month, not by row index; tint by distribution position, not by vibes.

**Less scrolling.** Density over length. Collapsible sections, minimized by default, beat long pages. If a page keeps growing, the answer is editing, not more page.

**Sparse copy.** Few words on screen. Captions and keys are short. If a label needs a sentence to explain it, the label is wrong.

## Type and hierarchy

**Headers are always larger than all their subtext.** This is her explicit standing rule, stated September 27, 2026 after three rounds of "Notes looks the same size as its subheading." A 2px gap is not a hierarchy — when two adjacent text elements look like twins, widen the size gap until they can't be confused.

**One line, no wrapping.** Row labels, metadata, and pill text fit on a single line. Reduce the size before ever allowing a wrap. (*"I hate wrapping."*)

**Big numbers for what matters.** Key figures are large, tabular, and nowrap. Data values are allowed to be bigger than their headers — they're data, not labels.

## Data presentation

**Distributions over averages.** She trusts IQR tinting, spread charts, and box plots more than a single mean. Color data by position in its own distribution (longer nights blue, shorter nights red relative to her IQR), not by distance to an arbitrary target.

**Every metric must answer a real question.** She killed "1 of 1 nights" as confusing and unhelpful. A comparison earns its place only if it tells her something she doesn't already know — e.g. period nights vs other nights, each row pairing average sleep *and* average tiredness. Vanity counts get cut.

**Small samples stay honest.** Averages carry their sample size ("1 night" / "6 nights") so a thin group can't masquerade as a finding.

## Motion and delight

This is where she lights up. *"I loveeeee clever graphical tricks — colors, shapes, animations."*

**Atmosphere befitting context.** Her bar for the tracker: dusk and dawn look great, so night and day must look equally mesmerizing — each time of day gets its own treatment. Translate that: decorative layers should fit the subject and mood, never be generic.

**Stars done right.** Pointy (not dots), many sizes, many transparencies, dozens to hundreds. Add shooting stars and aurora-class effects where they fit. Twinkle varies in size, opacity, delay, and direction — never uniform marching.

**Slow, smooth, purposeful.** She asked for the pulse to be slowed from 2.6s to 4s. Phase glides run ~2.4s. Nothing frantic, nothing frozen: when a layout bug threatened the sun animation, the fix was to stabilize the layout and *keep* the motion — never kill an effect she likes to patch a bug.

**Decoration never touches content.** Optical effects sit behind content and never cost legibility. (Real bug she caught: sun flare ghosts painting over the form card. Content always paints above decoration.)

## Copy

Plain, not punchy. Never sassy, never purple prose. Short captions, minimal keys. Client deliverables carry zero personal or romantic traces and zero placeholder text. And nowhere — commits, footers, about pages, code — does AI get credited. Her portfolio rule is absolute: no "Co-authored-by", no AI footers, no "built with AI" badges.

## How she iterates (the generator's QA loop should expect this)

**Fast terse bursts, final version wins.** She thinks out loud and refines mid-flight. Act on the latest instruction; when she reverses herself within a minute, the first version never happened. When she tightens a constraint mid-thread, the new constraint snaps the whole plan.

**Her iPhone is the final judge.** Nothing is "verified" until she confirms it on her device. Never claim a visual fix is done before that.

**She debugs mechanisms herself — and she's usually right.** "Do you take into consideration the length of the string?" nailed an iOS rendering bug. Test her hypothesis first, credit it plainly.

**Name the screen.** Her "logging page" and "sleep log page" are two different screens; guessing wrong costs a full round. Every change note says exactly which screen changed.

**Own misses in one line.** No padding, no defensiveness. Then fix it.

**Don't make her repeat herself.** Mine the thread — or the intake form — before asking for anything known. If a fix isn't showing, build a fresh preview instead of relitigating cache. (*"Just make a new preview I still don't see the fix."*)

**No sycophancy, ever.** She detects soft-pedaling instantly and it costs trust. Honest readouts only — including when her own requested change will look bad, with the reason stated plainly.

## Process rules (non-negotiable)

- **Open local before push.** Nobody sees a deploy until the local preview is opened and explicitly approved.
- **One deploy per feedback round.** Batch all approved changes; keep everything local until then.
- **Plain human commits.** Lowercase, comma-separated, descriptive (*"pattern card refinements, period sleep and tiredness"*). Authored as her. No AI-looking messages, ever.
- **Results over hype.** *"Don't go off hype — go off results."* Recommendations cite observed outcomes, not trends.

## Hate list (instant rejection)

Rainbow palettes. Whitespace-only grouping. Cramped monotonous forms. Walls of words. Wrapping labels. Headers smaller than their subtext. Vanity metrics. Sassy marketing copy. Purple prose. AI credit anywhere. Uniform marching animations. Decoration over content. Being asked twice for the same thing.
