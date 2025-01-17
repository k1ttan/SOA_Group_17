Cấu hình cơ sở dữ liệu tại file application.properties:  
spring.datasource.url=jdbc:mysql://localhost:3306/ecommerce_db #Tạo 1 db trống như tên  
spring.datasource.driver-class-name=com.mysql.cj.jdbc.Driver #Cấu hình driver kết nối db  
spring.datasource.username=root #Username của db  
spring.datasource.password= #Password  

Sau đó chạy Terminal project với lệnh: 
```
mvn clean install
```

Cấu hình chạy project SpringBoot với tool có sẵn trên IDE với tomcat server  
Project sẽ chạy trên url: http://localhost:8080/

Thực hiện lệnh sql để có dữ liệu trong db:
```
INSERT INTO `cart` (`id`, `quantity`, `product_id`, `user_id`) VALUES (1, 1, 1, 1);
INSERT INTO `cart` (`id`, `quantity`, `product_id`, `user_id`) VALUES (2, 2, 2, 3);
INSERT INTO `cart` (`id`, `quantity`, `product_id`, `user_id`) VALUES (3, 1, 12, 3);
INSERT INTO `cart` (`id`, `quantity`, `product_id`, `user_id`) VALUES (4, 1, 13, 3);
INSERT INTO `category` (`id`, `image_name`, `is_active`, `name`) VALUES (2, '', b'1', 'Xi măng');
INSERT INTO `category` (`id`, `image_name`, `is_active`, `name`) VALUES (3, '', b'1', 'Gạch');
INSERT INTO `category` (`id`, `image_name`, `is_active`, `name`) VALUES (4, '', b'1', 'Thép');
INSERT INTO `category` (`id`, `image_name`, `is_active`, `name`) VALUES (5, '', b'1', 'Cát');
INSERT INTO `category` (`id`, `image_name`, `is_active`, `name`) VALUES (6, '', b'1', 'Sỏi');
INSERT INTO `order_address` (`id`, `address`, `city`, `email`, `first_name`, `last_name`, `mobile_no`, `pincode`, `state`) VALUES (1, 'abcd', 'b', 'kiettan1510@gmail.com', 'le', 'kiet', '0369258147', '1234', 'abcd');
INSERT INTO `order_address` (`id`, `address`, `city`, `email`, `first_name`, `last_name`, `mobile_no`, `pincode`, `state`) VALUES (2, 'abcd', 'b', 'kiettan@gmail.com', 'le', 'kiet', '0369258147', '1234', 'abcd');
INSERT INTO `order_address` (`id`, `address`, `city`, `email`, `first_name`, `last_name`, `mobile_no`, `pincode`, `state`) VALUES (3, 'abcd', 'b', 'kiettan@gmail.com', 'aaa', 'baaa', '0369258147', '1234', 'abcd');
INSERT INTO `order_address` (`id`, `address`, `city`, `email`, `first_name`, `last_name`, `mobile_no`, `pincode`, `state`) VALUES (4, 'abcd', 'b', 'kiettan@gmail.com', 'abcder', 'baaa', '0369258147', '1234', 'abcd');
INSERT INTO `order_address` (`id`, `address`, `city`, `email`, `first_name`, `last_name`, `mobile_no`, `pincode`, `state`) VALUES (5, 'abcd', 'b', 'kiettan@gmail.com', 'abcder', 'baaa', '0369258147', '1234', 'abcd');
INSERT INTO `order_address` (`id`, `address`, `city`, `email`, `first_name`, `last_name`, `mobile_no`, `pincode`, `state`) VALUES (6, 'abcd', 'b', 'kiettan@gmail.com', 'aaaaaaaa', 'baaa', '0369258147', '1234', 'abcd');
INSERT INTO `order_address` (`id`, `address`, `city`, `email`, `first_name`, `last_name`, `mobile_no`, `pincode`, `state`) VALUES (7, 'abcd', 'b', 'kiettan@gmail.com', 'aaaaaaaa', 'baaa', '0369258147', '1234', 'abcd');
INSERT INTO `order_address` (`id`, `address`, `city`, `email`, `first_name`, `last_name`, `mobile_no`, `pincode`, `state`) VALUES (8, 'abcd', 'b', 'kiettan@gmail.com', 'aaaaaaaa', 'baaa', '0369258147', '1234', 'abcd');
INSERT INTO `order_address` (`id`, `address`, `city`, `email`, `first_name`, `last_name`, `mobile_no`, `pincode`, `state`) VALUES (9, 'abcd', 'b', 'kiettan@gmail.com', 'aaaaaaaa', 'baaa', '0369258147', '1234', 'abcd');
INSERT INTO `product` (`id`, `category`, `description`, `discount`, `discount_price`, `image`, `is_active`, `price`, `stock`, `title`) VALUES (1, 'Xi măng', 'Xi măng Portland chất lượng cao', 0, 50000, 'ximang.jpg', b'1', 50000, 50, 'Xi măng Portland');
INSERT INTO `product` (`id`, `category`, `description`, `discount`, `discount_price`, `image`, `is_active`, `price`, `stock`, `title`) VALUES (2, 'Gạch', 'Gạch đất sét đỏ', 5, 85499.525, 'gach.jpg', b'1', 89999.5, 1000, 'Gạch đất sét');
INSERT INTO `product` (`id`, `category`, `description`, `discount`, `discount_price`, `image`, `is_active`, `price`, `stock`, `title`) VALUES (3, 'Thép', 'Thanh thép cốt bê tông', 15, 849.15, 'thep.jpg', b'1', 999, 200, 'Thép cốt bê tông');
INSERT INTO `product` (`id`, `category`, `description`, `discount`, `discount_price`, `image`, `is_active`, `price`, `stock`, `title`) VALUES (4, 'Cát', 'Cát sông mịn', 0, 10000, 'cat.jpg', b'1', 10000, 500, 'Cát sông');
INSERT INTO `product` (`id`, `category`, `description`, `discount`, `discount_price`, `image`, `is_active`, `price`, `stock`, `title`) VALUES (5, 'Sỏi', 'Đá sỏi nghiền', 0, 2500, 'soi.jpg', b'1', 2500, 300, 'Đá sỏi nghiền');
INSERT INTO `product` (`id`, `category`, `description`, `discount`, `discount_price`, `image`, `is_active`, `price`, `stock`, `title`) VALUES (6, 'Xi măng', 'Xi măng trắng dùng cho trang trí và công trình', 5, 55000, 'ximang_trang.jpg', b'1', 60000, 30, 'Xi măng trắng');
INSERT INTO `product` (`id`, `category`, `description`, `discount`, `discount_price`, `image`, `is_active`, `price`, `stock`, `title`) VALUES (7, 'Gạch', 'Gạch đất sét đỏ chất lượng tốt', 5, 4749.525, 'gach_dat_set.jpg', b'1', 4999.5, 1000, 'Gạch đất sét đỏ');
INSERT INTO `product` (`id`, `category`, `description`, `discount`, `discount_price`, `image`, `is_active`, `price`, `stock`, `title`) VALUES (8, 'Gạch', 'Gạch ceramic cao cấp cho nội thất', 8, 1380.184, 'gach_ceramic.jpg', b'1', 1500.2, 750, 'Gạch ceramic');
INSERT INTO `product` (`id`, `category`, `description`, `discount`, `discount_price`, `image`, `is_active`, `price`, `stock`, `title`) VALUES (9, 'Thép', 'Thanh thép hình chữ U', 15, 8500, 'thep_chu_u.jpg', b'1', 10000, 200, 'Thép hình chữ U');
INSERT INTO `product` (`id`, `category`, `description`, `discount`, `discount_price`, `image`, `is_active`, `price`, `stock`, `title`) VALUES (10, 'Thép', 'Thép tròn đặc dùng trong xây dựng', 12, 9679.12, 'thep_tron.jpg', b'1', 10999, 150, 'Thép tròn đặc');
INSERT INTO `product` (`id`, `category`, `description`, `discount`, `discount_price`, `image`, `is_active`, `price`, `stock`, `title`) VALUES (11, 'Cát', 'Cát xây dựng, chất lượng cao', 0, 100000, 'cat_xay_dung.jpg', b'1', 100000, 500, 'Cát xây dựng');
INSERT INTO `product` (`id`, `category`, `description`, `discount`, `discount_price`, `image`, `is_active`, `price`, `stock`, `title`) VALUES (12, 'Cát', 'Cát trắng dùng cho trang trí cảnh quan', 0, 200000, 'cat_trang.jpg', b'1', 200000, 300, 'Cát trắng');
INSERT INTO `product` (`id`, `category`, `description`, `discount`, `discount_price`, `image`, `is_active`, `price`, `stock`, `title`) VALUES (13, 'Sỏi', 'Sỏi tự nhiên dùng cho trang trí sân vườn', 0, 120000, 'soi_tu_nhien.jpg', b'1', 120000, 200, 'Sỏi tự nhiên');
INSERT INTO `product` (`id`, `category`, `description`, `discount`, `discount_price`, `image`, `is_active`, `price`, `stock`, `title`) VALUES (14, 'Sỏi', 'Sỏi màu trang trí cho hồ cá', 0, 121212, 'soi_mau.jpg', b'1', 121212, 150, 'Sỏi màu');
INSERT INTO `product_order` (`id`, `order_date`, `order_id`, `payment_type`, `price`, `quantity`, `status`, `order_address_id`, `product_id`, `user_id`) VALUES (3, '2025-01-14', 'bb8b5e16-28da-42c0-b893-bcbd4d8f1fea', 'COD', 85499.525, 1, 'Đang giao', 3, 2, 3);
INSERT INTO `product_order` (`id`, `order_date`, `order_id`, `payment_type`, `price`, `quantity`, `status`, `order_address_id`, `product_id`, `user_id`) VALUES (4, '2025-01-14', 'd87e8c63-1352-483c-b2e5-18fde2c829e0', 'ONLINE', 85499.525, 1, 'Đang giao', 4, 2, 3);
INSERT INTO `product_order` (`id`, `order_date`, `order_id`, `payment_type`, `price`, `quantity`, `status`, `order_address_id`, `product_id`, `user_id`) VALUES (5, '2025-01-14', '2cef295d-0fcc-424c-9f58-980d7a1cc43d', 'ONLINE', 200000, 1, 'Đang giao', 5, 12, 3);
INSERT INTO `product_order` (`id`, `order_date`, `order_id`, `payment_type`, `price`, `quantity`, `status`, `order_address_id`, `product_id`, `user_id`) VALUES (6, '2025-01-15', 'cddd96e1-72c4-435a-bb78-59692d75f60c', 'ONLINE', 85499.525, 1, 'Đang giao', 6, 2, 3);
INSERT INTO `product_order` (`id`, `order_date`, `order_id`, `payment_type`, `price`, `quantity`, `status`, `order_address_id`, `product_id`, `user_id`) VALUES (7, '2025-01-15', 'f08c398b-7588-4df1-aba3-823cbf00e13c', 'ONLINE', 200000, 1, 'Đang giao', 7, 12, 3);
INSERT INTO `product_order` (`id`, `order_date`, `order_id`, `payment_type`, `price`, `quantity`, `status`, `order_address_id`, `product_id`, `user_id`) VALUES (8, '2025-01-17', 'a0702d80-ec5f-44fc-b74a-3ab7bd8b8c13', 'COD', 85499.525, 2, 'In Progress', 8, 2, 3);
INSERT INTO `product_order` (`id`, `order_date`, `order_id`, `payment_type`, `price`, `quantity`, `status`, `order_address_id`, `product_id`, `user_id`) VALUES (9, '2025-01-17', '656bd0f5-57e2-4645-968f-b55503e8361c', 'COD', 85499.525, 2, 'In Progress', 9, 2, 3);
INSERT INTO `user_dtls` (`id`, `account_non_locked`, `address`, `city`, `email`, `failed_attempt`, `is_enable`, `lock_time`, `mobile_number`, `name`, `password`, `pincode`, `profile_image`, `reset_token`, `role`, `state`) VALUES (1, b'1', 'abcd', 'b', 'kiettan@gmail.com', 0, b'1', NULL, '0369258147', 'kiet', '$2a$10$.Njau2xWahN9S9Qft1DPOumsLwJiyRw9wmu0eU9aptytvrsQJKFOW', '1234', 'faker1.jpg', '53bfdfb0-e446-4f23-bee7-23b2e525ef4a', 'ROLE_ADMIN', 'abcd');
INSERT INTO `user_dtls` (`id`, `account_non_locked`, `address`, `city`, `email`, `failed_attempt`, `is_enable`, `lock_time`, `mobile_number`, `name`, `password`, `pincode`, `profile_image`, `reset_token`, `role`, `state`) VALUES (3, b'1', 'abcd', 'b', 'kiet@gmail.com', 0, b'1', NULL, '0369258147', 'kiett', '$2a$10$DttGdyVANSMriCSZpTZM.eyWSWNxxlqO2o6DZQByWNgu4.M8r9jwO', '1234', 'images.jpg', NULL, 'ROLE_USER', 'abcd');
```
