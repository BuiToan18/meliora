# Vì sao không code trực tiếp trên main? 

- Main luôn phải ổn định.
- Main phải luôn deploy được.
- Main chỉ chứa code đẫ review.
- Main chỉ chứa code đã test.
- Main không chứa code đang phát triển.

Main còn được gọi là một cành cây được bảo vệ: 
- Không được push trực tiếp.
- Không được force push.
- Chỉ được merge qua Pull Request.

=> Main không phải nơi để phát triển. Main là nơi để phát hành (release)

=============================================

# Quy trình nhánh tính năng

## Vì sao phải tạo Feature Branch? 

Không làm việc trực tiếp trên main.
Mỗi tính năng sẽ có một branch riêng.

VD: 
main
feature/task-006-button-component

================================================

### Lợi ích: 
- Main luôn ổn định.
- Dễ review.
- Dễ test.
- Không ảnh hưởng Developer khắc.
- Dễ Rollback

=================================================

## Quy trình chuẩn 
Khi leader giao Task. Luôn làm theo trình tự

Nhận Task -> Pull latest code -> Create Feature Branch -> Push Branch -> Code -> Commit -> Push -> Create Pull Request -> Code Review -> Merge

=================================================

## Pull trước khi tạo Branch

Luôn chạy : git pull origin main

Mục đích: Đảm bảm branch mới luôn được tạo từ code mới nhất.

==================================================

## Tạo Feature Branch

git checkout -b feature/task-006-button-component

===================================================

## Kiểm tra branch

git branch

VD: 
* feature/task-006-button-component
main

===================================================

## Đẩy nhánh 

Lần đầu cần: 
git push -u origin feature/task-006-button-component

Sau đó thì chỉ cần: 
git push

====================================================

## Theo dõi nhánh

git push -u

Không chỉ push, nó còn tạo liên két Local Branch -> Remote Branch. Cho nên lần sau chỉ cần git push

====================================================

## Quy ước đặt tên

Tính năng: 
feature/task-006-button-component

Sửa lỗi: 
bugfix/task-010-login-api

Bản vá lỗi:
hotfix/login-api

====================================================

## Một Branch chỉ làm một việc
Ví dụ: feature/task-006-button-component

Branch này chỉ chứa
- Cái nút (Button).

Không chứa:
- Đăng nhập.
- Thanh điều hướng.
- Sửa lỗi API.
Một Branch chỉ nên kể một câu chuyện.

=====================================================

## Không code trên Main

Main là nơi: 
- Triển khai.
- Giải phóng.
- Ổn định.
Main không phải là nơi để phát triển, Main là nơi để phát hành (release)

======================================================
# Những bài học kinh nghiệm 
- Luôn Pull trước khi tạo Branch.
- Mỗi Task tạo một Branch riêng.
- Không code trực tiếp trên Main.
- Branch phải đặt tên theo Convention.
- Một Branch chỉ chứa một chức năng.
- Luôn Push Branch lên GitHub trước khi bắt đầu làm việc.