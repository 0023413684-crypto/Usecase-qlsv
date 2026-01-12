```mermaid
flowchart LR
usecaseDiagram
actor "Sinh viên" as SV
actor "Giảng viên" as GV
actor "Cán bộ quản lý" as CB
actor "Quản trị viên" as QT

rectangle "Hệ thống Quản lý Sinh viên" {

  (Đăng nhập hệ thống) as UC_Login

  (Tra cứu thông tin sinh viên) as UC_SearchSV
  (Tra cứu kết quả học tập) as UC_TraCuuDiem
  (Đăng ký môn học) as UC_DangKyMH

  (Quản lý sinh viên) as UC_QLSV
  (Quản lý lớp học) as UC_QLLop
  (Quản lý môn học) as UC_QLMH
  (Nhập & cập nhật điểm) as UC_NhapDiem

  (Quản lý người dùng) as UC_QLUser
  (Phân quyền hệ thống) as UC_PhanQuyen
}

SV --> UC_Login
SV --> UC_TraCuuDiem
SV --> UC_DangKyMH

GV --> UC_Login
GV --> UC_NhapDiem
GV --> UC_TraCuuDiem

CB --> UC_Login
CB --> UC_QLSV
CB --> UC_QLLop
CB --> UC_QLMH
CB --> UC_SearchSV

QT --> UC_Login
QT --> UC_QLUser
QT --> UC_PhanQuyen
```
