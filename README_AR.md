# تطبيق الأستاذي للأندرويد

هذا مشروع Android بسيط يغلّف ملف HTML المرفق داخل WebView حتى يمكن بناء APK.

## البناء عبر GitHub Actions
1. ارفع جميع محتويات هذا المجلد إلى مستودع GitHub جديد.
2. افتح تبويب Actions.
3. شغّل `Build Android APK` عبر Run workflow، أو ادفع التغييرات إلى main.
4. بعد نجاح البناء افتح نتيجة التشغيل (Actions run).
5. نزّل Artifact باسم `alustadhi-debug-apk` وفك ضغطه لتحصل على `app-debug.apk`.

## البناء محلياً
يتطلب JDK 17 و Android SDK 35 و Gradle 8.9:
`gradle assembleDebug`

## ملاحظات
- التطبيق يستخدم ملف HTML محلياً داخل `app/src/main/assets/index.html`.
- البيانات المحفوظة عبر localStorage تبقى داخل مساحة بيانات التطبيق.
- بعض الميزات في HTML تستدعي مكتبات وخدمات عبر الإنترنت؛ لذلك تحتاج اتصالاً بالإنترنت.
- هذا مشروع APK تجريبي (debug) وليس إصداراً منشوراً أو موقّعاً للنشر في المتجر.
- معرّف التطبيق: `com.alustadhi.school`.
