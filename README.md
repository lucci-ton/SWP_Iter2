# MIS – Intern Management System

## Overview

**MIS – Intern Management System** là hệ thống web hỗ trợ quản lý toàn bộ vòng đời của thực tập sinh tại một phòng Lab, từ tiếp nhận CV, phỏng vấn, tuyển chọn đến đào tạo, đánh giá và gửi thông báo.

### End-to-End Flow

```text
Candidate
→ CV Review
→ Interview Scheduling
→ Interview Evaluation
→ Pass / Fail
→ Intern
→ Class Assignment
→ Lecturer Assignment
→ Training
→ Evaluation
→ Notification
```

---

## My Role – Business Analyst

Trong dự án, tôi chịu trách nhiệm phân tích nghiệp vụ và chuyển đổi yêu cầu business thành yêu cầu hệ thống có thể triển khai.

Các công việc chính:

- Thu thập và làm rõ yêu cầu
- Phân tích business flow và system flow
- Xác định Actor, Use Case và phạm vi chức năng
- Xây dựng Feature List và Use Case Description
- Xác định Business Rule và Validation Rule
- Phân tích trạng thái và luồng chuyển trạng thái
- Phân tích entity và mối quan hệ dữ liệu
- Thiết kế Business Flow và Swimlane Diagram
- Phối hợp với Developer, Tester và stakeholder
- Hỗ trợ API Testing và UAT

---

## Main Actors

| Actor | Responsibility |
|---|---|
| Admin / Lab Coordinator | Quản lý Candidate, Intern, Interview và Class |
| Interviewer | Phỏng vấn và đánh giá Candidate |
| Lecturer | Phụ trách lớp và đánh giá Intern |
| Candidate | Tham gia quy trình tuyển dụng |
| Intern | Tham gia chương trình đào tạo |
| System | Xử lý workflow, trạng thái và notification |

---

## Core Modules

### Candidate Management

- Quản lý hồ sơ Candidate
- Lưu trữ CV
- Review CV
- Theo dõi trạng thái tuyển dụng

### Interview Management

- Tạo và cập nhật lịch phỏng vấn
- Phân công Interviewer
- Ghi nhận đánh giá
- Xác định kết quả Pass / Fail

### Intern Management

- Chuyển Candidate đã Pass thành Intern
- Theo dõi trạng thái đào tạo
- Theo dõi lớp và kết quả đánh giá

### Class & Lecturer Management

- Tạo và quản lý lớp
- Xếp Intern vào lớp
- Phân công Lecturer
- Theo dõi trạng thái lớp

### Evaluation

- Nhập điểm và nhận xét
- Theo dõi kết quả Intern
- Tổng hợp kết quả theo Intern / Class

### Notification

- Lịch phỏng vấn
- Kết quả tuyển dụng
- Xếp lớp
- Lịch học
- Kết quả đánh giá

---

## State Management

### Candidate

```text
New
→ CV Reviewing
→ Interview Scheduled
→ Interviewed
→ Passed / Failed
```

### Intern

```text
Waiting for Class
→ Training
→ Completed
```

### Class

```text
Planning
→ Upcoming
→ In Progress
→ Completed
```

---

## Business Rules

Một số rule tiêu biểu:

- Candidate phải có thông tin hợp lệ trước khi tham gia quy trình tuyển dụng
- Candidate chỉ được chuyển thành Intern khi đã Pass
- Interview phải có Candidate, Interviewer và thời gian hợp lệ
- Intern chỉ được xếp vào Class phù hợp
- Chỉ người có quyền mới được nhập hoặc cập nhật Evaluation
- Score phải đúng kiểu dữ liệu và nằm trong khoảng hợp lệ
- Các thao tác phải tuân thủ trạng thái hiện tại của entity

---

## Core Data Model

```text
Candidate
   │
   └── Interview
          │
          └── Interview Result
                  │
                  └── Intern
                         │
                         ├── Class
                         │     └── Lecturer
                         │
                         └── Evaluation

Candidate / Intern
        └── Notification
```

Các entity chính:

- Candidate
- Interview
- Intern
- Class
- Lecturer
- Evaluation
- Notification

---

## Validation

Các nhóm validation chính:

- Required Field
- Data Type
- Format
- Duplicate
- Range
- Date Validation
- Permission
- State Transition

---

## API Testing & UAT

### API Testing

- Request / Response
- HTTP Status Code
- Required Field
- Data Type
- Business Validation
- Error Response
- Mapping dữ liệu giữa API và UI

### UAT

- Happy Case
- Validation Case
- Boundary Case
- Permission Case
- Invalid Data
- Status Transition
- End-to-End Flow

---

## BA Deliverables

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

## Repository Structure

```text
MIS-Intern-Management-System/
│
├── README.md
│
├── docs/
│   ├── 01_Project_Overview.md
│   ├── 02_Business_Flow.md
│   ├── 03_Feature_List.md
│   ├── 04_Business_Rules.md
│   ├── 05_Data_Model.md
│   └── 06_API_UAT_Notes.md
│
└── diagrams/
    ├── business-flow.png
    ├── swimlane.png
    └── erd.png
```

---

## Skills Demonstrated

- Requirement Analysis
- Business Process Analysis
- Use Case Analysis
- Business Rule Definition
- Data Analysis
- State Management
- API Understanding & Testing
- UAT
- Cross-functional Collaboration

Định hướng chính của dự án là kết nối:

```text
Business Requirement
→ Business Process
→ Business Rule
→ System Behavior
→ Data / API
→ Testing
```

---

## Tools

- Jira
- Confluence / Lark
- Figma
- Draw.io
- Postman
- Swagger
- SQL
- Git / GitHub

---

## Disclaimer

Repository này được xây dựng với mục đích portfolio cá nhân.

Tên, dữ liệu và một số quy trình đã được đơn giản hóa hoặc ẩn danh. Không công khai dữ liệu nhạy cảm, credential hoặc tài liệu nội bộ của tổ chức.
