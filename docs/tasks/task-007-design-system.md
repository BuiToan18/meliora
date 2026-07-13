# TASK-007 — Design System Foundation

## Mục tiêu

Xây dựng nền tảng Design System cho Meliora nhằm đảm bảo toàn bộ giao diện của dự án được thống nhất, dễ bảo trì và có khả năng mở rộng cho cả Admin Portal và User Portal trong tương lai.

====================================

## Nội dung thực hiện

### 1. Design Principle

- Xây dựng tư duy thiết kế thống nhất
- Quy định cách sử dụng Design Token
- Thiết lập quy tắc Visual Hierarchy
- Định hướng khả năng mở rộng của Design System

====================================

### 2. Design Tokens

Xây dựng hệ thống token dùng chung.

Bao gồm:

- Color Token
- Spacing Token
- Typography Token
- Radius Token
- Shadow Token
- Breakpoint Token

====================================

### 3. Color System

Thiết kế bảng màu.

Bao gồm:

- Brand Color
- Semantic Color
- Neutral Color
- Background Color
- Text Color

====================================

### 4. Spacing System

Xây dựng hệ thống khoảng cách.

Ví dụ:

- 4px
- 8px
- 12px
- 16px
- 20px
- 24px
- 32px
- 48px
- 64px

====================================

### 5. Typography System

Thiết kế hệ thống Typography.

Bao gồm:

- Font Family
- Font Scale
- Font Weight
- Line Height
- Typography Hierarchy

====================================

### 6. Border Radius

Quy định Border Radius.

Bao gồm:

- none
- sm
- md
- lg
- full

====================================

### 7. Shadow System

Thiết lập Shadow Token.

Bao gồm:

- Shadow Small
- Shadow Medium
- Shadow Large

====================================

### 8. Responsive Breakpoint

Thiết lập Breakpoint.

Bao gồm:

- sm
- md
- lg
- xl

====================================

### 9. SCSS Architecture

Thiết kế cấu trúc thư mục Style.

```text
styles/

abstracts/
base/
components/
layout/
pages/

styles.scss
```

====================================

### 10. Global Style

Thiết lập Global Style.

Bao gồm:

- Reset CSS
- Body Style
- Global Typography
- Utility Rule

====================================

### 11. Documentation

Cập nhật Handbook.

Bao gồm:

- Design Principle
- Token Guideline
- Typography Guideline
- Color Guideline
- SCSS Architecture
- Best Practices

====================================

## Deliverables

Hoàn thành:

- Design Token
- Color Palette
- Typography System
- Spacing System
- Radius System
- Shadow System
- Breakpoint System
- SCSS Architecture
- Global Style
- Handbook Documentation

====================================

## Kết quả mong đợi

- Có một Design System hoàn chỉnh.
- Không hardcode giá trị CSS.
- Toàn bộ Component sử dụng Design Token.
- Có thể tái sử dụng cho Admin Portal và User Portal.

====================================

## Status
Done