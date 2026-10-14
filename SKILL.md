---
name: arabic-native
description: Write, rewrite, translate or review Arabic so it reads as if a native writer wrote it first, never word-for-word from English. Covers UI and app copy, marketing, social posts, WhatsApp and notifications, articles and scripts, with Saudi/Gulf as the default audience. Use whenever Arabic text is produced or checked, including "translate to Arabic", "localize", "Arabic version", and Arabic captions or slogans.
author: Hatem Abusitta (حاتم أبو ستة)
license: CC BY 4.0
---

# Arabic, written native

*By Hatem Abusitta · حاتم أبو ستة*

Most Arabic produced by machines and rushed translators is **correct but foreign**. It is grammatical Arabic that no Arab would actually say. Readers notice in one line: English word order, «قم بـ», «الخاص بك», «يتم … بنجاح», clichés like «أطلق العنان». This skill writes Arabic **from the meaning**, in the register the reader lives in.

The one test for every line: **would a native writer who never saw the English write exactly this?** If not, rewrite it.

## How to work

1. **Pin the reader and the moment.** Who reads it (a customer, an engineer, a teenager on TikTok, a ministry), in which country, on which surface (button, ad, contract, push notification, caption), and what they must understand or do. Default audience: **Saudi Arabia / the Gulf**, unless told otherwise.
2. **Choose one register** (table below) and keep to it for the whole piece. Never mix registers or dialects in one piece.
3. **Write the Arabic from the meaning.** Use the English, if there is one, only as a brief. Don't follow its sentence shape. Restructure freely: verb-first, shorter, split or merge sentences. Then check the facts still match.
4. **Run the check** at the end of this file. For anything beyond a few lines, load the matching reference.
5. **Say what you weren't sure of.** Flag slang, puns, product names and anything marked [observed / verify] for a native reviewer. Don't present guesses as rules.

## Pick the register

| Surface | Register |
|---|---|
| App and web UI labels, buttons, settings, errors | **Simple modern MSA** (فصحى سهلة): short, clear, warm |
| Contracts, legal, government, banking terms, B2B, press | **Formal MSA** |
| Push notifications, social posts, ads, influencer scripts (consumer, Saudi audience) | **White Saudi dialect** (لهجة بيضاء): Saudi, but without strong regional markers |
| WhatsApp and SMS to customers | Polite white dialect, or simple MSA. Short. |
| Pan-Arab audience | MSA, or separate dialect versions per market |
| Children, education, Quran or poetry quotes | MSA with full vowel marks |

Details and the evidence behind this: `references/dialects-and-new-generation.md`.

## The rules that fix most text

**Kill the calques** (full list in `references/translation-pitfalls.md`):

| Literal | Native |
|---|---|
| قم بالضغط / قم بإضافة | اضغط / أضِف |
| كلمة المرور الخاصة بك | كلمة مرورك |
| يتم إرسال الرمز | نرسل لك الرمز · يُرسَل الرمز |
| تم الحفظ بنجاح | تم الحفظ · حُفظت التغييرات |
| من قِبَل المسؤول | (active voice) أنشأ المسؤول… |
| دعنا نبدأ | لنبدأ · يلا نبدأ (casual) |
| هل أنت متأكد أنك تريد حذف…؟ | حذف الصورة؟ |
| فشل… | تعذّر… |
| من خلال / عبر (everywhere) | بـ · على |
| في عالم اليوم المتسارع، أطلق العنان، رحلة، تجربة لا مثيل لها | delete; say the actual benefit |

**Grammar that machines get wrong:**
- **Non-human plurals take feminine singular agreement:** «الطلبات جاهزة», «لا توجد رسائل».
- **Numbers** have six forms in Arabic:
  - 0: rephrase («لا توجد…»)
  - 1: «رسالة واحدة»
  - 2: the dual, «رسالتان»
  - 3–10: plural noun, with the number in the opposite gender: «ثلاث رسائل», «ثلاثة كتب»
  - 11–99: singular accusative noun: «خمسون ريالًا»
  - 100 and up: singular genitive noun: «مئة ريال»

  Never glue a sentence from fragments around a number. Use a full string per form (ICU plural rules).
- **Hamza on UI verbs:** form IV keeps it («أرسِل، أضِف، أدخِل، إرسال، إضافة»); forms VII, VIII and X don't («اختر، استخدم، اشترك، انضم»).
- **Spelling that marks careless text:**
  - ة vs ه: «مكتبة» is a library, «مكتبه» is "his office"
  - ى vs ي: «على» vs «علي»
  - ض vs ظ: «نضارة» is radiance, «نظارة» is glasses
  - «إن شاء الله», never «إنشاء الله»
  - «الآن», «مسؤول» (Gulf spelling)

**Address the reader without awkward slashes.** Use verbal nouns for buttons («حفظ، إرسال، تسجيل الدخول»). Use unvowelled suffixes, which read the same for both genders («لك، حسابك»). Address a group with the plural («حيّاكم»). Or personalize when you know the reader's gender. Avoid «سجّل/ي».

**Buttons are verbal nouns; calls-to-action may be imperatives.** System buttons and menus: «حفظ، إلغاء، مشاركة». Marketing: «اطلب الآن، جرّب مجانًا». Pick a convention per product and keep it.

**Format:**
- Arabic punctuation: ، ؛ ؟, with «» for quotes.
- **One digit system per product.** Western 0–9 is the default for digital work in Saudi Arabia; Eastern ٠–٩ only if the brand requires it. Never mix the two, and never mix in Persian digits.
- Dates: Saudi month names (يناير…). Note when the Hijri date matters.
- Currency: «ريال / ر.س / SAR». There is a new riyal sign (U+20C1); check that the font supports it.
- In right-to-left text, wrap Latin runs and numbers in `<bdi>` or Unicode isolates.
- **Never letter-space Arabic**, and never fake italics or uppercase.

## Watch the double meanings

Unvowelled Arabic is ambiguous, and short headlines have no context to rescue them.
- **Words with several readings:**
  - «قبلة»: prayer direction or a kiss
  - «دين»: religion or debt
  - «حمل»: carrying or pregnancy
  - «شعر»: hair or poetry

  Add **one** vowel mark («القِبلة») or rewrite.
- **Words whose meaning flips with age or register:** «رهيب، خطير، فظيع» mean *awesome* to young Saudis and *terrifying, dangerous, horrible* in MSA.
- **Words that change across dialects:**
  - «العافية» is *fire* in Morocco
  - «ماشي» means *not* there
  - «عيش» is bread in Egypt and rice in the Gulf
  - «صاحبتي» implies a girlfriend in Egypt and the Levant

**Run every brand name, slogan and pun past Gulf, Egyptian, Levantine and Maghrebi readers.** Full lists: `references/double-meanings.md`.

## Make it sound native, not just correct

- **Concise:** «خير الكلام ما قلّ ودلّ». Cut «عملية / إمكانية / القيام بـ + masdar».
- **Verb-first for action and news; subject-first for punchy headlines** («حسابك جاهز»).
- **Rhythm sells.** One rhymed or parallel pair per headline works well («اطلب، تابع، استلم»). More than that sounds preachy.
- **Proverbs and religious phrases:** use them correctly, lightly and respectfully. Never quote the Quran in ads, and never make a religious phrase the punchline.
- **Coin with the root system, not against it.** A new word on a known pattern (مِفعال, فعّالة, فاعل) reads naturally.

See `references/style-and-rhetoric.md` and `references/history-and-roots.md`.

## Sound human, not machine-written

Arabic readers now recognize AI text on sight. It is correct, balanced and empty. The tells:
- **Stock openers and connectors:**
  - «في عالم اليوم»، «لا شك أن»، «يُعدّ … من أهم»، «تجدر الإشارة إلى»
  - «علاوة على ذلك»، «بالإضافة إلى ذلك»، «مما يجعل»، «في الختام»
- **Calqued contrasts:** «ليس فقط… بل أيضًا»، «ليس مجرد… بل».
- **Inflated nouns:** «رحلة»، «عالم»، «نقلة نوعية»، «تجربة استثنائية»، «حلول مبتكرة».
- **Shape:**
  - bullet lists where a person would tell a story
  - triplets everywhere («سهل، سريع، آمن»)
  - every sentence the same length
  - ending with a summary of what was just said
- **No detail, no person:** nothing only this writer could know.

To make it human:
- **Start from a real moment** («كنت أراجع…», «أول ما فتحت…») or a concrete example, not a thesis.
- **Use one specific detail:** a number, a word, a mistake you actually saw.
- **Vary the rhythm.** Let a short sentence stand alone. A long one, then a short one.
- **In casual registers, use spoken connectors** naturally: «بصراحة»، «يعني»، «ترى»، «الزبدة». Allow light humour where the reader would smile.
- **Prose over bullets** in posts and messages. Keep lists for real lists.
- **End with a question, an ask or a feeling,** not «في الختام».
- **Read it aloud in the reader's accent.** If it sounds like a press release and isn't one, rewrite it.

## Load a reference when the task needs it

| Task | Read |
|---|---|
| App, website or product copy | `references/ui-and-product-writing.md`, `references/translation-pitfalls.md` |
| Translating or localizing anything | `references/translation-pitfalls.md`, `references/double-meanings.md` |
| Ads, slogans, social posts, scripts, naming | `references/style-and-rhetoric.md`, `references/dialects-and-new-generation.md`, `references/double-meanings.md` |
| Youth or Gen Z voice, slang, Franco/Arabizi | `references/dialects-and-new-generation.md` (verify slang with a young native speaker; it ages fast) |
| Coining terms, naming, explaining Arabic | `references/history-and-roots.md` |
| Citing evidence | `references/sources.md` |

## Final check before handing over Arabic

1. Read it aloud. Would a native speaker of the target country say or accept it?
2. Search for «قم بـ، الخاص بك، يتم، بنجاح، من قبل، دعنا، عبر» and the clichés, and fix every hit.
3. Gender and number: are non-human plurals feminine singular, and are the 1/2/3–10/11+ forms right?
4. Is the reader addressed the same way throughout?
5. Are hamza, ة/ه, ى/ي and ض/ظ right?
6. Is there one register, one dialect and one digit system, with Arabic punctuation?
7. Does it sound like a person wrote it, with no stock openers, no inflated nouns, no list where a story belongs, and varied rhythm?
8. Could any word, without vowel marks or in another dialect, be read differently, embarrassingly or offensively?
9. Is every religious phrase used respectfully?
10. Is anything uncertain flagged for a native reviewer?

## When you're corrected

A native speaker's correction beats this file. Apply it, and suggest adding it to the project's glossary so it sticks.

---

*arabic-native* by **Hatem Abusitta** (حاتم أبو ستة). Licensed under CC BY 4.0. You are free to use, share and adapt it, with credit to the author.
