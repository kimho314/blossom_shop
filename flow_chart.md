# 고객 화면 흐름도

```mermaid
flowchart TD
    Home[🏠 홈]
    Products[🛍️ 상품 목록]
    ProductDetail[📄 상품 상세]
    Cart[🛒 장바구니]
    Checkout[💳 주문/결제]
    Login[🔐 로그인]
    Signup[🆕 회원가입]
    OrderComplete[✅ 주문 완료]
    MyPage[👤 마이페이지]
    OrderHistory[📦 주문 내역]
    Review[⭐ 리뷰 작성]
    EditProfile[✏️ 회원정보 변경]
    Address[📫 주소 관리]
    ResetPassword[🔑 비밀번호 재설정]

    Home --> Products
    Products --> ProductDetail
    ProductDetail --> Cart
    Cart --> Checkout
    Checkout --> Login
    Login --> Checkout
    Checkout --> OrderComplete
    OrderComplete --> MyPage

    Home --> Signup
    Login --> MyPage
    MyPage --> OrderHistory
    MyPage --> Review
    MyPage --> EditProfile
    MyPage --> Address

    Login --> ResetPassword
```

# 관리자 화면 흐름도

```mermaid
flowchart TD
    AdminLogin[🔐 관리자 로그인]
    Dashboard[📊 관리자 대시보드]
    ProductMgmt[🛠️ 상품 관리]
    AddProduct[➕ 상품 등록]
    EditProduct[✏️ 상품 수정/삭제]
    OrderMgmt[📦 주문 관리]
    UserMgmt[👥 회원 관리]
    ReviewMgmt[🗨️ 리뷰 관리]

    AdminLogin --> Dashboard
    Dashboard --> ProductMgmt
    ProductMgmt --> AddProduct
    ProductMgmt --> EditProduct
    Dashboard --> OrderMgmt
    Dashboard --> UserMgmt
    Dashboard --> ReviewMgmt
```
