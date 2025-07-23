# 📘 Product Requirement Document (PRD)

## 🛍️ Project Name

Blossom Shop - Online Store for Books, Bookmarks, and Tumblers

---

## 📌 Overview

Blossom Shop is an e-commerce platform focused on delivering a smooth and intuitive shopping experience for customers looking for books, bookmarks, and tumblers. The website will feature user-friendly navigation, secure user authentication, product browsing, shopping cart functionality, real-time payment integration, and an admin dashboard for managing products and orders.

---

## 🎯 Goals

- Provide an intuitive shopping platform for physical products.
- Implement secure user registration and authentication (JWT).
- Allow customers to browse, search, and filter products.
- Enable seamless checkout and payment process.
- Provide order tracking for users and management for admins.
- Deploy the platform using CI/CD pipelines and cloud infrastructure.

---

## 🖥️ Tech Stack

| 계층           | 기술 스택                                               |
| -------------- | ------------------------------------------------------- |
| **Frontend**   | Vue.js, Vue Router, Pinia, Tailwind CSS, Axios          |
| **Backend**    | Spring Boot, Spring Security, JPA (Hibernate), JWT 인증 |
| **Database**   | MySQL                                                   |
| **Payment**    | Stripe (or Toss Payments) API integration               |
| **Deployment** | Docker, GitHub Actions, AWS (EC2, S3 등)                |

---

## 👤 User Types

### 🧑‍💻 General Users

- Register / Login
- Browse products by category
- Add to cart
- Checkout and pay
- View order history

### 🛠️ Admin

- Secure admin login
- Add/Edit/Delete products
- Manage categories
- View/manage orders

---

## 📦 Features

### 1. User Features

- [ ] JWT-based signup & login
- [ ] Browse & filter products by category
- [ ] Product detail view
- [ ] Cart: add, update, remove items
- [ ] Checkout with real-time payment
- [ ] View order history

### 2. Admin Features

- [ ] Admin login
- [ ] CRUD for products
- [ ] Manage product categories
- [ ] View and update order status

### 3. Payment System

- [ ] Integrate Stripe Payments API
- [ ] Secure checkout page with order summary
- [ ] Handle payment success/failure callbacks
- [ ] Store transaction info in DB
- [ ] Send order confirmation email (future)

### 4. UI/UX

- [ ] Responsive and mobile-first design
- [ ] Clean product browsing experience
- [ ] Clear checkout and payment flow
- [ ] Error handling and loading states

---

## 🔐 Authentication & Security

- JWT-based stateless authentication
- Role-based access (USER, ADMIN)
- Secure payment tokenization via payment API
- Backend validation for all transactions

---

## 📡 API Design (RESTful)

Example endpoints:

- `POST /api/auth/signup`
- `POST /api/auth/login`
- `GET /api/products`
- `GET /api/products/{id}`
- `POST /api/cart`
- `POST /api/orders`
- `POST /api/payments/checkout`
- `POST /api/payments/webhook`
- Admin:
  - `POST /api/admin/products`
  - `PUT /api/admin/products/{id}`
  - `DELETE /api/admin/products/{id}`
  - `GET /api/admin/orders`

---

## 🧪 Testing & QA

- Backend: JUnit + MockMVC for controllers/services
- Frontend: Unit tests for components (Vitest/Pinia Testing)
- Integration: Postman + Stripe Test API keys
- Manual testing of full purchase flow

---

## 🚀 Deployment Plan

- Dockerize frontend & backend separately
- Use GitHub Actions to automate builds
- AWS EC2 for app hosting
- AWS S3 for product image storage
- Stripe Dashboard or Toss Admin for payments
- HTTPS with SSL (e.g., Let's Encrypt)

---

## ✅ MVP Scope

✅ User auth + role  
✅ Product catalog + cart  
✅ Admin product & category CRUD  
✅ Checkout and payment  
✅ Basic order tracking

---

## 🧭 Future Enhancements

- Email notifications for orders
- Product reviews and ratings
- Wishlist/favorite feature
- Internationalization (i18n)
- Inventory management alerts
