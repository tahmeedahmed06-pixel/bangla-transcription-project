# Bengali text QA — Case 01

- Sample status: Synthetic portfolio sample
- Task type: Customer-support reply
- Verdict: Major revision

## Prompt

একজন গ্রাহক তিন দিন আগে অনলাইনে একটি পণ্য অর্ডার করেছেন। এখনো কোনো tracking update পাননি। তাঁকে ভদ্র ও সহায়ক বাংলায় একটি customer-support reply লিখুন। উত্তরটি 80 শব্দের মধ্যে রাখুন।

## Original AI answer

> প্রিয় গ্রাহক, আপনার মূল্যবান অর্ডার নিয়ে অসুবিধার জন্য আমরা আন্তরিকভাবে দুঃখ প্রকাশ করছি। আপনার অর্ডারটি খুব শীঘ্রই ডেলিভারি করা হবে এবং আমাদের টিম বিষয়টি দেখছে। অনুগ্রহ করে চিন্তা করবেন না, আমরা দ্রুততম সময়ে সমাধান করে দিব। আপনার ধৈর্য এবং সহযোগিতার জন্য ধন্যবাদ।

## QA findings

- `অনুগ্রহ করে চিন্তা করবেন না` বাক্যটি বাদ দেওয়া উচিত। এটি customer-support reply-তে প্রয়োজনীয় তথ্য দেয় না এবং কিছু গ্রাহকের কাছে dismissive মনে হতে পারে।
- `খুব শীঘ্রই ডেলিভারি করা হবে` ও `দ্রুততম সময়ে সমাধান করে দিব`—দুটিই নির্দিষ্ট তথ্য ছাড়া প্রতিশ্রুতি দিচ্ছে।
- গ্রাহকের জন্য কোনো কার্যকর next step নেই, যেমন order number চাওয়া বা status যাচাই করার কথা বলা।
- `আন্তরিকভাবে দুঃখিত` এবং `বিষয়টি আমাদের টিম যাচাই করছে`—এই ধরনের সংক্ষিপ্ত ও সরাসরি ভাষা বেশি উপযোগী।

## Corrected Bengali answer

> প্রিয় গ্রাহক, আপনার অর্ডারের tracking update না পাওয়ায় আমরা আন্তরিকভাবে দুঃখিত। বিষয়টি আমাদের টিম যাচাই করছে। অনুগ্রহ করে আপনার order number পাঠালে আমরা বর্তমান status দেখে আপনাকে update দিতে পারব। সহযোগিতার জন্য ধন্যবাদ।

## English rationale

The response needs a major revision. Although it includes an apology, it makes vague delivery and resolution promises without evidence and does not give the customer a practical next step. The revised answer removes the unnecessary reassurance, avoids unsupported commitments, and asks for the order number so the support team can check the status.
