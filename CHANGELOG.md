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