# Phase 2: Bengali audio evaluation and language QA

This phase extends the existing `clip_01` transcription review. It contains two portfolio sections: Bengali audio-quality evaluation and Bengali AI-text quality assurance. The work should be presented as personal portfolio samples, not client work.

## Working rule

Make each judgment traceable. Do not invent timestamps, scores, dialect labels, factual sources, or audio problems. If a point cannot be heard or verified, write `unclear` and explain what would be needed to decide it.

## Section A — Audio language evaluation

### Goal

Show that you can listen to Bengali speech and assess fluency, pronunciation, intonation, and intelligibility. This is different from producing a transcript.

### Minimum portfolio scope

Evaluate two short clips, ideally 30–90 seconds each. `clip_01.webm` can be the first clip. Use a second clip with a different speaker, recording condition, or speaking style if possible.

### Evaluation workflow for each clip

1. Listen once without writing scores. Note the general speech style and whether the recording is understandable.
2. Listen again and give a 1–5 score for each category below.
3. Write a concise English rationale for each score. Point to an audible feature; add a timestamp only if it has been checked against the audio.
4. Mark the result `unclear` instead of guessing where noise, uncertainty, or a short sample prevents a fair rating.

| Category | What to judge | Score meaning |
| --- | --- | --- |
| Fluency | Pauses, hesitations, restarts, and flow of speech | 1 = frequent disruption; 3 = understandable with noticeable disruption; 5 = consistently natural flow |
| Pronunciation | Clarity and articulation of Bengali words | 1 = often difficult to understand; 3 = mostly clear; 5 = consistently clear |
| Intonation | Natural pitch, stress, phrasing, and sentence rhythm | 1 = frequently unnatural or flat; 3 = generally natural with issues; 5 = consistently natural |
| Intelligibility | How easily a listener can understand the recording | 1 = hard to follow; 3 = understandable with effort; 5 = easy to follow |

### Required record fields

`clip_id`, `audio_length`, `review_status`, `fluency_score`, `pronunciation_score`, `intonation_score`, `intelligibility_score`, `English_rationale`, `evidence_timestamp`, `uncertainty_note`.

Leave `evidence_timestamp` blank unless it is verified from the audio. The score is an assessment of the sample, not a claim about the speaker as a person.

### Definition of done

Two clips have all four scores, clear English rationales, and honest uncertainty notes. The reviewer can understand why each score was assigned without being asked to trust a vague opinion.

## Section B — Bengali AI text QA

### Goal

Show that you can review Bengali AI output using a consistent rubric, explain the issue in English, and produce a better Bengali version.

### Minimum portfolio scope

Create six cases across different types of everyday work. A useful mix is: customer-support reply, formal email, education explanation, everyday conversation, translation/localization, and factual question.

For every case, keep the original prompt and the unedited AI answer. If you generate the sample answer yourself, label it `synthetic portfolio sample`.

### QA rubric

| Category | Pass means | Common failure |
| --- | --- | --- |
| Instruction following | The answer completes the prompt's requested task | Misses format, language, length, or requested detail |
| Meaning and factuality | Claims are accurate or properly qualified | Wrong fact, mistranslation, contradiction, unsupported claim |
| Bengali quality | Grammar, spelling, and sentence construction are natural | Incorrect grammar, awkward literal translation, unnecessary English mix |
| Tone and register | Tone suits the reader and situation | Casual language in a formal message, overly formal wording in a chat |
| Cultural fit | The wording makes sense for Bengali-speaking users | Inappropriate honorific, date/reference issue, unnatural local context |
| Clarity and safety | The answer is understandable and does not introduce harmful or misleading advice | Ambiguity, unsafe advice, unclear instruction |

### Workflow for each case

1. Save the Bengali prompt and original AI answer.
2. Choose one verdict: `Pass`, `Minor revision`, `Major revision`, or `Fail`.
3. Select only the rubric categories that actually apply.
4. Quote the short problem passage or describe the precise issue.
5. Write a corrected Bengali answer. Preserve any part that was already good.
6. Add a two- to four-sentence English rationale that explains the verdict and correction.
7. For factual claims, add a real source link or label the claim as unverified. Do not present a guess as fact-checking.

### Required record fields

`case_id`, `task_type`, `prompt_bn`, `model_answer_bn`, `verdict`, `error_categories`, `issue_evidence`, `corrected_answer_bn`, `English_rationale`, `source_or_verification_note`, `sample_status`.

### Definition of done

Six cases are complete. Each has an original answer, an evidence-based verdict, a correction where needed, and an English explanation. At least one case should be a factual claim with a real verification source or an explicit note that it could not be verified.

## Tonight's order of work

1. Select the two clips for Section A. Use `clip_01` as the first only after listening and scoring it.
2. Finish two audio-evaluation records before moving on.
3. Prepare six Bengali prompts and their AI answers for Section B.
4. QA and revise one case at a time; do not write all verdicts first and justify them later.
5. Put the finished examples in the main project README under `Audio evaluation` and `Bengali text QA`.

## Honest CV language after this phase

**Bengali AI Language Evaluation Portfolio (Personal Project)** — Reviewed Bengali speech for fluency, pronunciation, intonation, and intelligibility; performed rubric-based QA of Bengali AI responses; documented evidence, revisions, and concise English rationales.

Use this only after the two audio records and six QA cases are genuinely complete.
