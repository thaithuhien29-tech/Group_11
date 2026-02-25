<p align="center">
  <h1 align="center">📋 Mini Jira - Task Management System</h1>
  <p align="center">
    Java Application demonstrating Linked List, BST & Directed Graph (DFS)
  </p>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Java-21-blue?logo=java" />
  <img src="https://img.shields.io/badge/Maven-3.x-orange?logo=apachemaven" />
  <img src="https://img.shields.io/badge/DSA-LinkedList%20%7C%20BST%20%7C%20Graph-green" />
  <img src="https://img.shields.io/badge/Status-Completed-success" />
</p>

---

## 📌 Overview

Mini Jira là hệ thống quản lý công việc mô phỏng Jira, được xây dựng bằng **Java** nhằm minh họa việc áp dụng các cấu trúc dữ liệu trong thực tế.

🔎 Dự án tập trung vào:

- 🔗 Linked List (Task Board)
- 🌳 Binary Search Tree (Search Task by ID)
- 🔄 Directed Graph (Task Dependencies & Cycle Detection)

---

## 🚀 Features (DSA Modules)

| Module | Data Structure | Chức năng |
|--------|---------------|------------|
| **Task Board** | Linked List | Quản lý ToDo / Doing / Done |
| **Task Search** | BST | Tìm kiếm Task theo ID |
| **Task Dependency** | Directed Graph | Quản lý phụ thuộc giữa các Task |
| **Cycle Detection** | DFS | Kiểm tra chu trình phụ thuộc |

---

## 🏗️ Project Structure
src/main/java/com/minijira/
├── app/
│ └── Main.java # Entry point
├── entities/
│ ├── Task.java
│ └── Project.java
└── structures/
├── MyLinkedList.java # Task Board
├── MyBST.java # Search by ID
└── MyGraph.java # Directed Graph + DFS

---

## 🧠 Technical Details (DSA)

| Structure | Complexity | Description |
|------------|------------|-------------|
| **MyLinkedList** | Insert O(1), Delete O(n) | Mỗi cột (ToDo/Doing/Done) là một linked list |
| **MyBST** | Search O(log n) | Tìm kiếm Task theo ID |
| **MyGraph** | DFS O(V+E) | Kiểm tra phụ thuộc và chu trình |

---

## ⚙️ Technologies Used

| Component | Technology |
|------------|------------|
| Language | Java 21 |
| Build Tool | Maven |
| Architecture | OOP |
| Data Structures | Linked List, BST, Graph |

---

## ▶️ How to Run

### 1️⃣ Compile

```bash
mvn compile
2️⃣ Run Application
mvn exec:java -Dexec.mainClass="com.minijira.app.Main"
🔄 Main Workflow
Step	Action	Related Structure
1	Create Task	Linked List + BST + Graph
2	Move Task	Linked List
3	Search Task	BST
4	Add Dependency	Graph
5	Check Cycle	Graph (DFS)
Dự án thực hiện cho môn:

CSD201 – Data Structures and Algorithms
