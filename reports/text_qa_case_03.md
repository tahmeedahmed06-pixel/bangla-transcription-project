# Bengali text QA — Case 03

- Sample status: Synthetic portfolio sample
- Task type: Translation and localization
- Verdict: Major revision

## Prompt

নিচের English customer message-টি বাংলাদেশের ব্যবহারকারীদের জন্য স্বাভাবিক, ভদ্র বাংলায় অনুবাদ করুন। অপ্রয়োজনীয় English শব্দ ব্যবহার করবেন না।

> Your account verification is pending. Please upload a clear photo of your national ID so that we can complete the verification.

## Original AI answer

> আপনার অ্যাকাউন্ট ভেরিফিকেশন পেন্ডিং আছে। প্লিজ আপনার জাতীয় ID-এর একটি ক্লিয়ার ছবি আপলোড করেন, যাতে আমরা আপনার প্রোফাইল ভেরিফাই করতে পারি। ধন্যবাদ।

## QA findings

- `pending`, `প্লিজ`, `clear`, ও `verify` অপ্রয়োজনীয় English mix; এগুলোর স্বাভাবিক Bengali বিকল্প আছে।
- `আপলোড করেন`-এর বদলে ভদ্র অনুরোধ হিসেবে `আপলোড করুন` ব্যবহার করা উচিত।
- `জাতীয় পরিচয়পত্র` ও `যাচাই` ব্যবহার করলে ভাষা বাংলাদেশের ব্যবহারকারীদের কাছে বেশি স্বাভাবিক হয়।
- Source message-এ account verification সম্পন্ন করার কথা আছে; corrected text-এ সেই অর্থ বজায় রাখা হয়েছে।

## Corrected Bengali answer

> আপনার অ্যাকাউন্টের যাচাই প্রক্রিয়া এখনো অপেক্ষমাণ রয়েছে। দয়া করে আপনার জাতীয় পরিচয়পত্রের একটি পরিষ্কার ছবি আপলোড করুন, যাতে আমরা যাচাই প্রক্রিয়াটি সম্পন্ন করতে পারি। ধন্যবাদ।

## English rationale

The answer needs a major revision because it relies on unnecessary English words and uses an unnatural polite form. The revised version uses standard Bengali terminology, corrects the request form, and preserves the original meaning: the account verification is pending and an ID photo is needed to complete it.
