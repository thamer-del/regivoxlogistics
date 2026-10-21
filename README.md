# Regivox Logistics | موقع ريجيفوكس اللوجستية

موقع ثابت بصفحة واحدة، عربي (RTL) وإنجليزي (LTR)، جاهز للاستضافة على GitHub Pages.

## محتويات المجلد

- `index.html` الموقع كاملًا (الشعار والتصميم والسكربت داخل الملف).
- `favicon.png` أيقونة تبويب المتصفح.
- `og-image.png` صورة المعاينة عند مشاركة الرابط في واتساب ولينكدإن وغيرها.
- `privacy.html` صفحة سياسة الخصوصية بالعربي والإنجليزي، ورابطها بعد النشر `https://regivox.org/privacy.html`.

## 1) رفع الموقع إلى GitHub

1. سجّل الدخول إلى github.com، ثم **New repository**.
2. الاسم `regivox-logistics`، الظهور **Public**، ثم **Create repository**.
3. اضغط **uploading an existing file**، اسحب الملفات الأربعة (`index.html` و`privacy.html` و`favicon.png` و`og-image.png`)، ثم **Commit changes**.
4. من **Settings ← Pages**: Source = **Deploy from a branch**، Branch = **main** و **/ (root)**، ثم **Save**.
5. بعد دقيقة أو دقيقتين يظهر الرابط المؤقت `https://USERNAME.github.io/regivox-logistics/`.

## 2) ربط الدومين regivox.org (المسجل في Squarespace)

1. في GitHub: **Settings ← Pages ← Custom domain**، اكتب `regivox.org` ثم **Save**.
2. في Squarespace: account.squarespace.com/domains ← regivox.org ← **DNS** (DNS Settings).
3. احذف سجلات A و CNAME القديمة التي تشير إلى موقع Squarespace (للمضيف `@` وللمضيف `www`) فقط.
4. أضف أربعة سجلات من النوع A، المضيف `@`:
   - `185.199.108.153`
   - `185.199.109.153`
   - `185.199.110.153`
   - `185.199.111.153`
5. أضف سجل CNAME، المضيف `www`، القيمة `USERNAME.github.io` (اسم حسابك في GitHub بدون اسم المستودع).
6. انتظر من دقائق إلى 24 ساعة، ثم فعّل **Enforce HTTPS** في Settings ← Pages.

**تنبيه مهم للإيميل:** لا تحذف ولا تعدّل سجلات MX ولا TXT ولا أي سجل خاص بـ Google Workspace، حتى لا يتوقف بريد الشركة.

## 3) نموذج طلب عرض السعر

النموذج يرسل الطلبات إلى `thamer@regivox.org` عبر خدمة FormSubmit (مجانية وبدون حساب).

- أول طلب تجريبي ترسله من الموقع يصلك عليه إيميل تفعيل من FormSubmit. افتحه واضغط التفعيل، وبعدها تصل الطلبات مباشرة.
- إذا فشل الإرسال لأي سبب، يظهر للعميل رابط بريد جاهز بدل ضياع الطلب.
- لتغيير جهة الاستقبال أو الخدمة: ابحث في `index.html` عن `FORM_ENDPOINT` و `FORM_RECIPIENT` في بداية السكربت.

## 4) صفحة سياسة الخصوصية

- الرابط في فوتر الموقع وتحت نموذج عرض السعر يفتح `privacy.html`.
- عند أي تحديث للسياسة عدّل النص وتاريخ "آخر تحديث" في النسختين العربية والإنجليزية داخل `privacy.html`.
- راجع السياسة دوريًا مع الممارسات الفعلية للشركة (الخدمات التقنية المستخدمة في الموقع والنموذج والاستضافة).

## 5) تعديل الموقع لاحقًا

افتح `index.html` في GitHub، اضغط أيقونة القلم، عدّل النص (كل نص له نسخة `data-l="ar"` ونسخة `data-l="en"`)، ثم **Commit changes**. يتحدث الموقع خلال دقيقة تقريبًا.
