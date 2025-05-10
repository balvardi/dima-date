# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/ ), and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html ).

## [1.0.0-beta] - 2025-04-05

### Added
- Initial beta release of Dima Date plugin.
- Support for converting all visible dates in WordPress (frontend & admin).
- Admin settings page for customizing date format.
- REST API support for returning Jalali dates via `/wp-json/wp/v2/posts`.
- Internal Jalali date conversion library (no server dependencies like jdate()).
- PHP 8+ compatibility with modern syntax (enums, union types, arrow functions).

- # Changelog

همه تغییرات مهم در این پروژه بر اساس [Keep a Changelog](https://keepachangelog.com/en/1.0.0/ ) و [Semantic Versioning](https://semver.org/spec/v2.0.0.html ) گزارش شده است.

## [2.1.0] - 2025-04-10
### Added
- پشتیبانی از قالب زمانی (`H:i`) برای ساعت و دقیقه.
- پشتیبانی از ورودی `WP_Post` در تمام فیلترها.
- پیشنهاد قالب زمانی در صفحه تنظیمات: `l، j F Y H:i`.

### Fixed
- خطای `Deprecated: Creation of dynamic property jDateTime::$timestamp` با تعریف صریح متغیر در کلاس.
- مشکل نمایش `H:i` در قالب‌های تاریخ.
- عدم پذیرش `WP_Post` در فیلترهای وردپرس مثل `get_the_date()`.

### Changed
- به‌روزرسانی ساختار کلاس `jDateTime` برای سازگاری با PHP 8.2+
- بهبود مدیریت انواع ورودی در تابع `dima_convert_to_jalali()`
- اضافه کردن پشتیبانی از قالب‌های پیچیده تاریخ و زمان

---

## [2.0.0] - 2025-04-05
### Added
- اولین نسخه عمومی با پشتیبانی از PHP 8+.
- تبدیل تمام تاریخ‌ها در وردپرس (Frontend و Admin).
- صفحه تنظیمات در ادمین برای تغییر قالب تاریخ.
- پشتیبانی از REST API.
- کتابخانه داخلی برای تبدیل تاریخ بدون نیاز به `jdate()` سرور.
