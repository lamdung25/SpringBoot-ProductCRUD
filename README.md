# Spring Boot Product CRUD API

## 1. Giới thiệu dự án

Dự án bài tập thực tập xây dựng RESTful API quản lý sản phẩm bằng Java Spring Boot, kết nối cơ sở dữ liệu PostgreSQL.

Hệ thống hỗ trợ các chức năng CRUD: thêm, xem, cập nhật và xóa sản phẩm.

## 2. Công nghệ sử dụng

- Java 21
- Spring Boot 4.0.9
- Spring Data JPA / Hibernate
- PostgreSQL 17
- Maven
- IntelliJ IDEA
- HTTP Client để kiểm thử API

## 3. Cấu trúc dữ liệu

Bảng `products` gồm các trường:

| Trường | Kiểu dữ liệu | Mô tả |
|---|---|---|
| id | Long | Mã sản phẩm, tự tăng |
| name | String | Tên sản phẩm |
| price | Double | Giá sản phẩm |
| description | String | Mô tả sản phẩm |

## 4. Danh sách RESTful API

| Method | Endpoint | Chức năng |
|---|---|---|
| GET | `/api/products` | Lấy danh sách sản phẩm |
| GET | `/api/products/{id}` | Lấy sản phẩm theo ID |
| POST | `/api/products` | Thêm sản phẩm |
| PUT | `/api/products/{id}` | Cập nhật sản phẩm |
| DELETE | `/api/products/{id}` | Xóa sản phẩm |

## 5. Hướng dẫn chạy dự án

**Bước 1:** Cài đặt Java 21 và PostgreSQL.

**Bước 2:** Tạo database có tên `productcrud_db`.

**Bước 3:** Cấu hình kết nối trong `src/main/resources/application.properties`:

```properties
spring.datasource.url=jdbc:postgresql://localhost:5432/productcrud_db
spring.datasource.username=postgres
spring.datasource.password=${DB_PASSWORD}
spring.jpa.hibernate.ddl-auto=update
```

Thiết lập biến môi trường `DB_PASSWORD` bằng mật khẩu PostgreSQL trên máy chạy ứng dụng.

**Bước 4:** Mở dự án bằng IntelliJ IDEA và chạy `ProductcrudApplication.java`.

**Bước 5:** Truy cập API tại:

`http://localhost:8080/api/products`

## 6. Kiểm thử API

Dự án có file `api-test.http` để kiểm thử các API trực tiếp trong IntelliJ IDEA.

Các chức năng đã được kiểm thử thành công:

- GET: HTTP 200 OK
- POST: HTTP 201 Created
- PUT: HTTP 200 OK
- DELETE: HTTP 204 No Content

## 7. Kết quả đạt được

- Xây dựng thành công RESTful API CRUD cho bảng sản phẩm.
- Kết nối Spring Boot với PostgreSQL.
- Sử dụng Spring Data JPA để thao tác dữ liệu.
- Kiểm thử thành công các chức năng thêm, xem, sửa và xóa sản phẩm.

## 8. Thông tin bài tập

**Loại bài:** Bài tập cá nhân thực tập

**Nội dung:** Xây dựng RESTful CRUD API với Spring Boot và PostgreSQL.
