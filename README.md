# Zibno WooCommerce iOS

نسخه اختصاصی Zibno بر پایه اپ رسمی WooCommerce iOS.

این مخزن به‌جای نگهداری کل سورس WooCommerce، فقط لایه تغییرات Zibno را نگه می‌دارد. GitHub Actions هنگام Build سورس رسمی WooCommerce iOS را در یک commit مشخص می‌گیرد، patch اختصاصی Zibno را اعمال می‌کند و سپس Build می‌زند. این ساختار باعث می‌شود آپدیت‌های upstream قابل کنترل‌تر باشند و تغییرات گرافیکی Zibno از بین نروند.

## ساختار

- `patches/zibno.patch`: تغییرات گرافیکی و برندسازی Zibno
- `UPSTREAM_COMMIT`: نسخه پایه WooCommerce iOS که patch روی آن تست شده
- `.github/workflows/zibno-build.yml`: Build خودکار برای iOS Simulator
- `.github/workflows/zibno-testflight.yml`: پایه انتشار TestFlight پس از تنظیم Signing

## وضعیت فعلی

نسخه Zibno: `0.4.0`

تغییرات فعلی شامل نام Zibno، هدر اختصاصی داشبورد، ظاهر مینیمال Tab Bar و فارسی‌سازی عنوان‌های فروشگاه، سفارش‌ها، محصولات و بیشتر است.

## تست

از تب Actions، workflow با نام **Zibno iOS Build Check** را اجرا کنید.
