Mini Jira (Project Management System)

Ứng dụng quản lý công việc (Task Management) xây dựng bằng Java, minh họa các cấu trúc dữ liệu: Linked List, Binary Search Tree (BST) và Directed Graph.

Mô tả đề tài

Mini Jira mô phỏng hệ thống quản lý công việc với:

Bảng công việc (To Do / Doing / Done)

Tra cứu Task nhanh theo ID

Quản lý phụ thuộc giữa các Task

Tính năng (DSA)
Module	Cấu trúc dữ liệu	Chức năng
Task Board	Linked List	Mỗi cột (To Do, Doing, Done) là một Linked List
Task Search	BST	Tìm kiếm Task theo ID nhanh
Task Dependency	Directed Graph	Quản lý phụ thuộc Task A → Task B
Yêu cầu hệ thống

JDK 17 trở lên

Maven 3.x

Cách chạy
1. Build project
mvn compile
2. Chạy chương trình
mvn exec:java -Dexec.mainClass="com.minijira.app.Main"

(Thay bằng đúng main class của bạn nếu khác)

Hướng dẫn Demo
1️⃣ Task Board (Linked List)

Thêm Task mới vào cột To Do

Di chuyển Task giữa các cột:

To Do → Doing

Doing → Done

Khi di chuyển:

Cắt node khỏi Linked List cũ

Thêm node vào Linked List mới

Hiển thị theo dạng:

Head → Task1 → Task2 → Task3 → Tail
2️⃣ Tra cứu Task (BST)

Thêm Task vào hệ thống (tự insert vào BST)

Tìm kiếm theo ID (ví dụ: T001)

Xóa Task khỏi hệ thống

Độ phức tạp:

Search: O(log n)

Insert: O(log n)

Delete: O(log n)

3️⃣ Phụ thuộc Task (Graph)

Thiết lập quan hệ phụ thuộc:

Task A phải hoàn thành trước Task B

Biểu diễn bằng đồ thị có hướng

Kiểm tra:

Task có thể thực hiện chưa?

Có tồn tại chu trình (cycle) không?

Cấu trúc project
src/main/java/com/minijira/
├── app/
│   └── Main.java                # Entry point
├── entities/
│   ├── Task.java
│   └── Project.java
└── structures/
    ├── MyLinkedList.java        # Task Board (ToDo/Doing/Done)
    ├── MyBST.java               # Search Task by ID
    └── MyGraph.java             # Task Dependency (Directed Graph)
Chi tiết kỹ thuật (DSA)
Cấu trúc	Độ phức tạp	Mô tả
Linked List	Insert O(1), Delete O(n)	Mỗi cột là một danh sách liên kết
BST	Search O(log n)	Tìm kiếm Task theo ID
Directed Graph	DFS O(V+E)	Kiểm tra phụ thuộc và chu trình
Công nghệ sử dụng

Ngôn ngữ: Java

Build tool: Maven

Mô hình: OOP

Cấu trúc dữ liệu: Linked List, BST, Graph

Luồng xử lý chính

Tạo Task → Insert vào:

Linked List (To Do)

BST (Search)

Graph (Node mới)

Di chuyển Task:

Xóa node khỏi Linked List cũ

Thêm vào Linked List mới

Thêm phụ thuộc:

Thêm cạnh A → B trong Graph

Kiểm tra cycle (nếu có)

Chạy test
mvn test
Môn học

Dự án thực hiện cho môn CSD201 – Cấu trúc dữ liệu và giải thuật.
