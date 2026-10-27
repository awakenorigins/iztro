# iztro — Zi Wei Dou Shu (Purple Star Astrology) calculation engine

> Calculate a complete 12-palace Zi Wei Dou Shu chart from birth date and time using the iztro Node.js library. Supports solar and lunar input, tứ hóa, đại hạn, and lưu niên.

[![OpenClaw Skill](https://img.shields.io/badge/OpenClaw-Skill-blueviolet)](https://github.com/NachaFromMars)

## Overview
iztro wraps the [iztro](https://github.com/SylarLong/iztro) Node.js library to generate Zi Wei Dou Shu (紫微斗數) charts for AI agents. Input a birth date, time index (0–12 mapping to the 12 Earthly Branches), gender, solar/lunar flag, and language. The library returns the full 12-palace chart with star placements, Four Transformations (tứ hóa), major luck periods (đại hạn), and annual luck (lưu niên).

## Features
- **Two input modes** — `astro.bySolar()` and `astro.byLunar()`
- **12 palaces** — Mệnh, Phụ Mẫu, Phúc Đức, Điền Trạch, Quan Lộc, Nô Bộc, Thiên Di, Tật Ách, Tài Bạch, Tử Nữ, Phu Thê, Huynh Đệ
- **Star assignments** — full star placements per palace
- **Tứ hóa** — Four Transformations
- **Đại hạn + Lưu niên** — major luck periods and annual luck
- **Languages** — `vi-VN`, `zh-CN`, `zh-TW`, `en-US`

## Usage / Quick Start
```js
const { astro } = require('./lib');
// Solar input
const result = astro.bySolar('1986-05-15', 2, '男', true, 'vi-VN');
// result.palaces → 12-palace chart
```
Time index: 0=Tý (23:00–01:00) … 11=Hợi (21:00–23:00)

## Trigger Keywords (OpenClaw)
tử vi, 紫微, lá số, mệnh cung, đại hạn, lưu niên, 12 cung, tử vi đẩu số, ziwei, purple star astrology

## Related Skills
- [ziwei](https://github.com/NachaFromMars/ziwei) — full-stack Zi Wei web app with K-line visualization

---
Part of the [NachaFromMars](https://github.com/NachaFromMars) OpenClaw skill ecosystem.
