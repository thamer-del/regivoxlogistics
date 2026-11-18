# تطبيق ريجيفوكس للجوال (Capacitor)

التطبيق عبارة عن غلاف Android يعرض نسخة `www/index.html` من الموقع داخل WebView.

## التحديث بعد أي تعديل على الموقع
```bash
cp ../index.html www/
npx cap sync android
```

## بناء APK على جهازك
1. ثبّت Android Studio.
2. من داخل مجلد `mobile/`:
```bash
npm install
npx cap open android
```
3. من Android Studio: Build > Build Bundle(s) / APK(s) > Build APK(s).

معرّف التطبيق: `org.regivox.logistics` (عدّله في `capacitor.config.json` قبل النشر).
