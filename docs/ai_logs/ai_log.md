MiniJira_GroupXX

✅ CẤU TRÚC PROJECT (Mini Jira Version)
MiniJira_GroupXX/
├── src/
│ ├── main/
│ │ ├── java/
│ │ │ └── com/
│ │ │ └── minijira/
│ │ │ ├── app/
│ │ │ │ ├── ConsoleApp.java
│ │ │ │ └── WebServer.java
│ │ │ │
│ │ │ ├── entities/
│ │ │ │ ├── Task.java
│ │ │ │ └── Project.java
│ │ │ │
│ │ │ ├── structures/
│ │ │ │ ├── Node.java
│ │ │ │ ├── MyLinkedList.java
│ │ │ │ ├── MyBST.java
│ │ │ │ └── MyGraph.java
│ │ │ │
│ │ │ └── utils/
│ │ │ ├── FileLoader.java
│ │ │ └── InputValidator.java
│ │ │
│ │ └── resources/
│ │ ├── data/
│ │ │ ├── tasks.txt
│ │ │ └── dependencies.txt
│ │ │
│ │ └── public/
│ │ ├── index.html
│ │ ├── style.css
│ │ ├── script.js
│ │ └── assets/
│ │
│ └── test/
│ └── java/
│ └── com/
│ └── minijira/
│ └── structures/
│ ├── MyLinkedListTest.java
│ └── MyBSTTest.java

✅ SKELETON CODE (TUẦN 1–3)
1️⃣ app/ConsoleApp.java
package com.minijira.app;

import com.minijira.entities.Task;
import com.minijira.structures.MyLinkedList;
import com.minijira.structures.MyBST;
import com.minijira.structures.MyGraph;

public class ConsoleApp {

    public static void main(String[] args) {

        System.out.println("=== MINI JIRA - CONSOLE DEMO ===");

        MyLinkedList<Task> todoList = new MyLinkedList<>();
        MyBST taskTree = new MyBST();
        MyGraph taskGraph = new MyGraph();

        System.out.println("System initialized successfully.");
    }
}

2️⃣ app/WebServer.java
package com.minijira.app;

public class WebServer {

    public void start() {
        System.out.println("Web Server starting...");
    }
}

3️⃣ entities/Task.java
package com.minijira.entities;

public class Task {

    private String id;
    private String title;
    private String description;
    private String status; // ToDo, Doing, Done

    public Task(String id, String title, String description, String status) {
        this.id = id;
        this.title = title;
        this.description = description;
        this.status = status;
    }

    public String getId() {
        return id;
    }

    public String getStatus() {
        return status;
    }
}

4️⃣ entities/Project.java
package com.minijira.entities;

public class Project {

    private String id;
    private String name;

    public Project(String id, String name) {
        this.id = id;
        this.name = name;
    }
}
🔥 QUAN TRỌNG NHẤT – STRUCTURES

5️⃣ Node.java
package com.minijira.structures;

public class Node<T> {

    public T data;
    public Node<T> next;

    public Node(T data) {
        this.data = data;
        this.next = null;
    }
}

6️⃣ MyLinkedList.java (Task Board - Tuần 1)
package com.minijira.structures;

public class MyLinkedList<T> {

    private Node<T> head;

    public void add(T data) {
        // TODO: implement add
    }

    public void remove(T data) {
        // TODO: implement remove
    }

    public void display() {
        // TODO: implement display
    }
}

7️⃣ MyBST.java (Search Task - Tuần 2)
package com.minijira.structures;

public class MyBST {

    private class TreeNode {
        String key;
        TreeNode left;
        TreeNode right;

        TreeNode(String key) {
            this.key = key;
        }
    }

    private TreeNode root;

    public void insert(String key) {
        // TODO
    }

    public boolean search(String key) {
        return false;
    }

    public void delete(String key) {
        // TODO
    }
}

8️⃣ MyGraph.java (Dependency - Tuần 3)
package com.minijira.structures;

public class MyGraph {

    public void addEdge(String fromTask, String toTask) {
        // TODO
    }

    public boolean hasCycle() {
        return false;
    }
}

✅ UTILS
FileLoader.java
package com.minijira.utils;

public class FileLoader {

    public static void loadTasks(String filePath) {
        // TODO
    }
}
InputValidator.java
package com.minijira.utils;

public class InputValidator {

    public static boolean isValidId(String id) {
        return id != null && !id.isEmpty();
    }
}

✅ UNIT TEST (Skeleton)
MyLinkedListTest.java
package com.minijira.structures;

import org.junit.jupiter.api.Test;

public class MyLinkedListTest {

    @Test
    void testAdd() {
        // TODO
    }
}
MyBSTTest.java
package com.minijira.structures;

import org.junit.jupiter.api.Test;

public class MyBSTTest {

    @Test
    void testInsert() {
        // TODO
    }
}
🎯 Phù hợp kế hoạch tuần 1–3:
Tuần	Nội dung
1	Linked List (Task Board)
2	BST (Search Task)
3	Graph (Dependency + Cycle)
