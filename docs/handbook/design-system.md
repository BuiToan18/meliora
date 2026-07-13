# Design Principle

Meliora Design System được xây dựng dựa trên 5 nguyên tắc.

## 1. Simple

Thiết kế đơn giản, rõ ràng.

## 2. Consistent

Toàn bộ UI phải thống nhất.

## 3. Reusable

Component phải tái sử dụng.

## 4. Accessible

Đảm bảo khả năng sử dụng cho mọi người.

## 5. Responsive

Hoạt động tốt trên nhiều kích thước màn hình.

=============================================

# Design Philosophy

## Core Value

Professional

Meliora được xây dựng với định hướng là một hệ thống quản lý chuyên nghiệp.

Mọi quyết định về màu sắc, typography, spacing và component đều phải phục vụ mục tiêu này.

---

## Design Principles

- Simple
- Consistent
- Reusable
- Accessible
- Responsive

================================================

# Design Tokens

Design Token là tập hợp các giá trị dùng chung cho toàn bộ dự án.

Meliora sử dụng Token thay vì hardcode nhằm:

- Đồng nhất giao diện.
- Dễ thay đổi.
- Dễ bảo trì.
- Tăng khả năng tái sử dụng.

Các nhóm Token:

- Color
- Typography
- Spacing
- Radius
- Shadow

## Semantic Token


Không đặt Token theo giá trị.

Đặt Token theo ý nghĩa.

```scss
Ví dụ:

$spacing-md

$button-height-md

$avatar-size-md

$icon-size-md

$radius-md
```

Không sử dụng một Token cho nhiều mục đích khác nhau dù có cùng giá trị.

============================================

# Color Palette

## Mục tiêu

Thiết lập bộ màu thống nhất cho toàn bộ dự án Meliora.

Color Palette giúp:

- Đồng nhất giao diện.
- Dễ mở rộng.
- Dễ bảo trì.
- Giảm việc hardcode màu.

---

# Design Philosophy

Meliora theo định hướng:

> Professional + Modern

Màu sắc phải tạo cảm giác:

- Tin cậy
- Chuyên nghiệp
- Dễ nhìn
- Không gây mỏi mắt khi sử dụng lâu

---

# Primary Color

Primary Color đại diện cho thương hiệu Meliora.

```scss
$color-primary: #059669;
```

Emerald được lựa chọn vì:

- Khác biệt so với các Dashboard truyền thống sử dụng Blue.
- Mang ý nghĩa:
  - Growth
  - Stability
  - Trust
  - Professional

---

# Secondary Color

```scss
$color-secondary: #64748B;
```

Dùng cho:

- Text phụ
- Border
- Icon phụ
- Background nhẹ

---

# Semantic Colors

## Success

```scss
$color-success: #16A34A;
```

## Danger

```scss
$color-danger: #DC2626;
```

## Warning

```scss
$color-warning: #D97706;
```

## Info

```scss
$color-info: #0284C7;
```

---

# Neutral Colors

```scss
$gray-50
$gray-100
$gray-200
$gray-300
$gray-400
$gray-500
$gray-600
$gray-700
$gray-800
$gray-900
```

Neutral Colors sẽ chiếm khoảng **80–90% giao diện**.

Primary Color chỉ nên dùng làm điểm nhấn.

---

# Quy tắc

✔ Không hardcode màu.

✔ Luôn sử dụng Color Token.

✔ Primary chỉ dùng cho:

- Primary Button
- Active Menu
- Focus State
- Link
- Loading

Không sử dụng Primary cho toàn bộ giao diện.

======================================================

# Spacing System

## Mục tiêu

Thiết lập khoảng cách thống nhất cho toàn bộ dự án Meliora.

Spacing giúp:

- Giao diện cân đối.
- Đồng nhất.
- Dễ bảo trì.
- Không xuất hiện khoảng cách ngẫu nhiên.

---

# Base Grid

Meliora sử dụng:

> 4px Base Grid

Base Unit:

```text
4px
```

Từ Base Unit sẽ sinh ra toàn bộ Spacing Scale.

---

# Spacing Scale

```scss
$spacing-1: 4px;
$spacing-2: 8px;
$spacing-3: 12px;
$spacing-4: 16px;
$spacing-5: 20px;
$spacing-6: 24px;
$spacing-7: 28px;
$spacing-8: 32px;
$spacing-10: 40px;
$spacing-12: 48px;
$spacing-16: 64px;
```

---

# Vì sao chọn 4px Base Grid?

4px Base Grid linh hoạt hơn 8px Grid.

Nó vẫn hỗ trợ:

- 8px
- 16px
- 24px
- 32px

đồng thời cho phép sử dụng:

- 4px
- 12px
- 20px
- 28px

để tạo giao diện cân đối hơn.

Đây là cách nhiều Design System hiện đại sử dụng.

Ví dụ:

- Tailwind CSS
- Shopify Polaris
- Radix UI
- shadcn/ui

---

# Quy tắc

Chỉ sử dụng Spacing Token.

Không viết:

```scss
padding: 13px;
margin: 21px;
gap: 19px;
```

---

# Semantic Token

Spacing Token chỉ dùng cho **Spacing**.

Ví dụ:

```scss
padding: $spacing-4;
margin: $spacing-6;
gap: $spacing-3;
```

Không sử dụng Spacing Token cho:

- Height
- Width
- Icon Size
- Avatar Size

Ví dụ:

❌

```scss
height: $spacing-4;
```

Nên sử dụng Token riêng:

```scss
$button-height-md
$avatar-size-md
$icon-size-md
```

Mặc dù có thể cùng giá trị 16px, nhưng chúng mang ý nghĩa khác nhau.

---

# Quy tắc cuối cùng

Không đặt Token theo giá trị.

❌

```scss
$value16
```

✔

```scss
$spacing-4
$button-height-md
$icon-size-md
```

Token luôn được đặt theo **ý nghĩa**, không phải theo giá trị.

==============================================

# Typography System

## Font Family

Meliora sử dụng:

```scss
$font-family-base: "Inter", sans-serif;
```

Lý do:

- Hiện đại.
- Dễ đọc.
- Phù hợp Dashboard.
- Phổ biến trong các sản phẩm công nghệ.

---

## Font Size

| Token | Size |
|------|------:|
| xs | 12px |
| sm | 14px |
| md | 16px |
| lg | 18px |
| xl | 20px |
| 2xl | 24px |
| 3xl | 30px |
| 4xl | 36px |

---

## Font Weight

400

500

600

700

---

## Line Height

1.2

1.5

1.75

---

## Quy tắc

Không hardcode:

```scss
font-size:17px;
```

Luôn sử dụng Typography Token.

=================================================

# Typography System

## Font Family

Inter

## Font Scale

Display

H1

H2

H3

H4

H5

H6

Body

Caption

## Font Weight

400

500

600

700

## Line Height

1.2

1.5

1.75

## Typography Rule

- Không hardcode font-size.
- Không hardcode font-weight.
- Luôn sử dụng Typography Token.
- Typography phải thể hiện được thứ bậc thông tin (Hierarchy).

=========================================

# Border Radius System

## Radius Scale

none = 0px

sm = 4px

md = 8px

lg = 12px

full = 9999px

---

## Quy tắc

Không hardcode border-radius.

Luôn sử dụng Radius Token.

=========================================

# Shadow System

## Shadow Scale

sm

md

lg

---

## Quy tắc

Card

↓

Shadow MD

Modal

↓

Shadow LG

Button

↓

Không sử dụng Shadow mặc định.

===========================================

# SCSS Architecture

Meliora sử dụng kiến trúc SCSS theo từng tầng.

## abstracts

Chứa Design Tokens.

Không chứa CSS.

## base

Chứa Global Style.

## components

Chứa Shared Component Style.

## layout

Chứa Layout Style.

## pages

Chứa Page Style.

---

# Quy tắc

- Không hardcode Design Token.
- Không viết CSS trực tiếp trong styles.scss.
- Mỗi thư mục chỉ có một nhiệm vụ.