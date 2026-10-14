# UI and product writing in Arabic

> Part of the **arabic-native** skill by **Hatem Abusitta** (حاتم أبو ستة). Licensed CC BY 4.0. Keep this credit when you share or adapt it.
>
> Confidence tags: **[verified]** checked against a source in `sources.md`; **[common knowledge]** standard Arabic linguistics; **[observed / verify]** usage that shifts over time, so confirm with a native speaker or the live product.

## 8. UI and product writing conventions in Arabic

### 8.1 Buttons: verbal noun (مصدر) vs imperative (أمر)

The convention across major Arabic UIs [common knowledge; Microsoft verified; app specifics observed / verify]:

| Element | Preferred form | Examples |
|---|---|---|
| **System buttons, menu items, tabs** | **Verbal noun (مصدر)** or noun | حفظ، إلغاء، تعديل، حذف، مشاركة، إرسال، تسجيل الدخول، إنشاء حساب، الإعدادات، التالي، رجوع |
| **"Done"** | **تم** | iOS Arabic uses «تم» [observed] |
| **"OK"** | حسنًا / موافق | Android often «حسنًا» [observed] |
| **Marketing CTAs** | **Imperative** (masculine default, or plural) | اطلب الآن، حمّل التطبيق، جرّب مجانًا، اشترك، اكتشف العروض |
| **Instructions in body text** | Imperative or «يُرجى + مصدر» | «أدخل رمز التحقق المرسل إلى جوالك» / «يُرجى إدخال الرمز» |
| **Tooltips** | Verbal noun | «عرض الصفحات كما ستُطبع» (Microsoft) [verified] |

Why masdar for buttons: it is **gender-neutral**, short, and reads as a **label of the action** rather than a command. Imperatives are fine for persuasive CTAs, where a direct, warm command converts better.

### 8.2 Core UI glossary (Saudi-appropriate)

| English | Arabic (preferred) | Avoid / note |
|---|---|---|
| Sign in / Log in | تسجيل الدخول | الولوج (Maghreb/formal) |
| Sign out | تسجيل الخروج | |
| Sign up / Create account | إنشاء حساب / التسجيل | |
| Password | كلمة المرور | كلمة السر (also understood, less formal) |
| Verification code / OTP | رمز التحقق | كود (casual) |
| Mobile number | رقم الجوال | رقم الهاتف المحمول (stiff in Saudi) |
| National ID / Iqama | رقم الهوية / الإقامة | |
| Settings | الإعدادات | |
| Profile | الملف الشخصي / حسابي | |
| Home | الرئيسية | |
| Search | بحث / ابحث | |
| Filter / Sort | تصفية (or فلتر) / ترتيب | |
| Cart | السلة | |
| Checkout | إتمام الطلب / الدفع | |
| Wishlist / Favorites | المفضلة | |
| Notifications | الإشعارات / التنبيهات | |
| Share | مشاركة / شارك | |
| Download / Upload | تنزيل / رفع (or تحميل for download) | «تحميل» is ambiguous; many apps use it for download |
| Retry | إعادة المحاولة / حاول مجددًا | |
| Skip | تخطٍّ (imperative) / تخطّي (masdar) | The imperative is often misspelled «تخطي» |
| Next / Back | التالي / رجوع (or السابق) | |
| Continue | متابعة / استمرار | «متابعة» also means "follow"; context resolves it |
| Free trial | تجربة مجانية | |
| Subscribe / Upgrade | اشترك / ترقية | |
| Help / FAQ | المساعدة / الأسئلة الشائعة | |
| Terms / Privacy | الشروط والأحكام / سياسة الخصوصية | |
| Refund | استرداد المبلغ | إرجاع المال (casual) |

### 8.3 What major apps do [observed / verify against current versions]

- **Apple (iOS, macOS Arabic):** concise MSA, masdar labels (إلغاء، تعديل، مشاركة), «تم» for Done, «اضغط» for tap. Apple's WWDC22 "Design for Arabic" session covers RTL layout, Arabic typography and numerals. Apple's English style guide sends localizers to language-specific resources, and Apple publishes no public Arabic glossary. [verified on the WWDC/style guide points]
- **Google (Android, Material):** concise MSA; «حسنًا» for OK; Material's bidirectionality guidance on mirroring. [verified on Material]
- **Microsoft:** public Saudi Arabic style guide, the best open reference. Key points: imperative over «قم بـ», suffix possessives over «الخاص بك», gender-inclusive alternatives, Western digits, «تعذّر» for "couldn't", and a "feels originally written in Arabic" goal. [verified]
- **Absher, Tawakkalna, Nafath and other Saudi government apps:** formal MSA, masdar labels, «المستفيد» (beneficiary) as the neutral term for the user, Hijri and Gregorian dates. The Digital Government Authority launched **"كود المنصات"** (Platforms Code) in 2024, a national unified design system for government platforms. [verified on the Platforms Code]
- **STC, banks:** MSA in the app UI; white dialect in campaigns and social.
- **Careem, Jahez, HungerStation, Noon, Ninja:** MSA labels in UI, playful white Saudi dialect in push notifications, ads and social, with humor, food puns and seasonal hooks (Ramadan, payday, football). [observed]
- **UAE reference:** the UAE government's Arabic digital content guide (2021) recommends addressing the user in the singular, short sentences and paragraphs, simple words, consistent terms, lists, and content testing. [verified: u.ae]

### 8.4 Error messages

- **Microsoft's standard phrases** [verified]:
  - "Cannot / Could not..." → **«تعذّر...»** («تعذّر حذف الملف»)
  - "Failed to..." → «فشل...» (harsher; prefer تعذّر in user-facing text)
  - "Cannot find..." → «تعذّر العثور على...»
  - "... is not available" → «... غير متوفر»
- **Principles:**
  - Do not blame the user.
  - Say what happened, then what to do.
  - Avoid a bare «خطأ!».
  - Avoid stacking «عذرًا، حدث خطأ ما. يرجى المحاولة لاحقًا» on every screen.
- **Placeholders:** find out what fills «%s»/«{name}» so the sentence agrees in gender, number and definiteness. [verified: Microsoft]

| Situation | Stiff/translated | Natural MSA | Casual Saudi (consumer brand) |
|---|---|---|---|
| Network | حدث خطأ في الشبكة. يرجى المحاولة مرة أخرى لاحقًا. | تعذّر الاتصال. تحقّق من الإنترنت وحاول مجددًا. | النت فاصل؟ تأكد من الاتصال وجرّب مرة ثانية. |
| Wrong password | كلمة المرور التي أدخلتها غير صحيحة. | كلمة المرور غير صحيحة. حاول مجددًا أو أعِد تعيينها. | كلمة المرور مو صحيحة، جرّب مرة ثانية. |
| Payment failed | فشلت عملية الدفع. | لم يكتمل الدفع، ولم يُخصم أي مبلغ. جرّب بطاقة أخرى. | ما تم الدفع، ولا انخصم منك شي. جرّب بطاقة ثانية. |
| Not found (404) | الصفحة المطلوبة غير موجودة. | لم نجد هذه الصفحة. | الصفحة هذي مو موجودة 🤔 |

### 8.5 Empty states, success, confirmation

- **Empty states** need a reason plus a next step:
  - «لا توجد طلبات بعد. ابدأ أول طلب الآن.» (no orders yet; start your first order)
  - Casual: «سلّتك فاضية… وش ناقصك؟» (your cart is empty… what are you missing?)
- **Success:**
  - «تم» or «تم الحفظ» is enough. Drop «بنجاح».
  - Casual: «تم! طلبك في الطريق 🚗»
- **Confirmation dialogs:** ask the question as an action and label buttons with **verbs**, not «نعم/لا»:
  - Title: «حذف المحادثة؟»
  - Body: «لا يمكن التراجع عن الحذف.»
  - Buttons: «حذف» / «إلغاء»
- **Loading:** «جارٍ التحميل…», «لحظات…», or casual «ثواني بس…».
- **Forms:**
  - Label above the field.
  - Saudi formats in placeholders (05XXXXXXXX).
  - Validation that explains the fix: «أدخل رقم جوال يبدأ بـ 05».
- **Push notifications:**
  - Under about 60 characters for the title.
  - Dialect allowed for consumer brands.
  - Never fake urgency with religious wording.
  - Respect prayer times and Ramadan hours when scheduling. [observed best practice]

### 8.6 A quick self-check before shipping Arabic copy

1. Would a Saudi in their 20s say or accept this sentence? Read it aloud.
2. Any «قم بـ»، «الخاص بك»، «يتم»، «بنجاح»، «من قبل»، «دعنا»? Rewrite.
3. Do non-human plurals take feminine singular agreement? Are dual and number rules (3–10 / 11+) right?
4. Is the user addressed consistently (gender strategy chosen)?
5. Are hamzas right on UI verbs (أرسِل vs اختر), and are ة / ى / ض / ظ correct?
6. Arabic punctuation (، ؛ ؟), one digit system, and no bidi breakage with Latin terms?
7. Does any word have an unfortunate meaning in another dialect, or an unintended second reading without vowels?
8. One register only (MSA, or white dialect), with no dialect mixing?
9. No clichés (أطلق العنان، رحلة، تجربة لا مثيل لها)?
10. Any religious phrase or reference used respectfully, or removed?

---
