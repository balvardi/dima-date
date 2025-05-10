# dima-date - Persian (Jalali) Date Plugin for WordPress 🌟

> ⏳ Convert all dates in WordPress to Jalali (Solar Hijri) calendar with full admin settings and PHP 8+ support.

[![License](https://img.shields.io/badge/license-GPL--2.0-blue)](https://github.com/yourusername/dima-date/blob/main/LICENSE)

A lightweight, modern, and fully customizable **Persian date plugin for WordPress**, built with PHP 8+ features like enums, union types, and named arguments. This plugin converts all visible dates on both frontend and backend to the Jalali (Shamsi) calendar without relying on server-side extensions like `jdate()`.

---

## 📌 Features

- ✅ Converts all dates shown in WordPress (posts, comments, edit screens, etc.) to Jalali.
- ✅ Admin settings page to customize date format (`l، j F Y`, `Y/m/d`, etc.)
- ✅ REST API support – dates returned by `/wp-json/wp/v2/posts` are also converted.
- ✅ No need for `jdatetime` or `jdate()` PHP extension – uses an internal library.
- ✅ Built with modern PHP 8+ syntax.
- ✅ RTL & Persian-ready UI.

---

## 📁 Folder Structure

```
dima-date/
├── dima-date.php        ← Main plugin file
├── admin/
│   └── settings.php     ← Admin settings page
└── vendor/
    ├── jdf.php          ← Wrapper for jdate() function
    └── jdf-lib.php      ← Jalali date conversion library
```

---

## 🛠 Requirements

- WordPress 5.0+
- PHP 8.0+
- No external libraries or extensions needed.

---

## 📦 Installation

### Manual Installation

1. Download the latest release from GitHub.
2. Upload the `dima-date` folder to the `wp-content/plugins/` directory.
3. Go to **Plugins > Installed Plugins** in your WordPress dashboard.
4. Activate the **Dima Date - Persian Date** plugin.
5. Go to **Settings > تاریخ شمسی** to customize the date format.

---

## ⚙️ Settings

You can change the default date format under:
> **Settings > تاریخ شمسی**

Supported Format Keys:
| Key | Description           | Example         |
|-----|-----------------------|-----------------|
| `Y` | 4-digit year          | `1402`          |
| `y` | 2-digit year          | `02`            |
| `F` | Full month name       | `دی`            |
| `m` | 2-digit month         | `10`            |
| `n` | Numeric month         | `10`            |
| `l` | Full day name         | `دوشنبه`        |
| `d` | 2-digit day           | `05`            |
| `j` | Numeric day           | `5`             |

Examples:
- `Y/m/d` → `1402/10/05`
- `l، j F Y` → `دوشنبه، 5 دی 1402`

---

## 🧪 REST API Support

When fetching posts via the REST API (`/wp-json/wp/v2/posts`), the `date` and `modified` fields will be automatically returned in Jalali format based on your selected date format.

Example response:
```json
{
  "date": "1402/10/05",
  "modified": "1402/10/07"
}
```

---

## 🧑‍💻 Developers

Want to contribute or extend this plugin?

### Hooks Available

- `dima_date_jalali_format`: Modify the final Jalali date before output.
  ```php
  add_filter('dima_date_jalali_format', function($formatted_date) {
      return '📅 ' . $formatted_date;
  });
  ```

- `dima_date_format`: Change the date format dynamically.
  ```php
  add_filter('dima_date_format', function($format) {
      return 'Y/m/d';
  });
  ```

---

## 📜 License

This project is licensed under the [GNU General Public License v2.0](https://github.com/yourusername/dima-date/blob/main/LICENSE).

---

## 💬 Feedback & Contributions

Have a feature idea? Found a bug? Feel free to open an issue or submit a pull request!

Contributions are always welcome 👏

---

## ❤️ Credits

This plugin uses a modified version of the [jDateTime](https://github.com/sallar/jDateTime) library for Jalali date conversion.
```
