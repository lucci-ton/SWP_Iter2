# 02. Feature List

## 1. Feature Overview

| Module | Feature / Use Case | Actor | Description |
|---|---|---|---|
| Candidate Management | View Candidate List | Admin | Xem danh sách Candidate và trạng thái hiện tại |
| Candidate Management | View Candidate Detail | Admin | Xem thông tin chi tiết Candidate |
| Candidate Management | Create / Update Candidate | Admin | Tạo mới hoặc cập nhật thông tin Candidate |
| Candidate Management | Manage CV | Admin | Lưu trữ và truy cập CV của Candidate |
| Candidate Management | Review CV | Admin | Review hồ sơ và cập nhật trạng thái Candidate |
| Interview Management | Schedule Interview | Admin | Tạo lịch phỏng vấn cho Candidate |
| Interview Management | Assign Interviewer | Admin | Phân công Interviewer |
| Interview Management | Reschedule Interview | Admin | Cập nhật ngày giờ phỏng vấn |
| Interview Management | View Interview Schedule | Admin / Interviewer | Theo dõi lịch phỏng vấn |
| Interview Management | Evaluate Candidate | Interviewer | Nhập đánh giá và nhận xét sau phỏng vấn |
| Interview Management | Record Interview Result | Admin / Interviewer | Ghi nhận kết quả Pass / Fail |
| Intern Management | Convert Candidate to Intern | Admin | Chuyển Candidate đã Pass thành Intern |
| Intern Management | View Intern List | Admin | Xem danh sách Intern |
| Intern Management | View Intern Detail | Admin / Lecturer | Xem thông tin và quá trình đào tạo |
| Class Management | Create Class | Admin | Tạo lớp đào tạo |
| Class Management | Update Class | Admin | Cập nhật thông tin lớp |
| Class Management | Assign Intern to Class | Admin | Xếp Intern vào lớp |
| Class Management | Assign Lecturer | Admin | Phân công Lecturer phụ trách lớp |
| Class Management | View Class Detail | Admin / Lecturer | Xem thông tin lớp và danh sách Intern |
| Evaluation Management | Create Evaluation | Lecturer | Nhập điểm và nhận xét |
| Evaluation Management | Update Evaluation | Lecturer | Cập nhật kết quả đánh giá |
| Evaluation Management | View Intern Result | Admin / Lecturer | Xem kết quả theo Intern |
| Evaluation Management | View Class Result | Admin / Lecturer | Xem kết quả tổng hợp theo lớp |
| Notification Management | Send Interview Notification | System | Gửi thông báo lịch phỏng vấn |
| Notification Management | Send Interview Result | System | Gửi kết quả tuyển dụng |
| Notification Management | Send Class Assignment | System | Gửi thông báo xếp lớp |
| Notification Management | Send Training Notification | System | Gửi thông báo liên quan đến chương trình đào tạo |

---

## 2. Functional Grouping

### Candidate Management

Mục tiêu: quản lý Candidate từ khi tiếp nhận hồ sơ đến trước khi trở thành Intern.

Các chức năng chính:

- Quản lý thông tin Candidate
- Quản lý CV
- Review hồ sơ
- Theo dõi trạng thái tuyển dụng

### Interview Management

Mục tiêu: quản lý lịch phỏng vấn và kết quả đánh giá Candidate.

Các chức năng chính:

- Schedule Interview
- Assign Interviewer
- Reschedule Interview
- Interview Evaluation
- Recruitment Result

### Intern Management

Mục tiêu: quản lý Candidate sau khi được nhận vào Lab.

Các chức năng chính:

- Convert Candidate to Intern
- Theo dõi trạng thái đào tạo
- Theo dõi lớp và kết quả đánh giá

### Class Management

Mục tiêu: tổ chức chương trình đào tạo.

Các chức năng chính:

- Create / Update Class
- Assign Intern
- Assign Lecturer
- Theo dõi trạng thái lớp

### Evaluation Management

Mục tiêu: quản lý kết quả học tập của Intern.

Các chức năng chính:

- Score
- Comment
- Evaluation Result
- Intern Result
- Class Result

### Notification Management

Mục tiêu: gửi thông tin đến Candidate hoặc Intern tại các mốc quan trọng trong workflow.

Các sự kiện chính:

- Interview Scheduled
- Interview Rescheduled
- Interview Result
- Candidate Passed
- Class Assigned
- Evaluation Completed

---

## 3. End-to-End Feature Flow

```text
Candidate Management
        ↓
Interview Management
        ↓
Recruitment Result
        ↓
Intern Management
        ↓
Class Management
        ↓
Evaluation Management
        ↓
Notification
```

---

## 4. Notes

Feature list trong portfolio tập trung vào phạm vi nghiệp vụ chính. Chi tiết từng Use Case có thể được mở rộng thành:

- Preconditions
- Main Flow
- Alternative Flow
- Business Rules
- Validation Rules
- Output
- Error Handling
