<div align="center">

<img src="assets/azizide-128.png" alt="AzizIDE Logo" width="130">

# 🐧 AzizIDE

**برمج بطريقتك. ببساطة ومتعة!**  
*A friendly code editor made for Linux.*

**v0.7.1 · Ubuntu / Linux · Python + PySide6 · Free**

</div>

---

## ✨ وش هو AzizIDE؟

**AzizIDE** محرر أكواد مجاني لسطح مكتب Linux، صنعته لأقدم تجربة برمجة بسيطة ومريحة بواجهة داكنة وهوية مرحة، بعيدًا عن القوائم المزدحمة.

تقدر تكتب الأكواد، تفتح مشاريعك، تشغّل ملفاتك المحلية، تشوف معاينة HTML مباشرة، وتتصفح ملفات السيرفر عن بُعد عبر SSH، وكل هذا من مكان واحد.

## 🌟 أهم المميزات

| الميزة | التفاصيل |
|---|---|
| 📝 محرر أكواد | تلوين الصياغة البرمجية، اقتراحات وإكمال كلمات أساسي، وتبويبات متعددة |
| 📁 إدارة المشاريع | فتح الملفات والمجلدات المحلية وتصفحها من مستكشف الملفات |
| 💾 حفظ مريح | حفظ يدوي، مع خيار الحفظ التلقائي للملفات المحلية |
| 🔎 بحث سريع | بحث داخل الملف والمشروع، وعرض النتائج مع الانتقال للملف والسطر |
| 🌐 SSH / SFTP | استعراض ملفات المشاريع على السيرفر والبحث فيها **للقراءة فقط** |
| ▶️ تشغيل الأكواد | تشغيل ملفات برمجية محلية وعرض المخرجات في لوحة **Run Results** |
| 💻 Terminal | طرفية محلية لتشغيل الأوامر من داخل البرنامج |
| 👁️ Live Preview | معاينة HTML وCSS وJavaScript محليًا مع عرض رسائل JavaScript |
| 🔠 تخصيص الخط | تعديل حجم خطوط المحرر والواجهة بحسب راحتك |
| 🐧 تصميم مميز | واجهة داكنة منظمة وشعار خاص ببرنامج AzizIDE |

> **ملاحظة:** دعم SSH في إصدار v0.7.1 مخصص لتصفح ملفات السيرفر والبحث فيها، وليس لتحريرها أو رفعها. ميزة تشغيل الأكواد والطرفية تعملان **محليًا** على جهازك.

## 🚀 تحميل وتثبيت AzizIDE على Ubuntu

اختر الطريقة اللي تناسبك من صفحة **[الإصدارات (Releases)](https://github.com/mraziz2005-hue/AzizIDE/releases)**.

### 🥇 الطريقة الأولى: تثبيت حزمة Snap المحلية

هذه أسهل طريقة إذا كان ملف Snap مرفقًا بالإصدار. حمّل:

`azizide_0.7.1_amd64.snap`

افتح Terminal ونفّذ:

```bash
cd ~/Downloads
sudo snap install --dangerous --classic ./azizide_0.7.1_amd64.snap
```

بعد التثبيت، افتح **AzizIDE** من قائمة التطبيقات، أو شغّله بالأمر:

```bash
snap run azizide
```

**معلومة:** هذه حزمة Snap للتثبيت المباشر من GitHub، وليست إصدارًا منشورًا حاليًا في Snap Store؛ لذلك يحتاج تثبيتها محليًا إلى الخيارين `--dangerous --classic`. حزمة Snap هذه مخصصة لمعمارية **amd64**.

### 🐧 الطريقة الثانية: التثبيت باستخدام ملفات Python

حمّل الملف التالي من **Releases** إذا كان مرفقًا:

`AzizIDE_0.7.1_Ubuntu_Installer.zip`

**1.** جهّز المتطلبات الأساسية على Ubuntu:

```bash
sudo apt update
sudo apt install python3 python3-venv python3-pip unzip
```

**2.** فك ضغط الملف وثبّت AzizIDE:

```bash
cd ~/Downloads
unzip -n AzizIDE_0.7.1_Ubuntu_Installer.zip
cd AzizIDE_0.7.1_Ubuntu_Installer
bash install.sh
```

**3.** افتح **AzizIDE** من قائمة التطبيقات. وتقدر تشغّله أيضًا من Terminal:

```bash
~/.local/bin/azizide
```

يقوم المثبّت بإنشاء بيئة Python خاصة بالبرنامج وتنزيل المكتبات اللازمة، ثم يضيف اختصار AzizIDE إلى قائمة التطبيقات. **لا تحتاج `sudo` عند تنفيذ `bash install.sh`**.

## 🧭 كيف تستخدم AzizIDE؟

### 📁 فتح مشروعك

اضغط **Folder** لاختيار مجلد مشروعك، ثم افتح أي ملف من مستكشف الملفات على الجانب. وتقدر تستخدم **New** لإنشاء ملف جديد و**Save** لحفظه.

### ▶️ تشغيل ملف برمجي

افتح ملفًا محليًا، مثل `hello.py`، واضغط **Run**. ستظهر نتيجة التشغيل داخل **Run Results**. يلزم وجود مفسّر اللغة أو أداة تشغيلها على جهازك.

```python
print("Hello from AzizIDE! 🐧")
```

### 👁️ معاينة صفحات الويب

افتح ملف HTML، ثم اضغط **Preview** لتظهر الصفحة بجانب المحرر. تقدر تعدّل HTML وCSS وJavaScript وتراجع النتيجة مباشرة.

### 🌐 تصفح مشاريع السيرفر عبر SSH

اضغط **SSH**، وأدخل عنوان السيرفر، واسم المستخدم، والمنفذ، ومسار المشروع، وطريقة الاتصال المناسبة. بعدها تقدر تفتح ملفات السيرفر وتبحث داخلها **دون تغيير الملفات البعيدة**.

### 🔎 البحث في المشروع

اضغط **Search Project** للبحث في مشروع محلي أو في اتصال SSH الحالي، ثم اختر إحدى النتائج للانتقال إلى السطر المطابق.

### 🔠 تكبير وتصغير الخط

اضغط **Aa Fonts** واضبط حجم الخط بما يناسبك.

## 💻 متطلبات التشغيل

- نظام Linux؛ التطوير والاختبار العملي الحالي على **Ubuntu**.
- تثبيت Snap يحتاج دعم `snapd` إذا اخترت حزمة `.snap`.
- طريقة Python تحتاج **Python 3** و`venv` واتصال إنترنت لتنزيل المكتبات أول مرة.
- المكتبات الأساسية في الإصدار: **PySide6** و**Paramiko**.
- تشغيل لغات البرمجة الأخرى يعتمد على أدوات التشغيل المثبتة على الجهاز.

## 🔄 تحديث AzizIDE

عند صدور إصدار جديد، بتلقاه في صفحة **[Releases](https://github.com/mraziz2005-hue/AzizIDE/releases)** في نفس المستودع.

- **إذا ثبّتّ Snap محليًا:** حمّل حزمة `.snap` الجديدة وثبّتها بالطريقة نفسها.
- **إذا ثبّتّ من Python:** حمّل ملف المثبّت الجديد، أغلق AzizIDE، ثم شغّل `bash install.sh` من المجلد الجديد.
- **التحديث التلقائي من GitHub غير متوفر حاليًا**؛ التحديث يدوي إلى أن نضيف آلية مناسبة.

> مثبّت Python يحتفظ بنسخة احتياطية من ملف البرنامج المثبّت السابق قبل تحديثه.

## 🔒 الخصوصية

في **AzizIDE**، تبقى ملفات مشاريعك المحلية على جهازك. الاتصال عبر SSH مخصص لتصفح ملفات السيرفر والبحث فيها للقراءة فقط، ولا يحفظ البرنامج كلمة مرور SSH ضمن إعدادات الاتصال. ولحماية مشروعاتك، احتفظ بمفاتيح الوصول وملفات الإعدادات الخاصة خارج المستودعات العامة.

## 🛠️ حل المشكلات الشائعة

| المشكلة | الحل |
|---|---|
| التطبيق لا يظهر في قائمة البرامج | جرّب `snap run azizide` أو `~/.local/bin/azizide` حسب طريقة التثبيت |
| مشكلة عند إنشاء بيئة Python | تأكد من تثبيت `python3-venv` |
| خطأ أثناء تنزيل المكتبات | تأكد من الإنترنت، ثم أعد `bash install.sh` |
| تشغيل الكود لا يعمل | تأكد من وجود مفسّر اللغة المطلوب، وراجع **Run Results** |
| SSH لا يتصل | راجع عنوان السيرفر والمنفذ وبيانات الدخول وإعدادات SSH |
| Live Preview لا تظهر | افتح ملف HTML محليًا وتأكد أن مكتبات التطبيق ثبتت بنجاح |

## 📁 ملفات المشروع

```text
AzizIDE/
├── main.py                # المحرر والواجهة ووظائف البرنامج
├── assets/                # شعارات وأيقونات AzizIDE
├── requirements.txt       # مكتبات Python المطلوبة
├── install.sh             # تثبيت البرنامج على Ubuntu
├── RELEASE_CHECKLIST.md   # قائمة مراجعة الإصدار
└── snap/                  # ملاحظات تجهيز Snap
```

## 📌 حالة المشروع

**AzizIDE v0.7.1** إصدار تجريبي مجاني قيد التطوير، وتُضاف التحسينات تدريجيًا. لتقديم اقتراح أو الإبلاغ عن مشكلة، استخدم تبويب **[Issues](https://github.com/mraziz2005-hue/AzizIDE/issues)**.

البرنامج مجاني، لكن لم يُحدَّد بعد ترخيص عام لإعادة استخدام الكود وتوزيعه؛ نشر الكود على GitHub لا يمنح تلقائيًا ترخيصًا مفتوح المصدر.

---

## 🌍 English quick start

**AzizIDE** is a free, penguin-themed code editor for Ubuntu/Linux, built with Python and PySide6. It offers syntax highlighting, multiple tabs, local project search, basic completion, local code execution, a built-in local terminal, HTML live preview, and read-only SSH/SFTP project browsing.

**Install from the Ubuntu installer ZIP:**

```bash
sudo apt update
sudo apt install python3 python3-venv python3-pip unzip
cd ~/Downloads
unzip -n AzizIDE_0.7.1_Ubuntu_Installer.zip
cd AzizIDE_0.7.1_Ubuntu_Installer
bash install.sh
```

Launch it from the Applications menu or run `~/.local/bin/azizide`.

Alternatively, download the `amd64` Snap asset from **Releases**, install it locally with `sudo snap install --dangerous --classic ./azizide_0.7.1_amd64.snap`, and launch with `snap run azizide`.

**Status:** early preview · **Platform:** Ubuntu/Linux · **Updates:** manual via GitHub Releases.

---

<div align="center">

**Made with 🐧 for Linux users.**

*Code comfortably. Enjoy the process.*

</div>
