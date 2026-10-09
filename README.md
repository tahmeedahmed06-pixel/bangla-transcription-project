# Bengali AI language evaluation portfolio

This completed personal portfolio project combines Bengali transcript verification, audio-language evaluation, and rubric-based Bengali AI-text QA. A concise overview and CV-ready wording are available in `PORTFOLIO_SUMMARY.md`.

## Project layout

- `audio/` contains the two audio/video samples.
- `data/` contains the `clip_01` transcripts and final error analysis.
- `reports/` contains the two audio evaluations, the `clip_02` source/licence record, six synthetic text-QA cases, the workflow guide, and the portfolio summary.

## Bengali ASR evaluation: clip_01

This small project compares an ElevenLabs machine transcript with a user-supplied verified Bengali transcript for `clip_01.webm`.

## Files

- `audio/clip_01.webm` — original audio/video source.
- `data/clip_01_machine.txt` — ElevenLabs machine transcript.
- `data/clip_01_verified.txt` — user-supplied verified transcript. It is treated as the reference and kept verbatim.
- `data/error_analysis.csv` — a manually aligned, evidence-based list of observed differences between the machine and verified texts.
- `reports/clip_01_audio_evaluation.md` — human listening evaluation for the first clip.
- `audio/clip_02.ogg` and its supporting evaluation and licence record in `reports/` — second audio-evaluation sample.

`clip_01_draft.txt` is not included because it was identical to `clip_01_verified.txt` and added no separate evidence.

The original audio and source transcript files are not modified by this project. The two deliverables are the CSV and this README.

## Method

The comparison follows the written transcript order. Each CSV row pairs a machine passage with the corresponding verified passage and labels the observed type of difference. The review preserves the verified transcript's fillers, repetitions, restarts, punctuation, spacing, spelling forms, and token splitting as supplied. Physical line wraps from the `.txt` files are converted to spaces inside CSV cells when a passage crosses a displayed line; they are not treated as spoken or transcription differences.

`start_time` and `end_time` are deliberately blank. None of the supplied text files contains segment-level timestamps, and this review does not infer timestamps from reading or listening. `alignment_status` is `clear` only when the matching transcript passages are plainly in the same sequence; it is not an audio time alignment claim.

## What the comparison shows

The machine transcript is substantially more normalized than the verified transcript. It commonly removes fillers and false starts (for example, `আআ`, `সোওও`, and repeated partial phrases), combines or changes tokenization such as `উইকি টাং এ`/`উইকিটাঙ্গে`, and changes some wording. The most material content difference is the speaker name: the machine text says `নুরুল নবী চৌধুরী হাসিব`, while the verified transcript says `নুরুন্নবী চৌধুরী আসিফ`.

Some rows are strict verbatim differences rather than clear semantic mistakes. For example, `২০০৮` versus `দুই হাজার আট`, or `আরো` versus `আরও`, may preserve the intended meaning but do not match the supplied reference exactly. The CSV labels these separately so that a later evaluation can decide whether to score them as ASR errors, normalization differences, or annotation-convention differences.

## Limits and follow-up

This is a transcript-to-transcript comparison, not a timestamped audit. A formal word-error-rate calculation should first define a normalization policy for Bengali spelling variants, number formatting, fillers, hesitations, restarts, punctuation, and split/joined words. If timing is needed, generate or manually verify timestamped segments against the audio before populating the timestamp columns.

## clip_01 audio language evaluation

The user-provided `clip_01.webm` was also reviewed as an audio-language sample. The listening evaluation identified frequent pauses and repeated non-lexical fillers, some unclear or potentially incorrect pronunciations, limited natural intonation, and unnecessary volume increases. No individual pronunciation examples or timestamps are claimed because they were not separately documented.

| Category | Score | Summary |
| --- | ---: | --- |
| Fluency | 2/5 | Frequent pauses, delays, and repeated fillers disrupted the speech flow. |
| Pronunciation | 3/5 | Some words were unclear or perceived as mispronounced. |
| Intonation | 2/5 | Limited natural variation; unnecessary raising of the voice was noted. |
| Intelligibility / Clarity | 3/5 | Generally understandable, but reduced by the issues above. |

Detailed English rationales are in `clip_01_audio_evaluation.md`.

## clip_02 অডিও ভাষা মূল্যায়ন

`clip_02.ogg` একটি আলাদা Bengali speech sample হিসেবে মূল্যায়ন করা হয়েছে। উৎসটি Wikimedia Commons-এর [Speech by Anubrata Manda (Bengali).ogg](https://commons.wikimedia.org/wiki/File:Speech_by_Anubrata_Manda_(Bengali).ogg); লাইসেন্স [CC BY-SA 3.0](https://creativecommons.org/licenses/by-sa/3.0/). Portfolio-তে ব্যবহার করলে title, author Jim Cartar, source link, এবং licence উল্লেখ করতে হবে।

| বিষয় | স্কোর | সংক্ষিপ্ত ফলাফল |
| --- | ---: | --- |
| Fluency | 5/5 | বক্তৃতার প্রবাহ স্বাভাবিক ও ধারাবাহিক। |
| Pronunciation | 3/5 | কয়েকটি শব্দের উচ্চারণে সমস্যা পাওয়া গেছে। |
| Intonation | 4/5 | স্বরভঙ্গি মোটের ওপর স্বাভাবিক। |
| Intelligibility / Clarity | 4/5 | সাধারণভাবে বোঝা যায়; কয়েকটি শব্দের উচ্চারণ clarity কমিয়েছে। |

Pronunciation review-এ `প্রার্থী` শব্দটি একাধিকবার ভুল উচ্চারণ করা হয়েছে। `এসেছি`-র বদলে `এসছি` এবং `প্রশাসন`-এর বদলে `পোশাসন` শোনা গেছে। `জ্বালিয়ে` শব্দটির উচ্চারণ অস্পষ্ট ছিল; তাই এটিকে নিশ্চিত error না বলে unclear observation হিসেবে রাখা হয়েছে। কোনো timestamp যোগ করা হয়নি, কারণ audio player-এ সেগুলো আলাদা করে যাচাই করা হয়নি। বিস্তারিত মূল্যায়ন `clip_02_audio_evaluation.md`-এ আছে.

## Bengali text QA

প্রথম text-QA sample-এ একটি Bengali customer-support reply review করা হয়েছে। এটি একটি synthetic portfolio sample। Verdict হলো `Major revision`, কারণ original answer-এ অস্পষ্ট প্রতিশ্রুতি ছিল এবং গ্রাহকের জন্য কোনো কার্যকর next step দেওয়া হয়নি। Corrected version-এ order number চেয়ে status যাচাই করার স্পষ্ট পরামর্শ যোগ করা হয়েছে। বিস্তারিত review, corrected Bengali answer, এবং English rationale `text_qa_case_01.md`-এ আছে।

দ্বিতীয় text-QA sample-এ একটি formal academic email review করা হয়েছে। এটিও synthetic portfolio sample এবং verdict `Major revision`। Original answer-এ email subject, proper closing, এবং formal register ছিল না। Corrected email-এ subject line, সংক্ষিপ্ত কারণ, দুই দিনের সময় চাওয়ার নির্দিষ্ট অনুরোধ, এবং formal closing যোগ করা হয়েছে। বিস্তারিত review `text_qa_case_02.md`-এ আছে।

তৃতীয় text-QA sample-এ বাংলাদেশের ব্যবহারকারীদের জন্য একটি customer message-এর translation ও localization review করা হয়েছে। এটিও synthetic portfolio sample এবং verdict `Major revision`। `pending`, `প্লিজ`, `clear`, ও `verify`-এর মতো অপ্রয়োজনীয় English mix বাদ দিয়ে স্বাভাবিক Bengali ব্যবহার করা হয়েছে; `আপলোড করেন`-ও `আপলোড করুন` করা হয়েছে। বিস্তারিত review `text_qa_case_03.md`-এ আছে।

চতুর্থ text-QA sample-এ factuality ও hallucination review করা হয়েছে। এটিও synthetic portfolio sample এবং verdict `Major revision`। Original answer-এ UNESCO-র অনুমোদনের সাল এবং বিশ্বজুড়ে পালন শুরুর সাল—দুটিই ভুল ছিল। [UNESCO-এর official page](https://www.unesco.org/en/days/mother-language) অনুযায়ী ১৯৯৯ সালে অনুমোদন হয় এবং ২০০০ সাল থেকে দিবসটি পালিত হচ্ছে। বিস্তারিত review ও corrected answer `text_qa_case_04.md`-এ আছে।

পঞ্চম text-QA sample-এ banking SMS phishing নিয়ে safety review করা হয়েছে। এটি synthetic portfolio sample এবং verdict `Fail`, কারণ original answer অচেনা link-এ click করতে এবং card number ও OTP দিতে বলেছিল। Corrected answer-এ link এড়িয়ে চলা, PIN/OTP না দেওয়া, এবং independently verified official channel-এ bank-এর সঙ্গে যোগাযোগ করার নির্দেশনা দেওয়া হয়েছে। বিস্তারিত review `text_qa_case_05.md`-এ আছে।

ষষ্ঠ text-QA sample-এ audience, tone, এবং instruction-following review করা হয়েছে। এটি synthetic portfolio sample এবং verdict `Major revision`। Original explanation তথ্যগতভাবে মোটের ওপর ঠিক ছিল, কিন্তু পঞ্চম শ্রেণির শিক্ষার্থীর উপযোগী ছিল না এবং English শব্দ ব্যবহার না করার নির্দেশ মানেনি। Corrected answer-এ সহজ বাংলা, ছোট বাক্য, এবং 60 শব্দের সীমা রাখা হয়েছে। বিস্তারিত review `text_qa_case_06.md`-এ আছে।
