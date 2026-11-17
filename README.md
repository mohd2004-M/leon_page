# Leon – Agency Landing Page

صفحة واحدة (One Page) لوكالة إبداعية بتصميم minimal، مطابقة لقالب [Leon – PSD Agency Template](https://www.graphberry.com/item/leon-psd-agency-template).
مبنية بـ HTML و CSS و JavaScript، مع Font Awesome للأيقونات و Google Fonts للخطوط.

## هيكل المشروع

```
leon-page/
├── index.html          ← هيكل الصفحة + JavaScript (القائمة الجانبية)
├── README.md           ← هذا الملف
├── css/
│   ├── main.css        ← كل تنسيقات الصفحة
│   └── all.min.css     ← ملف Font Awesome (من مكتبتك)
├── webfonts/           ← خطوط Font Awesome (من مكتبتك)
└── images/
    └── hero.jpg        ← صورة الجبال
```

> **مهم:** `all.min.css` بيدوّر على الخطوط بالمسار `../webfonts/`، لذلك مجلد `webfonts` لازم يكون بجذر المشروع، جنب مجلد `css` (مش جواته).

## إضافة Font Awesome (من المكتبة المنزّلة)

1. من مجلد مكتبة Font Awesome، انسخ `css/all.min.css` وحطه داخل `css/` بالمشروع.
2. انسخ مجلد `webfonts` كامل وحطه بجذر المشروع (جنب `css` و `index.html`).

بدون هالملفات الأيقونات ما رح تظهر.

## أقسام الصفحة

| القسم | الـ id | الوصف |
|---|---|---|
| Header | – | الشعار "lo" وزر القائمة |
| Side Menu | – | قائمة جانبية داكنة تفتح من اليمين |
| Hero | `#home` | عنوان "Hello There!" وصورة الجبال |
| Features | – | ثلاث ميزات بأيقونات |
| Services | `#services` | أربع خدمات + صورة |
| Portfolio | `#portfolio` | ثلاث بطاقات مشاريع + زر Show Me More |
| About | `#about` | صورة بشكل L أخضر + نص |
| Contact | `#contact` | البريد وروابط التواصل |
| Footer | – | شريط حقوق النشر |

## تنظيم الكود

**`css/main.css`** مقسّم لأجزاء مرقّمة بتعليقات:
Design tokens (الألوان والخط)، Reset، Header، Side menu، Hero، Features، Services، Portfolio، About، Contact، Footer، Responsive.

**`index.html`** بيربط الملفات بهالترتيب داخل `<head>`:
1. Google Fonts (Work Sans) برابط.
2. `css/all.min.css` (Font Awesome).
3. `css/main.css`.

**JavaScript** (أسفل `index.html`): وظيفة `setMenu()` لفتح وإغلاق القائمة الجانبية.

**الأيقونات:** `<i class="fa-solid fa-gem"></i>` للأيقونات العادية، و `fa-brands` لأيقونات السوشيال.

## الصور

- `images/hero.jpg`: صورة الجبال (محلية).
- صور المشاريع وقسم About: روابط مباشرة من [Pixabay](https://pixabay.com) (ترخيص مجاني). إذا فشل تحميل صورة بتظهر `hero.jpg` مكانها.

## التشغيل

افتح `index.html` من المتصفح مباشرة بعد ما تضيف ملفات Font Awesome. للنشر: ارفع المجلد كامل على GitHub، ثم **Settings ← Pages** واختر الفرع `main` والمجلد `/ (root)`.
