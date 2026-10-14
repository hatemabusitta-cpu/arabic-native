# arabic-native

**عربية تُكتب ولا تُترجَم · Arabic, written native**

*بقلم حاتم أبو ستة · By Hatem Abusitta*

---

## بالعربي

أغلب العربية التي تكتبها الآلات اليوم صحيحة نحويًا لكنها غريبة على الأذن: ترتيب جمل إنجليزي، و«قم بـ»، و«الخاص بك»، و«تم بنجاح» في كل سطر. القارئ العربي يكشفها من أول جملة.

هذه المهارة تعلّم Claude أن يكتب العربية من المعنى، بالمستوى الذي يعيشه القارئ: فصحى سهلة للتطبيقات، وفصحى رسمية للعقود، ولهجة سعودية بيضاء للإعلانات ووسائل التواصل.

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

This Claude skill writes Arabic **from the meaning**, in the register the reader actually lives in. Simple MSA for apps, formal MSA for contracts, and white Saudi dialect for ads and social. It covers register choice, a calque blacklist, number and gender agreement, double meanings across dialects, rhetoric, new-generation Arabic, UI writing, and the history behind the language. Saudi Arabia and the Gulf are the default audience.

## Install

Copy the `arabic-native` folder into your Claude skills folder:

```bash
cp -R arabic-native ~/.claude/skills/
```

Claude then uses it whenever you write, translate or review Arabic.

## Layout

- `SKILL.md`: the core rules and the final check
- `references/`: deep material, loaded only when a task needs it (history and roots, dialects and youth language, double meanings, style, translation pitfalls, UI writing, sources)

Claims are tagged **[verified]**, **[common knowledge]** or **[observed / verify]**. Slang and app-specific usage change fast, so confirm those with a native speaker.

## Credit and license

Created by **Hatem Abusitta** (حاتم أبو ستة). Licensed under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/): use it, share it, adapt it, and keep the credit.

Corrections from native speakers are welcome. Open an issue with the word, the context and what you would say instead.
