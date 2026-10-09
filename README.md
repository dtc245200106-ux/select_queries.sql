# Bài thực hành: Truy vấn dữ liệu CSDL Quản Lý Sinh Viên

## 📋 Thông tin
- **Database:** QuanLySinhVien
- **Công cụ:** MySQL Workbench
- **Số lượng truy vấn:** 5

## 📝 Danh sách các truy vấn

### Truy vấn 1: Hiển thị tất cả học viên
```sql
SELECT * FROM Student;
Truy vấn 2: Học viên đang theo học
sql
SELECT * FROM Student WHERE Status = 1;
Truy vấn 3: Môn học có Credit < 10
sql
SELECT * FROM Subject WHERE Credit < 10;
Truy vấn 4: Học viên lớp A1
sql
SELECT S.StudentId, S.StudentName, C.ClassName
FROM Student S 
JOIN Class C ON S.ClassId = C.ClassID
WHERE C.ClassName = 'A1';
Truy vấn 5: Điểm môn CF
sql
SELECT S.StudentId, S.StudentName, Sub.SubName, M.Mark
FROM Student S 
JOIN Mark M ON S.StudentId = M.StudentId 
JOIN Subject Sub ON M.SubId = Sub.SubId
WHERE Sub.SubName = 'CF';