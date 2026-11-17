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

## 🚀 تحميل وتثبيت AzizIDE على Linux

### التوافق واختيار الملف

نفس حزمة Snap يمكن استخدامها على توزيعات Linux متعددة تدعم **snapd وClassic**. تختلف أوامر تجهيز Snap حسب التوزيعة، ثم يكون أمر تثبيت التطبيق واحدًا. لا يعني ذلك ضمان التشغيل على كل توزيعة دون اختبار.

| النظام | الحالة |
|---|---|
| Ubuntu | بيئة التطوير والاختبار المذكورة سابقًا في المشروع |
| Fedora المكتبي التقليدي | تعليمات التجهيز أدناه؛ لم تتأكد تجربة AzizIDE عليه بعد |
| Debian / Linux Mint | تعليمات تجهيز Snap متاحة أدناه؛ اختبار التطبيق نفسه غير موثق هنا |
| توزيعات أخرى | تحتاج دعم Snap وClassic؛ راجع دليل توزيعتك |
| Fedora Silverblue / Kinoite | لا تُطبّق عليها خطوات Fedora التقليدي باعتبارها مضمونة |
| x86_64 / AMD64 | معمارية الحزمة الحالية، لمعالجات Intel وAMD ذات 64 بت |
| ARM / aarch64 أو 32 بت | الحزمة الحالية غير مناسبة |

**الملف المتاح فعليًا في إصدار v0.7.1:**

[تحميل azizide_0.7.1_amd64.snap](https://github.com/mraziz2005-hue/AzizIDE/releases/download/v0.7.1/azizide_0.7.1_amd64.snap)

يمكنك أيضًا فتح [صفحة الإصدار](https://github.com/mraziz2005-hue/AzizIDE/releases/tag/v0.7.1)، ثم توسيع **Assets** واختيار الملف نفسه.

**ملف `AzizIDE_0.7.1_Ubuntu_Installer.zip` غير مرفق بالإصدار عند مراجعة التعليمات بتاريخ 17 نوفمبر 2026.** لا تستخدم `Source code (zip)` أو `Code → Download ZIP` بدلًا منه؛ المستودع يحتوي README فقط حاليًا.

تحتاج جلسة سطح مكتب Linux، وصلاحية `sudo` للتثبيت، واتصال إنترنت عند تنزيل الحزمة واعتماديات Snap. لا تحتاج تثبيت Python أو PySide6 يدويًا لتثبيت نسخة Snap.

لمعرفة النظام والمعمارية:

```bash
cat /etc/os-release
uname -m
```

الناتج `x86_64` يطابق معمارية الحزمة.

### 1. تجهيز Snap — مرة واحدة فقط

افحص أولًا:

```bash
snap version
```

إذا ظهرت إصدارات `snap` و`snapd` وكان دعم Classic مجهزًا، انتقل إلى الخطوة 2. إذا سبق تجهيز Snap لتطبيق آخر على الجهاز، لا تحتاج إعادة تجهيزه لكل تطبيق.

إذا ظهر `command not found`، اتبع قسم توزيعتك فقط.

#### Ubuntu

إذا لم يكن Snap مثبتًا:

```bash
sudo apt update
sudo apt install snapd
sudo systemctl enable --now snapd.socket
```

سجّل خروجًا من جلسة سطح المكتب وادخل مجددًا، أو أعد تشغيل الجهاز، ثم انتقل إلى الخطوة 2.

#### Fedora Workstation / KDE التقليدي

Fedora يستخدم `dnf`، وليس `apt`.

ثبّت Snap وفعّل الخدمة:

```bash
sudo dnf install snapd
sudo systemctl enable --now snapd.socket
```

أنشئ مسار Classic إذا لم يكن موجودًا:

```bash
if [ ! -e /snap ] && [ ! -L /snap ]; then
    sudo ln -s /var/lib/snapd/snap /snap
fi
```

سجّل خروجًا وادخل مجددًا، أو أعد تشغيل الجهاز. إغلاق الطرفية وحده لا يُحدّث جلسة سطح المكتب.

تحقق:

```bash
snap version
```

ثم انتقل إلى الخطوة 2. هذه الخطوات لفيدورا التقليدي وليست تعليمات مؤكدة للأنظمة غير القابلة للتغيير مثل Silverblue / Kinoite.

#### Debian

```bash
sudo apt update
sudo apt install snapd
sudo systemctl enable --now snapd.socket
```

سجّل خروجًا وادخل مجددًا، ثم نفّذ خطوة snapd الموصى بها في دليل Debian الرسمي لـ Snap:

```bash
sudo snap install snapd
```

ثم انتقل إلى الخطوة 2.

#### Linux Mint

قد يمنع Mint تثبيت Snap بملف `nosnap.pref`. إذا اخترت استخدام Snap، انقل ملف المنع إلى نسخة احتياطية إن كان موجودًا:

```bash
if [ -f /etc/apt/preferences.d/nosnap.pref ]; then
    sudo mv -n /etc/apt/preferences.d/nosnap.pref /etc/apt/preferences.d/nosnap.pref.azizide-backup
fi
```

هذا يغيّر تفضيل Mint الذي يمنع تثبيت Snap. إذا بقي الملف الأصلي بسبب وجود نسخة احتياطية بالاسم نفسه، اختر اسم نسخة احتياطية آخر قبل المتابعة.

ثم:

```bash
sudo apt update
sudo apt install snapd
sudo systemctl enable --now snapd.socket
```

سجّل خروجًا وادخل مجددًا، أو أعد تشغيل الجهاز، ثم انتقل إلى الخطوة 2.

#### التوزيعات الأخرى

راجع [دليل تثبيت Snap حسب التوزيعة](https://snapcraft.io/docs/installing-snapd/) لتجهيز `snapd` والخدمة ودعم **Classic**، ثم تابع الخطوة 2.

### 2. تثبيت حزمة AzizIDE

حمّل ملف Snap وضعه في مجلد التنزيلات، ثم:

```bash
cd ~/Downloads
ls -lh azizide_0.7.1_amd64.snap
```

إذا كان مجلد التنزيلات باسم مختلف، افتحه في مدير الملفات واختر **فتح الطرفية هنا** بدل أمر `cd ~/Downloads`.

إذا ظهر الملف، ثبّته:

```bash
sudo snap install --dangerous --classic ./azizide_0.7.1_amd64.snap
```

تحقق من نجاح التثبيت:

```bash
snap list azizide
```

- `--dangerous`: يسمح بتثبيت ملف محلي دون التحقق من توقيعه عبر المتجر؛ استخدم ملف إصدار المشروع الموثوق.
- `--classic`: يتيح نمط Classic ذي الوصول الأوسع للنظام.
- هذه طريقة تثبيت محلي من GitHub؛ لا تفترض أن `sudo snap install azizide` من المتجر متاح.

### 3. تشغيل AzizIDE

```bash
snap run azizide
```

أو ابحث عن **AzizIDE** في قائمة التطبيقات.

**شغّل التطبيق بحسابك العادي، دون `sudo`.** بعد نجاح التثبيت لا تحتاج بقاء ملف التنزيل `.snap` لتشغيل النسخة المثبتة.

### 4. إذا اشتغل ولم يظهر في قائمة التطبيقات

سجّل خروجًا وادخل مجددًا أولًا. إذا بقي غير ظاهر، افحص اختصارات الحزمة:

```bash
ls -l /var/lib/snapd/desktop/applications/azizide*.desktop
```

إذا ظهر الملف بالاسم **`azizide_azizide.desktop`**، نفّذ:

```bash
if [ -f /var/lib/snapd/desktop/applications/azizide_azizide.desktop ]; then
    mkdir -p "$HOME/.local/share/applications"
    ln -sfnT /var/lib/snapd/desktop/applications/azizide_azizide.desktop "$HOME/.local/share/applications/azizide_azizide.desktop"
else
    printf '%s\n' 'لم يُعثر على ملف الاختصار المتوقع؛ راجع نتيجة ls قبل إنشاء الرابط.'
fi
```

هذا يربط اختصار الحزمة بقائمة تطبيقات حسابك. إذا سبق تخصيص اختصار محلي بنفس الاسم، احتفظ بنسخة منه قبل استبداله.

أغلق القائمة وافتحها وابحث عن **AzizIDE**. إذا لم تتحدث، سجّل خروجًا وادخل مجددًا.

إذا ظهر اسم ملف مختلف، استخدم الاسم الفعلي الظاهر في نتيجة الفحص بدل تخمينه. وإذا لم يظهر أي ملف، لا تنشئ رابطًا لملف مفقود؛ أرسل نتيجة `snap list azizide` في بلاغ المشكلة.

### 🐍 مثبّت Python — غير متاح للتحميل حاليًا

كانت التعليمات السابقة تشير إلى `AzizIDE_0.7.1_Ubuntu_Installer.zip`، لكنه **غير موجود ضمن Assets حاليًا**. استخدم نسخة Snap أعلاه.

لمن يحتفظ بنسخة المثبّت الأصلية سابقًا، هذه تعليماته الموثقة لـ Ubuntu فقط، ولا تُعد تأكيدًا لتوافق سكربت المثبّت مع Fedora:

```bash
sudo apt update
sudo apt install python3 python3-venv python3-pip unzip
cd ~/Downloads
unzip -n AzizIDE_0.7.1_Ubuntu_Installer.zip
cd AzizIDE_0.7.1_Ubuntu_Installer
bash install.sh
```

وفق وصف المثبّت السابق، يُنشئ بيئة Python ويثبت المكتبات ويضيف اختصارًا. لا تستخدم `sudo` لتشغيل `install.sh`. أمر تشغيل هذه النسخة:

```bash
~/.local/bin/azizide
```

هذه الأوامر ليست مطلوبة لنسخة Snap، ولا يمكن تنفيذها دون امتلاك أرشيف المثبّت الفعلي.


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
- نسخة Snap تحتاج `snapd` ودعم Classic ومعمارية x86_64؛ لا تحتاج تثبيت مكتبات Python يدويًا.
- طريقة Python تحتاج **Python 3** و`venv` واتصال إنترنت لتنزيل المكتبات أول مرة.
- المكتبات الأساسية في الإصدار: **PySide6** و**Paramiko**.
- تشغيل لغات البرمجة الأخرى يعتمد على أدوات التشغيل المثبتة على الجهاز.

## 🔄 تحديث AzizIDE

عند صدور إصدار جديد، بتلقاه في صفحة **[Releases](https://github.com/mraziz2005-hue/AzizIDE/releases)** في نفس المستودع.

- **إذا ثبّتّ Snap محليًا:** حمّل حزمة `.snap` الجديدة وثبّتها بالطريقة نفسها.
- **إذا تستخدم مثبّت Python القديم:** انتظر نشر أرشيف مثبّت جديد وتعليماته؛ أرشيف المثبّت غير مرفق بالإصدار الحالي.
- **التحديث التلقائي من GitHub غير متوفر حاليًا**؛ التحديث يدوي إلى أن نضيف آلية مناسبة.

> وفق وصف المثبّت السابق، يحتفظ مثبّت Python بنسخة احتياطية من ملف البرنامج قبل تحديثه؛ سكربته غير متاح حاليًا في المستودع للتحقق منه.

## 🔒 الخصوصية

في **AzizIDE**، تبقى ملفات مشاريعك المحلية على جهازك. الاتصال عبر SSH مخصص لتصفح ملفات السيرفر والبحث فيها للقراءة فقط، ولا يحفظ البرنامج كلمة مرور SSH ضمن إعدادات الاتصال. ولحماية مشروعاتك، احتفظ بمفاتيح الوصول وملفات الإعدادات الخاصة خارج المستودعات العامة.

## 🛠️ حل المشكلات الشائعة

### Snap غير موجود أو الخدمة لا تستجيب

- `snap: command not found`: اتبع قسم تجهيز Snap لتوزيعتك.
- `apt: command not found` على Fedora: استخدم `dnf`.
- `snapd unavailable` أو `cannot communicate with server`: على الأنظمة التقليدية المذكورة أعلاه افحص الخدمة:

```bash
sudo systemctl enable --now snapd.socket
systemctl status snapd.socket --no-pager
snap version
```

### خطأ متعلق بـ Classic أو مسار /snap

افحص:

```bash
ls -ld /snap /var/lib/snapd/snap
```

على Fedora التقليدي، إذا غاب `/snap` وكان المسار الثاني موجودًا، اتبع خطوة إنشاء الرابط في قسم Fedora. إذا كان `/snap` موجودًا، لا تحذفه أو تستبدله عشوائيًا؛ أرفق نتيجة الفحص. على الأنظمة الأخرى راجع دليل توزيعتك.

### ملف التثبيت غير موجود أو المعمارية غير مناسبة

- `No such file or directory`: تحقق من اسم الملف والمجلد باستخدام `pwd` و`ls`.
- خطأ معمارية أو `Exec format error`: تحقق من `uname -m`؛ الحزمة الحالية تحتاج x86_64.

### التطبيق لا يظهر أو لا يفتح

إذا يعمل من الطرفية ولا يظهر بالقائمة، اتبع الخطوة 4 أعلاه. إذا لا يفتح أو يغلق فورًا، شغّله من الطرفية وانسخ الخطأ:

```bash
snap run azizide
```

لا تفترض أن تغيير إعدادات Qt أو تعطيل حمايتها يحل المشكلة دون قراءة الخطأ أولًا.

### مشاكل داخل التطبيق

| المشكلة | ما الذي تفحصه؟ |
|---|---|
| Run لا يعمل | وجود مفسّر اللغة أو أداة تشغيلها على الجهاز، ورسالة Run Results |
| SSH لا يتصل | عنوان السيرفر والمنفذ وبيانات الدخول وإعدادات SSH |
| Preview لا تظهر | افتح ملف HTML محليًا، وشغّل التطبيق من الطرفية لقراءة الخطأ |
| مشكلة venv في مثبّت Python القديم على Ubuntu | توفر حزمة python3-venv؛ لا تنطبق هذه الخطوة على Snap |

عند فتح [بلاغ](https://github.com/mraziz2005-hue/AzizIDE/issues)، أرفق اسم التوزيعة وإصدارها والمعمارية ورسالة الخطأ ونتيجة:

```bash
snap version
snap list azizide
```

لا ترسل كلمات المرور أو مفاتيح SSH الخاصة أو محتوى ملفات مشروع حساس.

## 🗑️ إزالة نسخة Snap

أغلق البرنامج واحفظ عملك واحتفظ بإعداداتك المهمة، ثم:

```bash
sudo snap remove azizide
```

إذا أضفت رابط الاختصار يدويًا بالطريقة أعلاه، أزله:

```bash
if [ -L "$HOME/.local/share/applications/azizide_azizide.desktop" ]; then
    rm -- "$HOME/.local/share/applications/azizide_azizide.desktop"
fi
```

هذه ليست أوامر حذف مشاريعك المحفوظة خارج بيانات الحزمة.

## 📚 مصادر تجهيز Snap

رُوجعت تعليمات التثبيت بتاريخ **17 نوفمبر 2026**. هذه المصادر تشرح تجهيز Snap، ولا تثبت اختبار AzizIDE على كل نظام:

- [Ubuntu](https://snapcraft.io/docs/tutorials/install-the-daemon/ubuntu/)
- [Fedora](https://snapcraft.io/docs/tutorials/install-the-daemon/fedora/)
- [Debian](https://snapcraft.io/docs/tutorials/install-the-daemon/debian/)
- [Linux Mint](https://snapcraft.io/docs/tutorials/install-the-daemon/linux-mint/)


## 📁 ملفات المشروع

البنية التالية موثقة لنسخة ملفات المشروع السابقة؛ هذه الملفات ليست موجودة في المستودع الحالي ولا في ZIP مصدر GitHub التلقائي:

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

**Install the available local Snap:**

Download `azizide_0.7.1_amd64.snap` from the v0.7.1 release. Prepare snapd and classic support using the distribution-specific instructions above, then:

```bash
cd ~/Downloads
sudo snap install --dangerous --classic ./azizide_0.7.1_amd64.snap
snap run azizide
```

The build targets x86_64 / AMD64, not ARM or 32-bit devices. Run the app without sudo.

Fedora setup instructions are provided, but AzizIDE's Fedora run has not yet been confirmed. If the app runs but is missing from the menu, follow step 4 above: inspect the actual desktop-file name before creating its user-menu symlink.

The previously documented Python installer ZIP is **not currently attached** to the release. GitHub's automatic source ZIP is not a substitute; the repository currently contains only this README.

**Status:** early preview · **Platform:** Ubuntu/Linux · **Updates:** manual via GitHub Releases.

---

<div align="center">

**Made with 🐧 for Linux users.**

*Code comfortably. Enjoy the process.*

</div>
