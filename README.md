# Yr Player Pro — YRP

[![Release](https://img.shields.io/badge/release-v1.0.7-2BD47D?style=for-the-badge)](https://github.com/yazid900/y-player_pro/releases/tag/v1.0.7)
![Platform](https://img.shields.io/badge/platform-Windows%20x64-0078D6?style=for-the-badge)
![Stack](https://img.shields.io/badge/stack-WPF%20%7C%20.NET%2010-512BD4?style=for-the-badge)
![Wallet](https://img.shields.io/badge/identity-MAC%20%2B%20Device%20Key-E8B44A?style=for-the-badge)

مشغّل IPTV سريع لواجهة Windows، بهوية **YRP** الجديدة، وكاش دائم على القرص، وإدارة قوائم عن بُعد عبر موقع ويب آمن — بدون فتح منافذ أو إعدادات شبكة.

---

## تنزيل سريع

| الملف | الوصف | التحميل |
|---|---|---|
| `YrPlayerPro_Setup_v1.0.7.exe` | مثبّت Windows x64 كامل، لا يحتاج تثبيت .NET | [تحميل المثبّت](https://github.com/yazid900/y-player_pro/releases/download/v1.0.7/YrPlayerPro_Setup_v1.0.7.exe) |
| `IbPlayerClone_Fixed.zip` | المصدر الكامل للمشروع | [تحميل المصدر](https://github.com/yazid900/y-player_pro/releases/download/v1.0.7/IbPlayerClone_Fixed.zip) |
| `Web.zip` | نسخة الموقع الخلفي PHP/MySQL | [تحميل الموقع](https://github.com/yazid900/y-player_pro/releases/download/v1.0.7/Web.zip) |
| `SHA256SUMS.txt` | بصمات التحقق من الملفات | [عرض البصمات](https://github.com/yazid900/y-player_pro/releases/download/v1.0.7/SHA256SUMS.txt) |

> يُنصح دائماً بتنزيل الإصدار من صفحة [Releases](https://github.com/yazid900/y-player_pro/releases) والتحقق من البصمة قبل التثبيت.

---

## أبرز المزايا

- **كاش دائم:** تُحفظ كل القنوات والأفلام والمسلسلات على القرص، وتُفتح القائمة فوراً عند العودة إليها.
- **قوائم ضخمة بانتظار مستمر:** يعمل مع أكثر من 16,000 قناة وأكثر من 65,000 فيلم/مسلسل من نفس المصدر، مع شريط تقدّم حتى 100% وانتظار غير محدود حتى تكتمل القائمة.
- **دخول مباشر للمشاهدة:** النقر على بطاقة القائمة يفعّلها ويفتح شاشة المشاهدة فوراً بينما يستمر التحميل في الخلفية.
- **إدارة عن بُعد:** أضف القوائم وفعّلها واحذفها من الموقع، وستظهر داخل البرنامج تلقائياً خلال ثوانٍ.
- **هوية بصرية:** خط **Tajawal** مضمّن، أخضر جزائري `#2BD47D` وذهبي `#E8B44A`، وحواف شبه مربّعة.
- **حماية الهوية:** الدخول إلى الموقع بـ **MAC** و**Device Key** فقط، ولا توجد أوامر تحكم بالجهاز عن بُعد.

---

## أول تشغيل

1. شغّل `YrPlayerPro_Setup_v1.0.7.exe` واتبع معالج التثبيت.
2. عند أول إقلاع، سترى شاشة تفعيل تعرض **MAC** و**Device Key** ورابط الموقع.
3. افتح [https://yr-player.page.gd/](https://yr-player.page.gd/) وأدخل نفس القيم لإدارة قوائمك.
4. أضف قائمة Xtream أو رابط M3U من داخل البرنامج أو من الموقع، ثم انقر على البطاقة للبدء بالمشاهدة.

يتم نسخ إعداداتك وقوائمك وكاش النسخ السابقة تلقائياً عند الترقية، دون فقدان البيانات.

---

## الموقع المرافق

- الرابط: [https://yr-player.page.gd/](https://yr-player.page.gd/)
- الملفات: `Web.zip`
- قاعدة البيانات: MySQL / PHP
- المزامنة تعمل عبر HTTPS فقط، دون port forwarding.

راجع `Web/README_AR.md` داخل ملف المصدر أو `README_AR.md` داخل `Web.zip` لخطوات النشر والتجربة المحلية بـ Laragon.

---

## البناء من المصدر

```powershell
git clone https://github.com/yazid900/y-player_pro.git
cd y-player_pro
# استخرج IbPlayerClone_Fixed.zip إلى مجلد IbPlayerClone بجانب IbPlayerClone.slnx
dotnet build IbPlayerClone\IbPlayerClone.csproj -c Release
```

لإعادة توليد المثبّت بعد تثبيت Inno Setup 6:

```powershell
.\IbPlayerClone\build_installer.ps1
```

النتيجة المتوقعة دائماً: `0 Warning(s), 0 Error(s)`.

---

## التحقق من الملفات

بعد التنزيل، تحقق من البصمة:

```powershell
Get-FileHash .\YrPlayerPro_Setup_v1.0.7.exe -Algorithm SHA256
```

قارن النتيجة مع `SHA256SUMS.txt` المرفق بالإصدار.

---

## الخصوصية

- التطبيق يرسل فقط **MAC** و**Device Key** وبيانات القوائم إلى الموقع المرافق.
- لا يوجد أي أمر تحكم بالجهاز (تشغيل/إيقاف/ملء شاشة) عبر الويب.
- بيانات القنوات تُخزّن محلياً على جهازك في `%APPDATA%\YrPlayerPro\cache`.

---

## الدعم

افتح [Issue](https://github.com/yazid900/y-player_pro/issues) أو [مناقشة](https://github.com/yazid900/y-player_pro/discussions) عند الحاجة، واذكر رقم الإصدار ونوع القائمة (Xtream أو M3U).
