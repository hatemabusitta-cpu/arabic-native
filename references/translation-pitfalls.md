# Translation and localization pitfalls

> Part of the **arabic-native** skill by **Hatem Abusitta** (حاتم أبو ستة). Licensed CC BY 4.0. Keep this credit when you share or adapt it.
>
> Confidence tags: **[verified]** checked against a source in `sources.md`; **[common knowledge]** standard Arabic linguistics; **[observed / verify]** usage that shifts over time, so confirm with a native speaker or the live product.

## 7. Translation and localization pitfalls

### 7.1 The calque blacklist

| Calque | Source | Fix |
|---|---|---|
| **قم بـ + masdar** («قم بفتح التطبيق») | "Do X" | Plain imperative: «افتح التطبيق». Microsoft's Saudi style guide makes this exact recommendation. [verified] |
| **الخاص بك / الخاصة بك** («كلمة المرور الخاصة بك») | "your" | Possessive suffix: «كلمة مرورك». Microsoft: use the suffix the first time only, or drop it when the owner is obvious. [verified] |
| **الخاص بي** («الملفات الخاصة بي») | "my" | «ملفاتي». [verified: Microsoft] |
| **يتم + masdar** («يتم إرسال الرمز») | English passive | Active voice with a subject: «نرسل لك رمزًا» / «سنرسل...»; or a true passive marked with a damma: «يُرسَل الرمز خلال دقيقة». |
| **تم ... بنجاح** («تم حفظ التغييرات بنجاح») | "successfully" | «حُفظت التغييرات» or simply «تم الحفظ». «بنجاح» is usually redundant. In Saudi UI «تم» on its own is natural. |
| **من قِبَل** («تم إنشاء الحساب من قبل المسؤول») | "by" (passive agent) | Active: «أنشأ المسؤول الحساب». |
| **دعنا / دعونا** («دعنا نبدأ») | "Let's" | «لنبدأ» / «هيا نبدأ» / «يلا نبدأ» (casual). |
| **هل أنت متأكد من أنك تريد...؟** | "Are you sure you want to...?" | «حذف الصورة؟» or «تريد حذف الصورة فعلًا؟» |
| **والذي / والتي** after a comma | ", which" | «الذي» without و, or split the sentence. |
| **حيث** as a universal connector | "where / whereas / as" | Use «إذ»، «لأن»، «فـ» or a new sentence. |
| **سوف لن** | "will not" | «لن». |
| **كلما... كلما** | "the more... the more" | «كلما... ـ» (one كلما): «كلما طلبت أكثر، وفّرت أكثر». |
| **تواجد** for "presence" | | «وجود». Purists object that تواجد originally meant feigning ecstasy; «وجود» is always safe. |
| **إمكانية القيام بـ** | "the ability to do" | Verb: «تستطيع أن...» / «يمكنك...». |
| **أكثر من رائع** | "more than amazing" | Fine colloquially; overused. |
| **في عالم اليوم المتسارع** | "In today's fast-paced world" | Delete. |
| **من خلال / عبر** in every sentence | "through / via" | «بـ»: «ادفع بالبطاقة». |
| **جاري التحميل** | "Loading" | Grammatically «جارٍ التحميل». Also acceptable: «يُحمَّل...» or «لحظات...». |

### 7.2 Passive overuse

- English UI loves passive voice; Arabic tolerates it far less. Prefer:
  1. **Active, with "we"**: «أرسلنا الرمز إلى جوالك» (We sent the code to your phone).
  2. **A true passive with a damma** (Microsoft requires the damma to avoid ambiguity): «أُرسِل الرمز». [verified]
  3. **A verbal noun as a label**: «إرسال الرمز...».
  4. **An impersonal construction with a preposition**: Microsoft's example renders "The problem was investigated" as «بُحث في المسألة». [verified]

### 7.3 Gender and number agreement

- **Every verb, adjective and pronoun agrees in gender.** English "you" is four forms in Arabic: أنتَ (m.), أنتِ (f.), أنتما (dual), أنتم/أنتنّ (pl.).
- **Non-human plurals take feminine singular agreement**: «الطلبات **جاهزة**» (the orders are ready, not جاهزون); «الملفات **حُذفت**»; «لا **توجد** طلبات» (no orders), not «لا يوجد طلبات». The latter is common in speech but is an error in MSA.
- **Dual:** English plural maps to either the Arabic plural or the dual. Microsoft's example: the two spin arrows are «سهمان», not «أسهم». [verified] UI examples: «رسالتان جديدتان» (2 new messages), «منذ يومين» (2 days ago).
- **Numbers and counted nouns** [common knowledge]:

| Number | Rule | Example |
|---|---|---|
| 0 | Rephrase | «لا توجد رسائل» (Microsoft: write 0 items as "there are no items") [verified] |
| 1 | Noun singular; number after noun as adjective | «رسالة واحدة» or just «رسالة» |
| 2 | Dual noun; number optional | «رسالتان» |
| 3–10 | **Plural** noun, genitive; number word takes the **opposite gender** of the singular noun | «ثلاثة كتب» (كتاب m. → ثلاثة), «ثلاث رسائل» (رسالة f. → ثلاث) |
| 11–99 | **Singular** noun, accusative | «أحد عشر كتابًا»، «خمسون ريالًا» |
| 100, 1000, … | **Singular** noun, genitive | «مئة ريال»، «ألف متابع» |

- **Software plural handling:** Arabic uses all six CLDR plural categories: **zero, one, two, few (3–10), many (11–99), other (100+ and others)**. Every count string («{n} items») needs six variants in ICU MessageFormat or platform plural resources. A cheap alternative is a label-colon pattern: «عدد العناصر: 5», or putting the digit before a noun form that works for all counts. [common knowledge; CLDR]

### 7.4 Gender-neutral addressing strategies

Arabic has no neutral "you". Strategies, from cleanest to clumsiest:

1. **Write without vowels in the pronoun suffix:** «لك»، «بك»، «حسابك» are gender-ambiguous in writing (لكَ / لكِ). «أهلًا بك» works for everyone.
2. **Use verbal nouns** for buttons, labels and tooltips: «تسجيل الدخول»، «حفظ»، «عرض الكل». Microsoft recommends verbal nouns in tooltips because Arabic has no neutral "it" (an icon is feminine, a button masculine). [verified]
3. **Use «يُرجى / يمكنك / يجب» + masdar** in instructions: «يُرجى إدخال رمز التحقق», «يمكنك تغيير الصورة لاحقًا». Microsoft recommends this pattern for instructions. [verified]
4. **First-person plural (we/let's):** «لنبدأ»، «خلّنا نكمل».
5. **Plural address (أنتم):** common in brand voice («حيّاكم»، «اطلبوا الآن»). It feels collective, respectful and inclusive.
6. **Collective nouns** for groups: Microsoft suggests «الحضور» instead of «المشاركون/المشاركات», «فريق العمل» instead of «الموظفون/الموظفات», «كبار السن» instead of «المسنّين». [verified]
7. **Personalize by gender** when known (ask at onboarding, or infer from a profile with consent), then use full feminine forms for women. This is the most native experience.
8. **Masculine generic** (سجّل، اطلب): widely accepted in Arabic marketing as the default, but increasingly criticized.
9. **Avoid slashes** («سجّل/ي», «عزيزي/عزيزتي») except in forms; they are ugly and hard to read aloud.

### 7.5 Tashkeel (vowel marks)

- **Do not fully vowel normal copy.** It slows reading and looks childish or religious.
- **Add a mark when it:**
  - prevents a wrong reading (القِبلة، الحُب، عُلِم)
  - marks the passive (أُرسِل، حُفظ) [Microsoft: required for passives]
  - shows shadda on a form-II verb that otherwise reads as form I (فعّل, حمّل, سجّل)
  - adds tanween on adverbs/accusatives: «شكرًا», «مجانًا», «أيضًا». The modern convention puts the tanween on the letter before the alif (شكرًا), not on the alif (شكراً); both are seen.
- **Fully vowel:** children's books, language-learning material, Quran/hadith quotes, poetry, and names the reader may not know.

### 7.6 Numbers and digits

- **Two digit sets:** Western Arabic (0123456789) and Eastern Arabic or "Hindi" (٠١٢٣٤٥٦٧٨٩, U+0660–0669). **Persian/Urdu digits** (۴۵۶, U+06F0–06F9) look similar but are different code points. Never mix them; it breaks search and parsing.
- **Regional preference** (sources disagree; this is a moving target):
  - Microsoft's Saudi Arabic style guide: always use Western digits, which are becoming standard across the Arab world. [verified]
  - Wikipedia: both systems coexist in the Arab east, but Western digits are increasingly favored, **particularly in Saudi Arabia**; the UAE uses both. [verified]
  - Google's Saudi localization guide (undated): Eastern digits are widely used in Saudi Arabia. [verified as stated]
  - Practical observation: Saudi apps and websites use Western digits overwhelmingly. Eastern digits survive in printed newspapers, official letters, mosque timetables, wedding invitations and some government documents. Maghreb countries use Western digits. [observed]
  - **Rule for the skill:** Western digits by default for digital and tech; Eastern digits only if the brand style requires it; **never mix in one product**.
- **Direction:** numbers are written and read left-to-right even inside RTL text, and are **not mirrored** in RTL layouts (including clocks and phone numbers). [verified: Material Design]
- **Separators:** with Eastern digits use the Arabic decimal separator «٫» (U+066B) and thousands separator «٬» (U+066C). Microsoft notes that with Arabic context, version numbers use Eastern digits with a comma-like separator, otherwise keep the source format. [verified] With Western digits, the period and comma are the norm in Saudi UI.
- **Percent:** «٪» (U+066A) with Eastern digits, «%» with Western.
- **Phone numbers:** Saudi mobile numbers are 05XXXXXXXX locally and +966 5X XXX XXXX internationally. Wrap them in an LTR isolate (7.8).
- **Currency:**
  - Text forms: «ريال», «ر.س» (abbreviation), «SAR».
  - **The new Saudi Riyal symbol:** SAMA introduced an official riyal symbol in February 2025, and Unicode encoded it (SAUDI RIYAL SIGN, U+20C1) in Unicode 17.0 (2025). Font support was still spreading as of late 2025. Use an SVG or icon fallback and verify rendering. [common knowledge; verify]
  - Placement: in Arabic text, the amount usually comes first: «50 ريالًا» or «٥٠ ر.س». Follow the brand's design system for symbol placement.
- **Dates and calendars:**
  - Saudi Arabia uses both the **Hijri (Umm al-Qura)** and Gregorian calendars. Government moved to the Gregorian calendar for many financial matters in 2016, but Hijri dates remain common in religious, official and cultural contexts.
  - Gregorian month names differ by region: Saudi/Gulf/Egypt use «يناير، فبراير، مارس...»; Levant and Iraq use Syriac names «كانون الثاني، شباط، آذار...»; Algeria/Tunisia use French-derived «جانفي، فيفري...». Use «يناير» for Saudi.
  - The week starts on **Sunday**; the weekend is **Friday–Saturday**.
  - Date format: day/month/year («14 أكتوبر 2026» or 14/10/2026).

### 7.7 Punctuation

| Mark | Arabic | Notes |
|---|---|---|
| Comma | **،** (U+060C) | No space before, one after. [verified: Microsoft] Never use the Latin comma in Arabic text. |
| Semicolon | **؛** (U+061B) | Often used for cause/explanation. |
| Question mark | **؟** (U+061F) | Mirrored form. |
| Quotation marks | **« »** (guillemets) or straight " " | Many Arab publishers use «»; Microsoft uses straight quotes for UI element names. [verified] Pick one per brand. |
| Period, colon, exclamation | . : ! | Same characters; no space before. [verified: Microsoft] |
| Dash | Avoid the kashida-as-dash in UI | Microsoft suggests the kashida character visually aligns better as a dash, but it causes search and accessibility problems in web/UI text. Use an en dash or rephrase. [verified + caution] |
| Ellipsis | ... | Same as source. [verified: Microsoft] |
| Parentheses | ( ) | Mirrored automatically by the bidi algorithm; type them logically. |

### 7.8 RTL and bidi issues when mixing Latin text

- **The problem:** an Arabic sentence containing a Latin term, number, or URL can display with punctuation or words in the wrong place. A trailing period after an English word may jump to the wrong side; «iPhone 16 Pro» may display as «Pro 16 iPhone» in some contexts.
- **Fixes** [common knowledge; Material and Wikimedia guidance]:
  - Set `dir="rtl"` and `lang="ar"` on Arabic containers; use `dir="auto"` for user-generated text.
  - Wrap embedded LTR runs in `<bdi>` or Unicode isolates (LRI U+2066 ... PDI U+2069; FSI U+2068).
  - Use RLM (U+200F) after a Latin word at the end of an Arabic sentence so the punctuation stays on the correct side.
  - **Mirror** layout, navigation and direction-bearing icons (back arrows, progress); do **not** mirror clocks, media-play icons, charts, logos, or numbers. Android Compose has auto-mirroring icons. [verified: Material]
- **Typography:**
  - **Never apply letter-spacing (tracking) to Arabic.** It breaks letter connections.
  - Arabic has **no uppercase**. Emphasis comes from weight, size or color. Do not fake italics.
  - Arabic needs **more line height** than Latin (diacritics above and below).
  - Do not justify with stretched kashida in UI.
  - Use a font with real Arabic support (IBM Plex Sans Arabic, Noto Sans/Kufi Arabic, Tajawal, Cairo, Almarai, or SF Arabic / Segoe UI on system).
- **Hashtags:** Arabic hashtags join words with underscores (#موسم_الرياض). Mixed-script hashtags can break.
- **Length:** Arabic strings are often similar in character count to English but behave differently in width, and dialect copy may be longer. Leave room for at least 25–30% expansion and test real strings.

### 7.9 Hamza, taa marbuta, alif maqsura and other spelling errors

**إنّ vs أنّ**
- Use **إنّ** at the start of a sentence, after «قال» and its derivatives, and after oaths: «قال إنّ الخدمة متوقفة».
- Use **أنّ** after most other verbs and prepositions (as a "that" clause): «نودّ أن نؤكد أنّ طلبك وصل»، «علمنا أنّ...».
- **إن** (if / indeed) vs **أن** (to, that + verb): «أريد أن أشترك» (I want to subscribe).
- **«إن شاء الله», not «إنشاء الله»**: «إنشاء» means "creation". This is the most notorious error.

**Hamzat al-qat' vs al-wasl** (high impact on UI verbs)

| With hamza (قطع) | Without hamza (وصل) |
|---|---|
| Form IV verbs and imperatives: أرسِل، أضِف، أدخِل، أكمِل، أنشِئ، أغلِق، ألغِ | Form VII/VIII/X imperatives and masdars: اختر، استخدم، انتقل، انضم، استمتع، اشترك، اختيار، استخدام، انتظار |
| Form IV masdars: إرسال، إضافة، إدخال، إكمال، إنشاء، إغلاق، إلغاء | Form I imperatives: اكتب، ادخل (enter, form I)، افتح |
| Nouns: أسعار، أخبار، أكثر | Nouns: اسم، ابن، امرأة، اثنان |
| Prefix: إعدادات، إشعارات | Articles: ال (الإعدادات) |

Note: «ادخل» (enter, form I: go in) and «أدخِل» (form IV: input/insert) differ in meaning. "Enter your password" is «أدخِل كلمة المرور», and "Come in" is «ادخل».

**Middle hamza seats:** «مسؤول» (Saudi and Gulf standard, seat on waw) vs «مسئول» (Egyptian convention). Similarly «شؤون/شئون», «يقرؤون/يقرأون». Use the Saudi form for Saudi audiences.

**Taa marbuta (ة) vs haa (ه):** casual typing drops the dots: «مدرسه» for «مدرسة». This is an error, and sometimes it changes meaning: «مكتبه» (his office) vs «مكتبة» (library); «سنه» (his tooth) vs «سنة» (year).

**Alif maqsura (ى) vs yaa (ي):**
- «على» (on) vs «علي» (Ali); «إلى» (to) vs «إلي» (to me).
- Egyptian-style typing writes every final ي as ى («فى»، «الذى»). This is common in Egypt but looks wrong to Gulf readers.
- Correct: «مستشفى»، «مستوى»، «حتى»; «في»، «الذي»، «التي».

**ض vs ظ** (merged in Gulf pronunciation, so frequently confused in Saudi writing):

| ظ | ض |
|---|---|
| ظل (shade, remained) | ضل (went astray) |
| نظارة (glasses) | نضارة (freshness, radiance) |
| حظ (luck) | حض (urging) |
| ظن (thought) | ضن (was stingy) |
| عظيم (great) | — |
| محظوظ (lucky; «محضوض» is a misspelling) | — |

A skincare ad promising «نضارة» (radiance) that is written «نظارة» promises eyeglasses.

**ث/س and ذ/ز** (merged in Egyptian and Levantine urban speech): «ثمين» (precious) vs «سمين» (fat); «ذكي» (smart), never «زكي» except as a name; «هذا» not «هزا»; «ذلك» not «ذالك»; «لكن» not «لاكن»; «هذا» not «هاذا».

**Tanween alif:** «شكرًا»، «أهلًا»، «جدًا»، «مجانًا»; not «شكرا ً» with stray spacing. Words ending in ة take no extra alif («رحمةً»). Words ending in hamza after alif take no extra alif («مساءً»، «سواءً»).

**Other frequent slips:**
- «مساءً» not «مسائً»
- «جزاك الله خيرًا»
- «اللهم» not «الله م»
- «الآن» (alif madda), not «الان»
- «يا» + name is written separately: «يا أحمد»
- «ابن» loses its alif between two names: «محمد بن سلمان»

---
