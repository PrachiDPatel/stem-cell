# Stem Cell Design Rules (RULES.md)

Enforceable rules for the AI site generator. Precedence: **client intake constraints first** (`colors_to_avoid`, `design_donts`, `brand_colors`, `color_scheme` are hard requirements and hard vetoes), then these rules, then generator defaults. When a client refines feedback mid-round, the latest instruction wins and earlier versions are dropped.

## 1. Layout and density

1. Group related content into distinct cards with visible surfaces and borders. Never group by whitespace alone.
2. Assign one restrained accent per card or surface, by function — never as decoration. Maximum five accents per site; never show all of them in a single viewport.
3. Categorical color must encode something stable and stated (e.g. color by month, by category). Never color by row index or position.
4. Prefer density over length: collapsible sections (minimized by default), compact rows, and editing beat long scrolling pages.
5. Every section must earn its place. If a block doesn't answer a client or visitor question, cut it.

## 2. Color discipline

6. No rainbow palettes, ever. Muted, restrained, cohesive.
7. `colors_to_avoid` and `design_donts` from intake are absolute vetoes — the QA pass checks the output against them explicitly before delivery.
8. When the client supplies `brand_colors`, build the palette from them. When they don't, pick a restrained house palette and keep it consistent across every page.

## 3. Typography and hierarchy

9. Headers are ALWAYS larger than all their subtext. No exceptions. If a heading and its subheading look like twins, widen the size gap until they can't be confused.
10. Row labels, metadata, and pill text fit on one line — no wrapping. Reduce size before allowing a wrap.
11. Labels are smaller and dimmer than their header; captions are smallest. Each level is visually unambiguous.
12. Data values may be larger than their headers — they are data, not labels. Key figures are big, tabular (`font-variant-numeric: tabular-nums`), and nowrap.

## 4. Data and numbers

13. Prefer distributions over bare averages: ranges, IQR tinting, spread indicators.
14. Color data by position in its own distribution, not by distance to an arbitrary target.
15. Every metric shown must answer a real question. Cut vanity counts and confusing fractions.
16. Comparisons pair the metric with its context (e.g. a row shows both average sleep and average tiredness, not one alone).
17. Averages carry their sample size so thin data can't masquerade as a finding.

## 5. Dark mode and atmosphere

18. Default to dark-mode-first celestial styling unless the client's `color_scheme` says light. Dark surfaces, luminous accents, depth.
19. Decorative atmosphere must befit the context — time of day, brand mood, subject matter each get their own treatment, not one generic backdrop.
20. Stars are pointy (never plain dots), in many sizes and transparencies, dozens to hundreds where the scene calls for it. Add shooting stars and aurora-class effects sparingly, matched to the scene.
21. Optical effects sit strictly behind content and never cost legibility. Content always paints above decoration (position/z-index accordingly). Test text contrast over every decorative layer.

## 6. Motion

22. Motion is slow, smooth, and purposeful. Default ambient pulses around 4s; transitions around 2–2.5s. Nothing frantic.
23. Never remove or freeze an animation the client likes to fix a layout bug — stabilize the layout and keep the motion.
24. Ambient motion varies in size, opacity, delay, and direction. No uniform marching.
25. Decorative animation must never move content or cause layout shift. Pin layout dimensions before animating decorative layers.

## 7. Copy

26. Sparse copy. Few words on screen. If a label needs a sentence to explain it, rewrite the label.
27. Plain, never punchy or sassy. No purple prose, no hype adjectives, no exclamation-point marketing voice.
28. Captions, keys, and legends are concise and minimalist.
29. No lorem ipsum, no placeholder text, no personal or romantic traces in any deliverable. Every word on the page belongs to the client's voice.

## 8. iPhone-first validation

30. The phone is the final judge. Validate every page on a real phone viewport before calling it done.
31. Never claim a visual fix is verified until it is confirmed on the target device.
32. Respect platform rendering quirks: iOS native controls, safe areas, notch, dynamic type. Test, don't assume.
33. Touch targets are at least 44px; tappable rows are full-width.

## 9. Portfolio-grade plainness (no AI artifacts)

34. No AI attribution anywhere: no "built with AI", no "Co-authored-by", no AI footers, no AI-looking commit messages. Commits are plain, lowercase, human, authored as Prachi.
35. No AI-tell visuals: no generic gradient-everywhere hero, no purple-blue blobs, no cookie-cutter SaaS layout, no emoji-as-iconography. Icons are functional (sun, moon, clock), not decorative emoji.
36. Public deliverables ship with working live/demo/download links where applicable, and READMEs that link them.

## 10. QA and delivery gates

37. **Open local before push.** The client approves a staging preview before anything goes live. No exceptions.
38. **One deploy per feedback round.** Batch all approved changes; keep everything local until approval.
39. Run the QA checklist against intake `design_donts` and `colors_to_avoid` before every delivery — that check is what makes this a service, not a generator.
40. Never ask the client for information already in the intake form or earlier in the thread.
41. When a fix isn't visible on the client's device, rebuild fresh — don't relitigate cache.
42. Every change note and reply names the exact screen or section changed, and stays a compact done-list.
43. Own misses in one line, no padding, then fix. No sycophancy: if a requested change will look bad, say so plainly with the reason.
