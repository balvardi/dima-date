# dima-date - تاریخ شمسی برای وردپرس ⏳

> ⏳ تبدیل تمام تاریخ‌ها در وردپرس به تاریخ شمسی (جلالی) با قابلیت تنظیم قالب در ادمین. ساخته شده با PHP 8+.

[![License](https://img.shields.io/badge/license-GPL--2.0-blue)](https://github.com/balvardi/dima-date/blob/main/LICENSE)

**dima-date** یک پلاگین سبک، قدرتمند و کاملاً قابل تنظیم برای **وردپرس** است که تمام تاریخ‌های نمایشی را در هسته وردپرس (Frontend و Admin) به **تقویم شمسی (جلالی)** تبدیل می‌کند.

---

## 🔖 ویژگی‌ها

✅ تبدیل تمام تاریخ‌ها به شمسی  
✅ صفحه تنظیمات در بخش ادمین وردپرس  
✅ پشتیبانی از قالب‌های مختلف (`Y/m/d`, `l، j F Y H:i` و غیره)  
✅ REST API Support – `/wp-json/wp/v2/posts`  
✅ بدون نیاز به `jdate()` یا افزونه سروری  
✅ سازگار با PHP 8.0+

---

## 👤 توسعه‌دهنده

- **نویسنده:** [R.Balvardi](mailto:r.balvardi@gmail.com)
- **وب‌سایت:** [dimagroup.ir](https://dimagroup.ir)

---

## 📁 نحوه نصب

### دستی:
1. فایل `dima-date.zip` را دانلود کنید.
2. در وردپرس بروید: **Plugins > Add New**
3. روی **Upload Plugin** کلیک کنید و فایل زیپ را آپلود کنید.
4. پلاگین را فعال کنید.

### از طریق گیت‌هاب:
```bash
git clone https://github.com/balvardi/dima-date.git
```

و پوشه `dima-date` را به `wp-content/plugins/` منتقل کنید.

---

## ⚙️ تنظیمات

بعد از فعال‌سازی:
- بروید به: **Settings > تاریخ شمسی**
- قالب تاریخ دلخواه را تعیین کنید.  
مثال:
- `Y/m/d` → `1404/02/20`
- `l، j F Y` → `جمعه، 20 اردیبهشت 1404`
- `l، j F Y H:i` → `جمعه، 20 اردیبهشت 1404 13:45`

---

## 🧪 پشتیبانی از REST API

وقتی پست‌ها را از طریق `/wp-json/wp/v2/posts` دریافت کنید، فیلدهای `date` و `modified` به صورت خودکار به تاریخ شمسی تبدیل می‌شوند.

---

## 📜 لایسنس

این پروژه تحت لایسنس [GNU General Public License v2.0](https://github.com/balvardi/dima-date/blob/main/LICENSE) منتشر شده است.

---

## 💬 پشتیبانی و همکاری

اگر باگی پیدا کردید یا پیشنهادی داشتید، حتماً Issue باز کنید یا Pull Request بفرستید.

همچنین اگر سوالی داشتید، می‌توانید از طریق ایمیل تماس بگیرید:  
📧 [r.balvardi@gmail.com](mailto:r.balvardi@gmail.com)

---

## ❤️ منابع

این پلاگین از یک نسخه اصلاح شده از کتابخانه [jDateTime](https://github.com/sallar/jDateTime) برای تبدیل تاریخ استفاده می‌کند.
```
