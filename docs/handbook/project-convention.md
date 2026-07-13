# Folder Conventrion

## Nguyên tắc: 

- Một thư mục chỉ có một trách nhiệm.
- Ưu tiên Feature-first Architecture.
- Shared chứa các thành phần tái sử dụng.
- Core chứa các thành phần dùng một lần cho toàn hệ thống.
- Mỗi Feature độc lập và có thể mở rộng hoặc xóa mà ít ảnh hưởng đến Feature khác.

## Mục tiêu: 

- Dễ tìm file.
- Dễ mở rộng.
- Dễ bảo trì.
- Dễ onboarding thành viên mới.

## Core

Core chứa những thành phần chỉ tồn tại một lần trong toàn bộ ứng dụng.

Ví dụ:

- AuthService
- HTTP Interceptor
- Global Guard
- App Config
- Error Handler

Không đặt các Service nghiệp vụ (RoomService, UserService...) vào Core.

## Shared

Shared chứa các thành phần có thể tái sử dụng giữa nhiều Feature.

Ví dụ:

- Button
- Input
- Card
- Modal
- Avatar
- Badge
- Pipes
- Directives

Quy tắc:

Nếu xóa một Feature mà thành phần đó vẫn còn dùng được ở Feature khác, nó nên nằm trong Shared.

=============================================
# File Naming Convention

## Công thức

feature-name.type.extension

Ví dụ:

button.component.ts

auth.service.ts

auth.guard.ts

focus.directive.ts

currency.pipe.ts

login-request.interface.ts

button-size.enum.ts

## Quy tắc

- Tên file viết bằng lowercase.
- Dùng dấu "-" để nối từ.
- Thể hiện rõ loại file qua hậu tố.
- Tuân theo Angular Style Guide.

Quy tắc đặt tên

Loại            ||	Ví dụ
Component       ||	button.component.ts
Service         ||	auth.service.ts
Guard           ||	auth.guard.ts
Directive       ||	focus.directive.ts
Pipe            ||	currency.pipe.ts
Interface       ||	login-request.interface.ts
Enum            ||	button-size.enum.ts
Constant        ||	app.constant.ts
Model (Class)   ||	user.model.ts (nếu dùng class model)

==============================================================

# Angular Convention

- Một Component chỉ có một trách nhiệm.
- Không gọi HttpClient trực tiếp trong Component.
- Không viết logic phức tạp trong HTML.
- Tái sử dụng Component thay vì copy code.
- Tách Business Logic khỏi UI.
- Không hardcode dữ liệu.

===============================================================

# Variable Convention

Variable
→ camelCase

Boolean
→ is / has / can

Observable
→ $

Constant
→ UPPER_CASE

Method
→ Verb + Noun

Event
→ on + Action

================================================================

# SCSS Convention

- Dùng BEM.
- Variable bắt đầu bằng $.
- Không hardcode màu.
- Tách SCSS theo module.
