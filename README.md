# 🎬 reel-editor — Claude يمنتجلك الفيديو ويسلّمك مشروع كاب كت جاهز

**عربي** · [English below](#english)

تعطي Claude فيديو (أو مشروعك بكاب كت)، وهو يسويلك مونتاج كامل:

- **موشن جرافيك** يطلع ويّا كل كلمة تنقال: بطاقات، أيقونات، عدّادات أرقام، قوائم، مقارنات، وعناصر **ورا الشخص** (علم، خط بياني، فكرة تطلع من راسه).
- **ترجمة** بالعربي (أو أي لغة)، وبإملاءك إنت.
- **انتقالات** على القطعات (Light Leaks مولّدة)، ومعالجة **البي رول** (أبيض وأسود + فلاش وثائقي).
- **ساوند ديزاين ومستوى صوت** للمنصات: مؤثرات مولّدة بلا حقوق، موسيقى من مكتبتك، والصوت على −14 LUFS.
- **مناطق أزرار المنصات** محسوبة (إنستا، تيك توك، يوتيوب شورتس)، فما يطلع شي تحت اللايك أو اسم الحساب.
- **بطاقة نهاية** باسمك وسؤالك الختامي.

وبالأخير يسلّمك:
1. **فيديو MP4 جاهز للنشر**
2. **مشروع كاب كت قابل للتعديل**: كل أنميشن كليب لحاله، والترجمة نصوص أصلية، وكل صوت كليب منفصل
3. **طبقات بريمير** (ProRes + XML) إذا تريد

## شنو تحتاج
- **Claude Code**: تطبيق Claude للحاسبة (تبويب Code) أو Claude Code بالترمنال، ويّا اشتراك.
- **Windows أو Mac**، وعليه **CapCut للحاسبة** (للمشروع القابل للتعديل) أو Premiere.
- **Python 3.9+ و FFmpeg**. إذا ما عندك، Claude ينصبهم بنفسه بعد ما تسمحله.

## التنصيب، اختار طريقة وحدة

**الأسهل:** افتح Claude Code وانسخ هالجملة:
```
نصبلي سكل المونتاج من https://github.com/husseinxh3-afk/reel-editor وجهز كل اللي تحتاجه
```

**بأمرين** (بداخل Claude Code):
```
/plugin marketplace add husseinxh3-afk/reel-editor
/plugin install reel-editor@reel-editor
```

**يدوي:** نزّل المشروع (Code ← Download ZIP)، وانسخ فولدر `plugins/reel-editor` إلى:
- Windows: `C:\Users\<اسمك>\.claude\skills\reel-editor`
- Mac: `~/.claude/skills/reel-editor`

## الاستخدام
اكتب لـ Claude بشكل طبيعي:
- `منتجلي هذا الفيديو C:\Users\...\video.mp4 وسويلي مشروع كاب كت`
- `مشروعي بكاب كت اسمه "الحلقة 3"، منتجه وخلي الترجمة بالعراقي`
- `سويله انميشنات وترجمة وطلعلي طبقات بريمير`

**أول مرة** Claude يسألك عن اسمك وجملتك التعريفية (لبطاقة النهاية)، والستايل اللي يعجبك (رسمي/إخباري، صانع محتوى، بسيط)، وألوان علامتك إذا عندك، ويحفظها لكل فيديو جاي.

**نصايح:**
- إذا عندك نص الفيديو، الصقه. الترجمة تطلع بإملاءك.
- لما يگلك "سدّ كاب كت"، سدّه بالكامل. كاب كت يعيد كتابة قائمة مشاريعه لما ينسد.
- Claude **ما يسمع** الصوت. يختار الموسيقى والمؤثرات بالتحليل، فاسمع النتيجة وگله إذا تريد تغيير.
- مشروعك الأصلي بكاب كت **ما ينلمس أبداً**. كلشي يطلع بمشروع جديد.
- **للتعديل بكاب كت:**
  - حتى تحرّك عنصر أو تكبّره: حدد قطعه ← كلك يمين ← **Create compound clip**.
  - حتى تغيّر مدته: مطّ قطعة الصورة اللي بالنص.
  - للتلوين: **Adjust ← LUT** ← `grade.cube`.

## ملاحظات
- المؤثرات الصوتية والـ Light Leaks **مولّدة بالكود**، فما بيها أي حقوق. الموسيقى من مكتبتك إنت.
- مشروع كاب كت مجرّب على **CapCut 9.5 (Windows)**.
- الترخيص: MIT. استخدمه، عدّله، وشاركه.

---

<a name="english"></a>
## English

**reel-editor** is a Claude Code plugin (skill) that edits vertical talking-head videos end to end — word-synced motion
graphics, captions (Arabic/RTL-ready), counters, icons, graphics behind the speaker, generated light leaks over jump
cuts, b-roll treatment, generated sound effects, music mixing at −14 LUFS, Instagram/TikTok/YouTube safe zones and an
end card — and hands back a **ready-to-post MP4**, an **editable CapCut project** (every animation its own clips,
native captions, separate audio) and optional **Premiere layers** (ProRes 4444 + FCP XML).

**Install** (inside Claude Code):
```
/plugin marketplace add husseinxh3-afk/reel-editor
/plugin install reel-editor@reel-editor
```
or copy `plugins/reel-editor` to `~/.claude/skills/reel-editor`, or just ask Claude: *"install the reel-editor
skill from https://github.com/husseinxh3-afk/reel-editor"*.

**Use**: "edit this video `path/to/video.mp4` and make me a CapCut project" · "my CapCut project 'Episode 3' — edit
it" · "export Premiere layers". First run asks for your name, tagline, style (news / creator / minimal) and brand
colours and saves them in `~/.reel-editor/config.json`.

**Requirements**: Claude Code, Windows or macOS, Python 3.9+, FFmpeg (Claude installs what's missing with your
permission), CapCut desktop (tested on 9.5 for Windows) and/or Premiere Pro.

Sound effects and light leaks are generated procedurally (no third-party assets). MIT licensed.
