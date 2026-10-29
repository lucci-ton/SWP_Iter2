# 01. Project Overview

## 1. Project Summary

**MIS – Intern Management System** là hệ thống web hỗ trợ quản lý toàn bộ vòng đời của thực tập sinh tại một phòng Lab, từ tiếp nhận hồ sơ ứng tuyển, phỏng vấn, tuyển chọn đến đào tạo, đánh giá và gửi thông báo.

Hệ thống giúp tập trung dữ liệu Candidate và Intern, chuẩn hóa quy trình vận hành và hỗ trợ các bên liên quan theo dõi trạng thái của từng ứng viên trong suốt quá trình tuyển dụng và đào tạo.

---

## 2. Business Problem

Quá trình quản lý thực tập sinh bao gồm nhiều bước và nhiều nhóm dữ liệu khác nhau:

- Hồ sơ Candidate
- CV
- Lịch phỏng vấn
- Kết quả phỏng vấn
- Thông tin Intern
- Lớp đào tạo
- Lecturer
- Điểm và đánh giá
- Notification

Nếu các dữ liệu này được quản lý rời rạc, việc theo dõi trạng thái, phối hợp giữa các bên và truy vết thông tin sẽ gặp nhiều khó khăn.

MIS được xây dựng nhằm tập trung các quy trình trên vào một hệ thống duy nhất.

---

## 3. Business Goal

- Quản lý tập trung Candidate và Intern
- Chuẩn hóa quy trình tuyển dụng
- Hỗ trợ lên lịch và quản lý phỏng vấn
- Quản lý lớp đào tạo và Lecturer
- Theo dõi kết quả học tập của Intern
- Hỗ trợ gửi Notification theo từng giai đoạn
- Đảm bảo khả năng truy vết dữ liệu xuyên suốt vòng đời Candidate → Intern

---

## 4. Scope

### In Scope

- Candidate Management
- CV Management
- Interview Management
- Recruitment Result
- Intern Management
- Class Management
- Lecturer Assignment
- Evaluation Management
- Notification Management

### Out of Scope

Các chức năng chưa được mô tả trong phạm vi portfolio này:

- Payroll
- Attendance
- Recruitment Marketing
- Employee Management sau giai đoạn Intern
- HRM đầy đủ

---

## 5. Main Actors

| Actor | Responsibility |
|---|---|
| Admin / Lab Coordinator | Quản lý Candidate, Intern, Interview, Class và các hoạt động vận hành |
| Interviewer | Phỏng vấn và đánh giá Candidate |
| Lecturer | Phụ trách lớp và đánh giá Intern |
| Candidate | Tham gia quy trình tuyển dụng |
| Intern | Tham gia chương trình đào tạo |
| System | Xử lý workflow, trạng thái và notification |

---

## 6. High-Level Business Flow

```text
Candidate
→ CV Review
→ Interview Scheduling
→ Interview
→ Evaluation
→ Pass / Fail
→ Intern
→ Class Assignment
→ Lecturer Assignment
→ Training
→ Evaluation
→ Notification
```

---

## 7. My Role – Business Analyst

Trong dự án, tôi tham gia vào quá trình phân tích nghiệp vụ và chuyển đổi yêu cầu business thành yêu cầu hệ thống có thể triển khai.

Các công việc chính:

- Thu thập và làm rõ yêu cầu
- Phân tích business flow và system flow
- Xác định actor, use case và phạm vi chức năng
- Xây dựng feature list
- Xác định business rule và validation rule
- Phân tích trạng thái và state transition
- Phân tích entity và mối quan hệ dữ liệu
- Thiết kế business flow và swimlane diagram
- Phối hợp với Developer, Tester và stakeholder
- Hỗ trợ API Testing
- Thực hiện UAT theo yêu cầu nghiệp vụ

---

## 8. BA Deliverables

- Project Overview
- Feature List
- Use Case Description
- Business Flow
- Swimlane Diagram
- Business Rules
- Validation Rules
- Data / Entity Analysis
- State Transition Analysis
- API Testing Notes
- UAT Scenario

---

## 9. System Analysis Focus

Dự án được phân tích theo hướng kết nối giữa business và system:

```text
Business Requirement
→ Business Process
→ Business Rule
→ System Behavior
→ Data / API
→ Testing & Validation
```

---

## 10. Disclaimer

Nội dung trong repository được xây dựng với mục đích portfolio cá nhân.

Tên, dữ liệu và một số quy trình đã được đơn giản hóa hoặc ẩn danh. Không có dữ liệu nhạy cảm, credential hoặc tài liệu nội bộ của tổ chức được công khai.
