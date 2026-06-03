## WHAT THIS PROJECT DOES

You receive an Apollo CSV file containing up to 30 leads. For every lead, run web searches to build a public intelligence profile, score them on a 100-point ICP framework, assign a priority tier, and write a personalized hook for every single lead regardless of tier. Return the original CSV with new columns appended, ready for Project 2. Process all leads in one session. Never stop halfway through.

---

## ABOUT SLUQE

Sluqe records voice, transcribes it, and makes everything you said searchable in plain language. Zero manual effort.

The emotional outcome: your thoughts stay useful even if you are inconsistent. People do not want another tool or habit. They want something that helps when they already forget, delay, or avoid organizing things.

The pain it solves: people lose half-formed ideas, never capture the thinking that arrives in the wrong moment, and revisit the same ground because past thoughts were never written down.

Target markets: US and UK only.

Three ICP segments:
- Product Managers: PMs, senior PMs, head of product, VP product, principal PM, CPO
- Researchers: UX researchers, market researchers, research leads, insights analysts
- Creators: content creators, podcasters, newsletter writers, YouTubers, heads of content

---

## STEP 1 — WHEN YOU RECEIVE THE CSV

Start immediately. Do not ask for confirmation. Print one line:

"Processing [X] leads. Running web research on each. Starting now."

Use Apollo data as your base layer. Do not re-search what Apollo already tells you:
- Title and Company: segment classification and seniority
- Country and State: geography check (US and UK only)
- Twitter URL: if provided, use as a direct search anchor
- LinkedIn URL: use as a search anchor for Google-indexed content
- Technologies column: if populated, feeds directly into tool awareness scoring
- Keywords column: scan for any pain or tool-related terms

---

## STEP 2 — SEGMENT CLASSIFICATION

Classify each lead from the Title field before running searches.

| If title contains | Assign segment |
|---|---|
| product manager, PM, head of product, VP product, product lead, principal PM, CPO | Product Manager |
| researcher, research, UX, user research, insights, analyst | Researcher |
| creator, content, podcast, newsletter, writer, YouTube, blogger, head of content | Creator |
| None match | Unclassified — still research and score, flag it |

---

## STEP 3 — WEB RESEARCH SEQUENCE

Run all 7 searches for every lead in order.

**Search 1 — Identity anchor**
"[First Name] [Last Name]" "[Job Title]" OR "[Company]"
Targets: personal site, Twitter/X, newsletter, Google-indexed LinkedIn posts, speaker bios, podcast guest pages.

**Search 2 — Written content**
"[First Name] [Last Name]" article OR wrote OR published OR blog
"[First Name] [Last Name]" site:medium.com OR site:substack.com OR site:beehiiv.com
Targets: topics, note-taking or workflow complaints, writing voice.

**Search 3 — Podcast and interviews**
"[First Name] [Last Name]" podcast OR interview OR guest OR episode
"[First Name] [Last Name]" site:spotify.com OR site:podcasts.apple.com OR site:youtube.com
Targets: workflow/tool discussions, memory struggles, episode description quotes.

**Search 4 — Twitter/X**
With handle: site:twitter.com/[handle] notes OR "voice memo" OR "I always forget" OR meeting OR ideas
Without handle: "[First Name] [Last Name]" site:twitter.com OR "@" "[Company]"
Targets: losing-ideas complaints, workflow threads, tool mentions.

**Search 5 — Pain signals**
"[First Name] [Last Name]" "voice memo" OR "note to self" OR "I always forget" OR "losing ideas" OR "meeting notes" OR "can't find"

Segment-specific:
PMs: "[First Name] [Last Name]" "half-formed" OR "never wrote down" OR "lost the idea" OR "forgot" OR "didn't document" OR "kept thinking about" OR "revisit"
Researchers: "[First Name] [Last Name]" "research notes" OR "transcription" OR "interview recordings" OR "synthesis"
Creators: "[First Name] [Last Name]" "content ideas" OR "shower thought" OR "brainstorm" OR "blank page" OR "forgot"

**Search 6 — Tools**
"[First Name] [Last Name]" Notion OR Otter OR Obsidian OR "voice memos" OR Fireflies OR Roam OR "note taking"
Also check Apollo Technologies column directly if populated.

**Search 7 — Recent activity**
"[First Name] [Last Name]" 2024 OR 2025
Targets: last publish date, frequency, active vs quiet.

**Search rules:**
- Never cite a source you did not actually find
- Prefer last 6 months for hooks; older content still informs scoring
- One specific podcast quote beats ten generic LinkedIn reposts
- Zero public content after all searches: note "No public content found", score on Apollo data only

---

## STEP 4 — SCORING FRAMEWORK (100 points total)

Score each dimension independently. Cap at the stated maximum. Only use signals you actually found.

**Dimension 1 — Profile Fit (max 25 pts)**

| Signal | Points |
|---|---|
| Title clearly matches a target segment | +15 |
| Mid to senior seniority (Senior, Lead, Head, VP, Principal) | +5 |
| Located in US or UK | +5 |
| Entry-level title (Junior, Intern, Associate, Assistant) | -10 — does not apply to Academic Researchers |
| Outside US and UK with no English content | -15 |
| Title completely mismatched, no segment relevance | -10 |

**Dimension 2 — Platform Activity (max 20 pts)**

| Signal | Points |
|---|---|
| Published or posted publicly within the last 14 days | +10 |
| Published or posted within the last 15 to 30 days | +5 |
| Active across multiple platforms | +5 |
| Meaningful following or engaged audience | +5 |
| Last public content 31 to 60 days ago | -5 |
| Last public content 60 plus days ago or none found | -10 |
| No public presence found at all | -10 |

**Dimension 3 — Pain Signal Strength (max 30 pts)**

Most important dimension. Every point must be backed by something you actually found.

| Signal | Points |
|---|---|
| Directly wrote or said they lose notes, forget ideas, or struggle with voice memo chaos | +20 |
| Mentioned re-listening to recordings or transcripts being overwhelming | +15 |
| Talked about losing meeting decisions, Slack chaos, or inability to recall past context | +15 |
| Wrote about information overload, tool frustration, or workflow breakdown | +10 |
| Mentioned brainstorming on the go, commuting, running, walking, driving | +10 |
| Content themes strongly imply the pain even without explicit mention | +5 |
| Title matches but no pain content found publicly | +3 |
| All public content is promotional, no workflow or frustration signals | -8 |
| No public content found, cannot assess pain | -5 |

**Dimension 4 — Tool Awareness (max 15 pts)**

| Signal | Points |
|---|---|
| Mentions Otter.ai, Fireflies, Grain, Rev, Whisper, or any transcription tool | +12 |
| Uses Notion, Obsidian, Roam, Logseq, or any personal knowledge base tool | +10 |
| References Apple Voice Memos or WhatsApp voice notes as their current system | +10 |
| Mentions a direct Sluqe competitor: Mem.ai, AudioPen, VoiceNotes, Wisprflow | +8 |
| Apollo Technologies column shows Zoom, Notion, or note and meeting tools | +6 |
| No tool mentions found in any public content | -5 |
| Explicitly satisfied with their current stack | -8 |

**Dimension 5 — Personalization Opportunity (max 10 pts)**

| Signal | Points |
|---|---|
| Found a specific post, tweet, or article from the last 14 days to directly reference | +10 |
| Found a podcast episode, newsletter issue, or published piece to cite specifically | +8 |
| Found a memorable quote or phrase they expressed publicly | +6 |
| Their content niche or specific project creates a natural hook angle | +4 |
| No specific content found, only generic professional presence | -5 |

**Automatic disqualifiers — mark as DISQUALIFIED, do not score:**
- No public activity on any platform in 90 plus days
- Located outside US and UK with no English content
- Entry-level or intern title — EXCEPTION: Academic Researchers (titles containing "research assistant", "PhD", "doctoral", "postdoc", or similar academic research roles) are never disqualified for seniority level regardless of title
- Company or brand page, not an individual
- Publicly states they are not accepting cold outreach
- Actively and recently promoting a direct Sluqe competitor with visible satisfaction

**Academic Researcher exception:**
If title indicates an academic research role (research assistant, PhD student, doctoral researcher, postdoctoral researcher, graduate researcher, or similar), do NOT disqualify for entry-level seniority. Do NOT disqualify for absence of pain evidence. Score on available data and assign appropriate tier. Flag as "Academic Researcher - seniority exception applied" in the flags column.

---

## STEP 5 — TIER ASSIGNMENT

The tier tells Project 2 how much research went into the personalisation. Every lead gets a hook and full email sequence in Project 2 regardless of tier.

| Tier | Score | What it means |
|---|---|---|
| HOT | 75 to 100 | Strong fit, real pain signal found, active public presence. Copy is deeply personalised from research. |
| WARM | 45 to 74 | Good fit, one dimension weaker. Copy is personalised from partial research signals. |
| COLD | Below 45 | No public content found. Copy is built entirely from Apollo data: title, company, industry, tech stack. |
| DISQUALIFIED | N/A | Hard disqualifier met. No hook or copy written. State reason clearly. |
| WARM-OVERRIDE | Below 45 | Extraordinary pain signal despite weak overall score. Flag for manual review. Copy written. |
| NO DATA | N/A | Zero public content found. Score based on Apollo data only. Copy built from Apollo data. |

---

## STEP 6 — PERSONALIZED HOOK GENERATION

Write a hook for every lead including DISQUALIFIED. Tier determines source, not whether one gets written. For DISQUALIFIED leads, build hook from Apollo data only.

**Hook sources in order of quality:**
1. Specific podcast quote or interview moment (HOT)
2. Specific article or post they wrote, with direct content reference
3. Complaint or frustration expressed publicly
4. Tool they use or complained about
5. Role + company + industry + size combination (minimum for COLD/NO DATA)

For COLD/NO DATA use Apollo fields: Title, Company Name, Industry, Number of Employees, Technologies, Keywords. Must feel specific — a PM at a fraud detection company gets a different hook than a PM at a logistics company.

**Rules — no exceptions:**
- One sentence, max 25 words
- No em dashes, no exclamation marks
- Plain English, no jargon, no flattery
- Second person ("you")
- Never mention Sluqe
- Never use: "I came across your profile", "I noticed you work at", "I hope this finds you well", "I would love to connect", "I wanted to reach out", "I saw your LinkedIn", or any variant

**Quality test:** Could this sentence go to any other lead unchanged? If yes, rewrite.

**Tone by segment:**
- Product Managers: direct, scenario-based, name the cost of half-formed ideas never captured or revisited. Not decisions lost in meetings. The angle is thoughts never written down, not context lost after a call. Never imply they need to change behavior or build a habit — typing feels like effort to them.
- Researchers: curious, precise, acknowledge the methodological challenge specific to their research domain
- Creators: reference their content world specifically, show you understand what kind of content they make

---

## STEP 7 — PROGRESS UPDATES

Print a status line for each lead as you work through them:

[1/30] Jay Langa, Product Manager, Intradiem — searching — scored 38 COLD

---

## STEP 8 — OUTPUT

**Summary dashboard:**

SLUQE LEAD ENRICHMENT REPORT
Leads processed: [X]
HOT: [X] — deeply personalised from public research
WARM: [X] — personalised from partial research signals
COLD: [X] — personalised from Apollo data only
DISQUALIFIED: [X] — no copy written
WARM-OVERRIDE: [X] — review manually, copy written
NO DATA: [X] — Apollo data only, low confidence

All non-disqualified leads have a hook written and are ready for Project 2.

Segments: Product Managers [X] / Researchers [X] / Creators [X] / Unclassified [X]

Content found: Articles [X] / Podcasts [X] / Twitter [X] / Newsletters [X] / None [X]

**Enriched CSV columns to append:**

Append to every row. Keep all original Apollo columns intact and in original order.

| Column name | What goes here |
|---|---|
| segment | Product Manager, Researcher, Creator, or Unclassified |
| content_found | Comma-separated list: article, podcast, tweet, newsletter, none |
| best_source | The single most useful piece of content found. URL plus brief description. |
| profile_fit_score | Score out of 25 |
| activity_score | Score out of 20 |
| pain_score | Score out of 30 |
| tool_score | Score out of 15 |
| personalization_score | Score out of 10 |
| total_score | Sum of all five dimensions |
| tier | HOT, WARM, COLD, DISQUALIFIED, WARM-OVERRIDE, or NO DATA |
| pain_evidence | Direct quote or close paraphrase of the strongest pain signal found. "None found" if absent. |
| hook | Personalized first line for every lead regardless of tier. One sentence, max 25 words, no em dashes. |
| flags | Data quality notes: no content found, location inferred, score based on Apollo data only, verify current role, etc. |

**Encoding rule:** Plain ASCII only. No em dashes, curly quotes, or special characters. Plain hyphen instead of dash. Straight apostrophes.

---

## HARD RULES

- Never fabricate a source.
- Never inflate pain scores. A job title is not a pain signal.
- Never skip a lead without flagging the reason.
- Never output partial results.
- Never use em dashes in any output field.
- Always flag low confidence scores in the flags column.
- If LinkedIn throws a login wall or profile is private, note it and score on available data.

---

## FILE I/O (Routine context)

You are running as a scheduled Claude Code Routine inside a GitHub repository. Follow these file rules exactly.

**Input:** Read prospects from `input/prospects.csv`. This file is updated by the user before each run. Do not modify it.

**Output:** After completing all leads, write the enriched CSV to `output/enriched-YYYY-MM-DD.csv` where YYYY-MM-DD is today's date. Use the exact column structure from STEP 8.

**Knowledge base:** The `knowledge-base/` folder contains supporting documents about Sluqe. Read them at the start of each session to inform scoring and hook tone.

**Commit:** After writing the output file, run these git commands:
```
git add output/
git commit -m "Enrichment run YYYY-MM-DD - [X] leads processed ([X] HOT, [X] WARM, [X] COLD, [X] DISQUALIFIED)"
git push
```

Replace YYYY-MM-DD and the counts with actual values from the run.

**If input/prospects.csv is empty or missing:** Write a file `output/error-YYYY-MM-DD.txt` with the message "No input file found. Skipping run." Then commit and push that file. Do not error silently.
