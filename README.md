# arabic-native

**عربية تُكتب ولا تُترجَم · Arabic, written native**

*بقلم حاتم أبو ستة · By Hatem Abusitta*

**Make ChatGPT, Claude, Gemini, or any AI write Arabic that sounds native, not translated.**
**اجعل ChatGPT وClaude وGemini وأي ذكاء اصطناعي يكتب عربية أصيلة، لا ترجمة حرفية.**

| English | Literal AI Arabic ✗ | arabic-native ✓ |
|---|---|---|
| Click the button below | قم بالضغط على الزر أدناه | اضغط الزر |
| Your password was successfully updated | تم تحديث كلمة المرور الخاصة بك بنجاح | تم تحديث كلمة مرورك |
| Are you sure you want to delete this photo? | هل أنت متأكد أنك تريد حذف هذه الصورة؟ | حذف الصورة؟ |
| Failed to connect | فشل الاتصال | تعذّر الاتصال |
| 12 new messages | 12 رسائل جديدة | 12 رسالة جديدة |
| Unlock your potential | أطلق العنان لإمكاناتك | قدراتك تكفي، ابدأ |

Works for: Arabic localization (تعريب) and translation (ترجمة), app and website copy, UX writing, marketing and ads, social media content (صناعة المحتوى), WhatsApp messages, and Saudi and Gulf audiences.

---

## بالعربي

أغلب العربية التي تكتبها الآلات اليوم صحيحة نحويًا لكنها غريبة على الأذن: ترتيب جمل إنجليزي، و«قم بـ»، و«الخاص بك»، و«تم بنجاح» في كل سطر. القارئ العربي يكشفها من أول جملة.

هذه المهارة تعلّم الذكاء الاصطناعي أن يكتب العربية من المعنى، بالمستوى الذي يعيشه القارئ: فصحى سهلة للتطبيقات، وفصحى رسمية للعقود، ولهجة سعودية بيضاء للإعلانات ووسائل التواصل.

**ما الذي تغطيه:**
- اختيار المستوى المناسب لكل منصة، وعدم خلط اللهجات
- قائمة بالتراكيب المترجمة حرفيًا وبدائلها الطبيعية
- قواعد العدد والجنس التي تخطئ فيها الآلات
- الكلمات ذات المعنيين، والأضداد، والكلمات التي يتغيّر معناها من لهجة إلى أخرى
- البلاغة التي تجعل النص عربيًا أصيلًا: الإيجاز، والإيقاع، والسجع، والأمثال
- لغة الجيل الجديد: العربيزي، والمزج بالإنجليزية، والعامية الشبابية
- كتابة الواجهات: الأزرار، ورسائل الخطأ، والصفحات الفارغة، والإشعارات
- لمحة عن تاريخ العربية ونظام الجذر والوزن

## In English

Most machine-made Arabic is grammatical but foreign: English word order, «قم بـ», «الخاص بك», «تم بنجاح» on every line. Native readers spot it instantly.

This skill teaches AI to write Arabic **from the meaning**, in the register the reader actually lives in. Simple MSA for apps, formal MSA for contracts, and white Saudi dialect for ads and social. It covers register choice, a calque blacklist, number and gender agreement, double meanings across dialects, rhetoric, new-generation Arabic, UI writing, and the history behind the language. Saudi Arabia and the Gulf are the default audience.

## استخدمها مع أي ذكاء اصطناعي · Use it with any AI

| الأداة · Tool | الطريقة · How |
|---|---|
| **Claude Code** | `cp -R arabic-native ~/.claude/skills/` |
| **Claude.ai** (web, desktop) | Settings › Capabilities › Skills, then upload `arabic-native.zip` from [Releases](../../releases) |
| **OpenAI Codex, Gemini CLI, Cursor, GitHub Copilot** and other tools that read the open `SKILL.md` standard | Copy the folder into the tool's skills folder, e.g. `~/.agents/skills/arabic-native` (Codex, Cursor) or `~/.gemini/skills/arabic-native` (Gemini CLI). Check your tool's docs for the exact path. |
| **ChatGPT** (Custom GPT) | Paste [`prompt/arabic-native-prompt.md`](prompt/arabic-native-prompt.md) into *Instructions*, then upload the files in `references/` as *Knowledge* |
| **ChatGPT** (any chat) | Paste the prompt into *Custom instructions* (paid plans allow 5,000 characters), or send it as the first message of a chat |
| **Gemini** (Gem) | Create a Gem, paste the prompt into *Instructions*, and add the `references/` files (7 files; Gems take up to 10) |
| **Any other AI** | Paste the prompt at the start of the conversation or into its system prompt |

The prompt is a compact version of the skill (about 3,200 characters). The full depth lives in `SKILL.md` and `references/`.

**بالعربي:** المهارة تعمل مع أي ذكاء اصطناعي. أدوات البرمجة الحديثة (Codex وGemini CLI وCursor وCopilot) تقرأ مجلد المهارة كما هو. وفي ChatGPT وGemini الصق ملف `prompt/arabic-native-prompt.md` في خانة التعليمات، وارفع ملفات `references` كمعرفة إضافية.

## Layout

- `SKILL.md`: the core rules and the final check
- `prompt/arabic-native-prompt.md`: the compact, paste-anywhere version for ChatGPT, Gemini and other assistants
- `references/`: deep material, loaded only when a task needs it (history and roots, dialects and youth language, double meanings, style, translation pitfalls, UI writing, sources)

Claims are tagged **[verified]**, **[common knowledge]** or **[observed / verify]**. Slang and app-specific usage change fast, so confirm those with a native speaker.

## Credit and license

Created by **Hatem Abusitta** (حاتم أبو ستة). Licensed under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/): use it, share it, adapt it, and keep the credit.

Corrections from native speakers are welcome. Open an issue with the word, the context and what you would say instead.
