# Task-005: Git Workflow 

## Epic
Epic-01: Project Initialization

-----------------------------

## Mục tiêu: 
Hiểu quy trình làm việc với Git trong một dự án thực tế và thống nhất Git Workflow của team

-----------------------------

## Business Context

Trong một dự án có nhiều Frontend Developer cùng làm việc, nếu mọi người đều làm trực tiếp trên branch 'main' sẽ rất dễ gây ra:

- Conflict
- Khó review code
- Khó xác định lỗi
- Khó rollback

=> Vì vậy cần xây dựng một Git Workflow thông nhất cho toàn bộ dự án.

-------------------------------

## Kiến thức cần học:

- Git Branch
- Git Workflow
- Feature Branch
- Bugfix Branch
- Pull Request (PR)
- Code Review
- Git Stash (Introduction)

------------------------------

## Convention

### Brach Naming

Feature

feature/task-009-button-component

Bug Fix

bugfix/task-021-login-error

Refactor

refactor/button-component

Documentation

docs/project-documentation

-------------------------------

### Git Workflow

Receive Task

↓

Create Branch

↓

Coding

↓

Commit

↓

Push

↓

Pull Request

↓

Code Review

↓

Merge

↓

Done

--------------------------------------

### Branch Rule

One Branch = One Purpose
Một branch chỉ thực hiện một nhiệu vụ.

Ví dụ: feature/tash-009-button-component
-> Chỉ chứa code của Button Component.
Không sửa Login, Header hoặc các chức năng khác trong cùng branch.

--------------------------------------

## Kiến thức học được:

- [ ] Hiểu Git Workflow
- [ ] Hiểu Feature Branch
- [ ] Hiểu Bugfix Branch
- [ ] Hiểu Pull Request
- [ ] Hiểu Code Review
- [ ] Biết Convention đặt tên Branch
- [ ] Hiểu nguyên tắc One Branch = One Purpose
- [ ] Biết khi nào sử dụng Git Stash

--------------------------------------

## Deliverables

- Hoàn thành tài liệu Git Workflow.
- Thống nhất Convention đặt tên Branch.
- Áp dụng Workflow cho toàn bộ dự án.

--------------------------------------

## Commit

docs: add git workflow documentation

--------------------------------------

## Bài học rút ra kinh nghiệm

- Git không chỉ là công cụ lưu code.
- Git Workflow giúp team làm việc hiệu quả.
- Không commit code chưa hoàn chỉnh nếu chưa cần thiết.
- Có thể sử dụng Git Stash khi cần chuyển sang xử lý công việc khẩn.

----------------------------------------

## Status

🟡 In Progress