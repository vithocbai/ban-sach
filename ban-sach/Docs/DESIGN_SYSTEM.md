# BOOK STORE — DESIGN SYSTEM

## 1. Design Direction

* Light theme
* Modern
* Minimal
* Clean
* Friendly
* Responsive
* Mobile-first

---

## 2. Colors

### Primary

```text
blue-600
blue-700
blue-50
```

### Accent

```text
amber-500
amber-600
amber-50
```

### Background

```text
stone-50
```

### Surface

```text
white
```

### Text

```text
stone-900
stone-600
stone-500
stone-400
```

### Status

```text
Success: green
Warning: amber
Error: red
Info: blue
```

---

## 3. Typography

### Font

```text
Inter
```

### Scale

```text
H1: text-4xl / text-5xl
H2: text-2xl / text-3xl
H3: text-xl
Body: text-base
Small: text-sm
Caption: text-xs
```

### Rules

* Heading: `font-sembold`
* Subheading: `font-semibold`
* Body: `font-normal`
* Button: `font-semibold`
* Line height ưu tiên `leading-relaxed` hoặc `leading-7`

---

## 4. Layout

### Container

```text
max-w-7xl
mx-auto
px-4
sm:px-6
lg:px-8
```

### Section

```text
py-16
lg:py-20
```

### Spacing

Ưu tiên spacing của Tailwind:

```text
gap-4
gap-5
gap-6
gap-8
```

---

## 5. Border Radius

```text
Button: rounded-xl
Input: rounded-xl
Card: rounded-2xl
Modal: rounded-2xl
Image: rounded-xl
Badge: rounded-full
```

---

## 6. Shadow

```text
Card: shadow-sm
Hover: shadow-md
Modal: shadow-xl
```

Không sử dụng shadow quá mạnh cho UI thông thường.

---

## 7. Buttons

### Primary

```text
bg-blue-600
text-white
hover:bg-blue-700
rounded-xl
```

### Secondary

```text
bg-white
border
border-stone-300
text-stone-700
hover:bg-stone-50
rounded-xl
```

### Danger

```text
bg-red-600
text-white
hover:bg-red-700
rounded-xl
```

### Ghost

```text
text-stone-600
hover:bg-stone-100
rounded-xl
```

---

## 8. Inputs

```text
w-full
rounded-xl
border
border-stone-200
bg-white
px-4
py-3
```

Focus:

```text
border-blue-500
ring-2
ring-blue-100
```

Error:

```text
border-red-500
ring-red-100
```

---

## 9. Cards

Default:

```text
bg-white
border
border-stone-200
rounded-2xl
shadow-sm
```

Hover:

```text
hover:shadow-md
hover:-translate-y-1
transition
```

---

## 10. Navbar

### Desktop

* Sticky top
* White background
* Bottom border
* Logo bên trái
* Navigation ở giữa
* Search / Cart / User bên phải

### Mobile

* Logo
* Cart
* Menu button
* Navigation dạng mobile menu

---

## 11. Hero

* Background `blue-50`
* Heading lớn
* Text ngắn
* Primary CTA
* Hình sách
* Không dùng gradient mạnh

---

## 12. Book Card

Hiển thị:

* Book image
* Category
* Title
* Author
* Rating
* Price
* Sale price nếu có
* Add to cart

Image:

```text
aspect-[3/4]
object-cover
rounded-xl
```

Grid:

```text
grid-cols-2
md:grid-cols-3
lg:grid-cols-4
```

---

## 13. Product Detail

Desktop:

```text
2 columns
Image
Product information
```

Mobile:

```text
1 column
```

Thông tin:

* Image
* Category
* Title
* Author
* Rating
* Price
* Description
* Stock
* Quantity
* Add to cart

---

## 14. Forms

Form layout:

```text
Label
Input
Error
```

Spacing:

```text
space-y-4
```

Primary action:

```text
w-full
sm:w-auto
```

---

## 15. Cart

Desktop:

```text
Product list + Order summary
```

Mobile:

```text
Product cards
Order summary
```

Hiển thị:

* Product
* Price
* Quantity
* Subtotal
* Remove
* Total

---

## 16. Checkout

Desktop:

```text
Shipping information + Order summary
```

Mobile:

```text
1 column
```

Fields:

* Full name
* Phone
* Address
* Note
* Payment method

---

## 17. Order Status

```text
PENDING    → amber
CONFIRMED  → blue
SHIPPING   → indigo
COMPLETED  → green
CANCELLED  → red
```

Badge:

```text
rounded-full
px-3
py-1
text-xs
font-semibold
```

---

## 18. Admin

Admin dùng chung design system với storefront.

### Layout

```text
Sidebar + Content
```

### Sidebar

* Dashboard
* Books
* Categories
* Orders
* Users

Active:

```text
bg-blue-50
text-blue-700
```

Normal:

```text
text-stone-600
hover:bg-stone-50
```

---

## 19. States

Mọi component interactive cần có:

```text
Default
Hover
Focus
Active
Disabled
Loading
Error
Empty
```

---

## 20. Loading

Dùng:

```text
spinner
skeleton
```

Không dùng loading animation phức tạp.

---

## 21. Empty State

Dùng cho:

* Empty cart
* No books
* No orders
* No search results

Bao gồm:

```text
Icon
Title
Description
Optional CTA
```

---

## 22. Toast

Dùng cho:

* Add to cart
* Remove from cart
* Login success
* Order success
* CRUD success
* Error

---

## 23. Modal

```text
fixed
inset-0
bg-stone-900/40
```

Content:

```text
bg-white
rounded-2xl
shadow-xl
```

---

## 24. Responsive

### Mobile

```text
< 640px
```

* 2-column book grid
* Mobile navigation
* Full-width buttons
* 1-column forms

### Tablet

```text
640px - 1024px
```

### Desktop

```text
>= 1024px
```

* Full navigation
* 4-column book grid
* Multi-column layouts
* Admin sidebar

---

## 25. Animation

Chỉ dùng animation nhẹ:

```text
transition
duration-200
duration-300
hover:-translate-y-1
hover:shadow-md
group-hover:scale-105
```

Không lạm dụng animation.

---

## 26. Icons

Dùng:

```text
Lucide React
```

Style:

```text
stroke-width: 2
```

Icon không dùng để thay thế text ở các action quan trọng.

---

## 27. Accessibility

* Button phải có text hoặc `aria-label`
* Input phải có label
* Image phải có `alt`
* Focus state phải rõ ràng
* Contrast đủ đọc
* Không chỉ dùng màu để biểu thị trạng thái
* Keyboard navigation phải hoạt động

---

## 28. UI Rules

* Không dùng quá nhiều màu
* Không dùng gradient mạnh
* Không dùng shadow nặng
* Không dùng border dày
* Không nhồi quá nhiều thông tin
* Ưu tiên khoảng trắng
* Giữ spacing nhất quán
* Giữ border-radius nhất quán
* Mobile-first
* Component phải tái sử dụng được

---

## 29. Core UI Tokens

```text
Primary:    blue-600
Accent:     amber-500
Background: stone-50
Surface:    white
Text:       stone-900
Muted:      stone-500
Border:     stone-200

Radius:
xl / 2xl

Shadow:
sm / md

Font:
Inter
```

---

## 30. Visual Goal

Website phải có cảm giác:

```text
Clean
Modern
Light
Trustworthy
Friendly
Easy to use
```
