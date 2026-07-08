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

======================================================

## Pull Request

Pull Request không phải là Merge.
Pull Request là một yêu cầu xin phép Merge từ Feature Branch vào Main Branch.
Mục đích chính của Pull Request là: 
- Code review
- Discussion
- Quality control
- Approval
Merge chỉ diễn ra sau khi Pull Request được review và Approve.

======================================================

## Pull Request Best Practice

- Một Pull Request chỉ nên chứa một Task.
- Một Pull Request chỉ nên giải quyết một vấn đề.
- Pull Request càng nhỏ thì Review càng nhanh.
- Không trộn nhiều chức năng vào cùng một Pull Request.

Rule: 
1 Branch = 1 TASK
1 Pull Request = 1 TASK
1 Pull Request = 1 Story

=======================================================

## Pull Request Description

Pull Request không chỉ chứa code.

Pull Request cần có Description.

Description giúp:

- Reviewer hiểu mục đích của PR.

- QA biết cần kiểm thử gì.

- Leader dễ Review.

- Dễ tra cứu sau này.

Template của Team Meliora:

## Task

## Summary

## Testing

## Screenshot (nếu có UI)

=====================================================

## Commit Message

Commit Message không được viết cho bản thân hiện tại.

Commit Message được viết cho:

- Developer trong tương lai.

- Tech Lead.

- QA.

- Product Owner.

- Toàn sau 6 tháng nữa.

Một Commit tốt giúp Git History trở thành tài liệu của dự án.

Không dùng:

- fix
- done
- update
- test

Nên dùng:

feat(button): create reusable button component

fix(auth): handle token expiration

refactor(layout): simplify sidebar structure

======================================================

## Review Comment Workflow

Khi Tech Lead comment:

1. Sửa code.
2. Commit.
3. Push.
4. Reply vào comment.
5. Chờ review tiếp.

Không cần tạo Pull Request mới.

Pull Request luôn theo dõi Branch hiện tại.

=====================================================

## Reply Review Comment

Không nên:

Done all.

Nên:

- Reply đúng vào từng comment.
- Mô tả ngắn gọn điều đã sửa.
- Nếu chưa hiểu comment, hỏi lại ngay trong thread đó.

Ví dụ:

Done.
Renamed variable.

Updated.
Using design token now.

Could you explain this comment in more detail?

=======================================================

# Pull Request Workflow

## Quy trình

```text
Task
↓
Feature Branch
↓
Code
↓
Commit
↓
Push
↓
Create Pull Request
↓
Review
↓
Fix
↓
Push
↓
Approve
↓
Merge
↓
Delete Branch
↓
Pull Main
```

## Review Status

- Comment
- Request Changes
- Approve

## Sau khi Merge

- Delete Feature Branch.
- Checkout về main.
- Pull code mới nhất.
- Bắt đầu Task tiếp theo.

## Best Practice

- 1 Branch = 1 Task.
- 1 Pull Request = 1 Task.
- Viết Title và Description rõ ràng.
- Reply từng Review Comment.
- Không mở Pull Request mới khi chỉ sửa comment.
- Chỉ Merge sau khi được Approve.

====================================================

## Update Pull Request

Nếu Pull Request chưa Merge.

Phát hiện Bug.

Không cần tạo Pull Request mới.

Thực hiện.

- Fix.

- Commit.

- Push.

Pull Request sẽ tự động cập nhật.

Lưu ý.

Một số công ty sẽ yêu cầu Review lại nếu Pull Request có Commit mới sau khi đã được Approve.