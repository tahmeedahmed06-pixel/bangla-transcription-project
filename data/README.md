# Bengali ASR evaluation: clip_01

This small project compares an ElevenLabs machine transcript with a user-supplied verified Bengali transcript for `clip_01.webm`.

## Files

- `clip_01.webm` — original audio/video source.
- `clip_01_machine.txt` — ElevenLabs machine transcript.
- `clip_01_verified.txt` — user-supplied verified transcript. It is treated as the reference and kept verbatim.
- `clip_01_draft.txt` — duplicate of the verified transcript at the time of review.
- `error_analysis.csv` — a manually aligned, evidence-based list of observed differences between the machine and verified texts.

The original audio and source transcript files are not modified by this project. The two deliverables are the CSV and this README.

## Method

The comparison follows the written transcript order. Each CSV row pairs a machine passage with the corresponding verified passage and labels the observed type of difference. The review preserves the verified transcript's fillers, repetitions, restarts, punctuation, spacing, spelling forms, and token splitting as supplied. Physical line wraps from the `.txt` files are converted to spaces inside CSV cells when a passage crosses a displayed line; they are not treated as spoken or transcription differences.

`start_time` and `end_time` are deliberately blank. None of the supplied text files contains segment-level timestamps, and this review does not infer timestamps from reading or listening. `alignment_status` is `clear` only when the matching transcript passages are plainly in the same sequence; it is not an audio time alignment claim.

## What the comparison shows

The machine transcript is substantially more normalized than the verified transcript. It commonly removes fillers and false starts (for example, `আআ`, `সোওও`, and repeated partial phrases), combines or changes tokenization such as `উইকি টাং এ`/`উইকিটাঙ্গে`, and changes some wording. The most material content difference is the speaker name: the machine text says `নুরুল নবী চৌধুরী হাসিব`, while the verified transcript says `নুরুন্নবী চৌধুরী আসিফ`.

Some rows are strict verbatim differences rather than clear semantic mistakes. For example, `২০০৮` versus `দুই হাজার আট`, or `আরো` versus `আরও`, may preserve the intended meaning but do not match the supplied reference exactly. The CSV labels these separately so that a later evaluation can decide whether to score them as ASR errors, normalization differences, or annotation-convention differences.

## Limits and follow-up

This is a transcript-to-transcript comparison, not a timestamped audit. A formal word-error-rate calculation should first define a normalization policy for Bengali spelling variants, number formatting, fillers, hesitations, restarts, punctuation, and split/joined words. If timing is needed, generate or manually verify timestamped segments against the audio before populating the timestamp columns.
