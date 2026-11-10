# دليل إنشاء APK لتطبيق Billing App

## المتطلبات
- Flutter SDK متوافق مع قيمة Dart المحددة في `pubspec.yaml`.
- Android Studio أو Android SDK وJava 17 أو أحدث.

## إنشاء APK على الحاسوب
افتح الطرفية داخل مجلد المشروع ونفّذ:

```bash
flutter doctor
flutter pub get
flutter analyze
flutter build apk --release
```

ستجد الملف الناتج هنا:

`build/app/outputs/flutter-apk/app-release.apk`

## إنشاء APK عبر GitHub Actions
1. ارفع مجلد المشروع إلى مستودع GitHub.
2. افتح تبويب **Actions**.
3. اختر **Build Android APK** ثم **Run workflow** (أو ادفع تغييرا إلى فرع `main` أو `master`).
4. بعد نجاح العملية، افتح نتيجة التشغيل ونزّل artifact باسم `billing-app-release-apk`.

## ملاحظات
- إعداد التوقيع الحالي يستخدم مفتاح debug؛ مناسب للتجربة والتثبيت الاختباري، وليس للنشر النهائي على Google Play.
- لم يتم اختبار البناء في هذه البيئة لعدم توفر Flutter SDK وAndroid SDK هنا.
