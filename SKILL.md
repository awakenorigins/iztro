# Tử Vi Đẩu Số — iztro Skill

## Mô tả
Lập lá số Tử Vi Đẩu Số (紫微斗数) bằng thư viện iztro. Input: ngày sinh + giờ sinh + giới tính → Output: lá số 12 cung đầy đủ sao, tứ hóa, đại hạn, lưu niên.

## Trigger Keywords
`tử vi`, `紫微`, `lá số`, `mệnh cung`, `đại hạn`, `lưu niên`, `12 cung`, `thiên cơ`, `thái dương`, `tham lang`, `tử vi đẩu số`, `ziwei`, `iztro`, `bài tử vi`, `xem tử vi`, `lập lá số`, `purple star astrology`

## Cách dùng

### Lập lá số theo dương lịch
```js
const { astro } = require('/root/.openclaw/workspace/skills/iztro/lib');
// astro.bySolar(ngaySinh, gioSinh, gioiTinh, isLeap, ngonNgu)
const result = astro.bySolar('1986-05-15', 2, '男', true, 'vi-VN');
```

### Lập lá số theo âm lịch
```js
const result = astro.byLunar('1986-04-07', 2, '女', false, 'vi-VN');
```

### Giờ sinh (index 0-12)
| Index | Giờ | Chi |
|-------|-----|-----|
| 0 | 23:00-01:00 | Tý |
| 1 | 01:00-03:00 | Sửu |
| 2 | 03:00-05:00 | Dần |
| 3 | 05:00-07:00 | Mão |
| 4 | 07:00-09:00 | Thìn |
| 5 | 09:00-11:00 | Tỵ |
| 6 | 11:00-13:00 | Ngọ |
| 7 | 13:00-15:00 | Mùi |
| 8 | 15:00-17:00 | Thân |
| 9 | 17:00-19:00 | Dậu |
| 10 | 19:00-21:00 | Tuất |
| 11 | 21:00-23:00 | Hợi |

### Output chính
- `result.palaces` — 12 cung (Mệnh, Phụ Mẫu, Phúc Đức, Điền Trạch, Quan Lộc, Nô Bộc, Thiên Di, Tật Ách, Tài Bạch, Tử Nữ, Phu Thê, Huynh Đệ)
- `result.zodiac` — Con giáp
- `result.sign` — Cung hoàng đạo
- Mỗi palace có: `majorStars`, `minorStars`, `adjectiveStars`, `mutagen` (tứ hóa)

### Tính năng nâng cao
- Đại hạn, tiểu hạn, lưu niên, lưu nguyệt, lưu nhật, lưu thời
- Tứ hóa phi tinh
- Tam phương tứ chính
- Chain API: `result.palace('命宮').surroundedPalaces()`

## Kết hợp với các skill khác
- **Thiên Nhãn** (xem tướng mặt) + **Tử Vi** = phân tích toàn diện
- **Chỉ tay/chân** + **Tử Vi** = cross-reference vận mệnh
- **ziwei app** (`skills/ziwei/`) = UI đẹp + AI giải mệnh + K-line 100 năm

## Dependencies
- Node.js (đã build sẵn trong `lib/`)
- Ngôn ngữ: vi-VN, zh-CN, zh-TW, en-US, ja-JP, ko-KR

## Source
- GitHub: https://github.com/SylarLong/iztro
- NPM: https://www.npmjs.com/package/iztro
- Docs: https://docs.iztro.com
