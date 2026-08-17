# BOOK STORE — PROJECT PLAN

## 1. Tổng quan

Website bán sách online.

### Stack

* Frontend: ReactJS + Vite
* Styling: Tailwind CSS
* Backend: Django + Django REST Framework
* Database: PostgreSQL
* Authentication: JWT
* API: REST

---

## 2. Chức năng

### User

* Đăng ký
* Đăng nhập / đăng xuất
* Xem sách
* Tìm kiếm sách
* Lọc theo danh mục
* Xem chi tiết sách
* Thêm / xóa / cập nhật giỏ hàng
* Checkout
* Đặt hàng
* Xem lịch sử đơn hàng
* Xem thông tin cá nhân

### Admin

* Quản lý sách
* Quản lý danh mục
* Quản lý đơn hàng
* Quản lý người dùng
* Cập nhật trạng thái đơn hàng

---

## 3. Database

### User

Dùng Django User.

### Category

* id
* name
* slug
* description
* created_at

### Book

* id
* title
* slug
* author
* description
* price
* sale_price
* stock
* image
* category
* isbn
* publisher
* published_date
* is_active
* created_at
* updated_at

### Order

* id
* user
* full_name
* phone
* address
* note
* total_price
* status
* payment_method
* created_at
* updated_at

### OrderItem

* id
* order
* book
* quantity
* price
* subtotal

### Quan hệ

```text
User 1 ─── N Order
Category 1 ─── N Book
Order 1 ─── N OrderItem
Book 1 ─── N OrderItem
```

---

## 4. Backend Structure

```text
backend/
├── config/
├── accounts/
├── books/
├── orders/
├── manage.py
├── requirements.txt
└── .env
```

### Apps

* `accounts`: authentication
* `books`: books + categories
* `orders`: cart/order/checkout

---

## 5. Frontend Structure

```text
frontend/
├── src/
│   ├── components/
│   ├── pages/
│   ├── layouts/
│   ├── services/
│   ├── context/
│   ├── hooks/
│   ├── routes/
│   ├── App.jsx
│   └── main.jsx
├── package.json
└── .env
```

---

## 6. Frontend Pages

```text
/
├── Home
├── Books
├── BookDetail
├── Cart
├── Checkout
├── Login
├── Register
├── Profile
├── Orders
└── OrderDetail
```

### Admin

```text
/admin
├── Dashboard
├── Books
├── Categories
└── Orders
```

---

## 7. API

### Auth

```text
POST /api/auth/register/
POST /api/auth/login/
POST /api/auth/token/refresh/
```

### Books

```text
GET    /api/books/
GET    /api/books/:id/
POST   /api/books/
PUT    /api/books/:id/
DELETE /api/books/:id/
```

### Categories

```text
GET    /api/categories/
POST   /api/categories/
PUT    /api/categories/:id/
DELETE /api/categories/:id/
```

### Orders

```text
GET   /api/orders/
POST  /api/orders/
GET   /api/orders/:id/
PATCH /api/orders/:id/status/
GET   /api/orders/my-orders/
```

---

## 8. Authentication

JWT.

Frontend:

* Lưu access token
* Refresh token
* Axios interceptor
* Protected routes

Backend:

* JWT authentication
* User permission
* Admin permission

---

## 9. Cart

Cart được quản lý bằng React Context.

MVP:

* Add item
* Remove item
* Update quantity
* Calculate total
* Lưu LocalStorage
* Clear cart sau khi đặt hàng

---

## 10. Order

Payment MVP:

```text
COD
```

Order status:

```text
PENDING
CONFIRMED
SHIPPING
COMPLETED
CANCELLED
```

Backend phải kiểm tra stock trước khi tạo order.

---

## 11. Design Theme

### Style

* Light
* Modern
* Minimal
* Responsive
* Mobile-first

### Colors

```text
Primary: blue
Accent: amber
Background: stone-50
Surface: white
Text: stone-900
Muted: stone-500
```

### UI

* Rounded-xl / rounded-2xl
* Border nhẹ
* Shadow nhẹ
* Nhiều khoảng trắng
* Typography rõ ràng

---

## 12. Packages

### Backend

```text
Django
djangorestframework
djangorestframework-simplejwt
django-cors-headers
psycopg2-binary
Pillow
python-dotenv
```

### Frontend

```text
react-router-dom
axios
lucide-react
react-hook-form
```

---

## 13. Environment

### Backend

```env
DEBUG=True
SECRET_KEY=
DATABASE_NAME=
DATABASE_USER=
DATABASE_PASSWORD=
DATABASE_HOST=
DATABASE_PORT=
```

### Frontend

```env
VITE_API_URL=
```

---

## 14. Development Order

### Phase 1

* Setup React
* Setup Tailwind
* Setup Django
* Setup PostgreSQL
* Setup environment

### Phase 2

* Database models
* Django Admin
* JWT authentication
* API

### Phase 3

* Homepage
* Book list
* Book detail
* Search
* Filter

### Phase 4

* Cart
* Checkout
* Order
* Order history

### Phase 5

* Admin dashboard
* Book CRUD
* Category CRUD
* Order management

### Phase 6

* Testing
* Responsive
* Security
* Deployment

---

## 15. MVP Scope

### Có

* Authentication
* Books
* Categories
* Search
* Filter
* Cart
* Checkout
* Orders
* Admin

### Chưa có

* Online payment
* Voucher
* Wishlist
* Review
* Chat
* Recommendation
* Notification
* Redis
* WebSocket

---

## 16. Project Structure

```text
book-store/
├── frontend/
├── backend/
├── README.md
├── PROJECT_PLAN.md
└── .gitignore
```

---

## 17. MVP Done

Project hoàn thành khi:

* User có thể đăng ký / đăng nhập
* User có thể xem và tìm sách
* User có thể thêm sách vào giỏ
* User có thể đặt hàng
* User có thể xem đơn hàng
* Admin có thể CRUD sách
* Admin có thể CRUD danh mục
* Admin có thể quản lý đơn hàng
* Database hoạt động với PostgreSQL
* Frontend kết nối được Backend API
* Responsive trên mobile và desktop
