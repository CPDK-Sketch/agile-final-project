# Agile Final Project - Product Catalog

## 📖 Overview

The goal is to create a catalog system that allows **creating**, **retrieving**, **updating**, and **deleting** products. Additional features include **liking** and **disliking** products, and hosting the application in the **cloud** with **automated deployments**.

---

## 🚀 Project Setup

### 1. **Repository Creation**
- **GitHub Repository**: `agile-final-project`
- This repository is public and tracks project progress using **Agile methodologies** and a **Kanban board**.

### 2. **GitHub Kanban Board Setup**
- The Kanban board is used to track progress through various columns.
  
**Kanban Board Columns:**

| **Column**     | **Description**                                                                 |
|----------------|---------------------------------------------------------------------------------|
| **Icebox**     | Tasks that are low-priority or not yet ready for development.                    |
| **Product Backlog** | The list of tasks that are prioritized for the next sprint.                     |
| **Sprint Backlog** | Tasks selected from the Product Backlog for the current sprint.                 |
| **In Progress**| Tasks actively being worked on.                                                 |
| **Review/QA**  | Tasks that have been completed and are awaiting review or testing.              |
| **Done**       | Tasks that are fully completed and meet acceptance criteria.                     |

---

### 3. **Issue Template**
An **issue template** has been created to ensure each task is well-defined and includes the **user story** and **acceptance criteria** in **Gherkin syntax**.

---

## 📝 Sprint Workflow

### **Sprint Planning**
Each sprint begins with the selection of tasks from the **Product Backlog**. Tasks are prioritized, estimated with **story points**, and moved to the **Sprint Backlog**.

#### **Story Points**:
- Story points are used to estimate the complexity and effort of each task.
- Points are given based on the **Fibonacci sequence**: `1`, `2`, `3`, `5`, `8`, `13`.

---

## 🧑‍💻 Sprint Execution

### **Step-by-Step Sprint Execution**

1. **Move Tasks to "In Progress"**:  
   - Once you begin working on a task, move it from **Product Backlog** (or **Sprint Backlog**) to **In Progress**.

2. **Move Tasks to "Review/QA"**:  
   - After completing a task, move it to **Review/QA** for testing or code review.

3. **Move Tasks to "Done"**:  
   - Once tasks pass review/QA and meet acceptance criteria, move them to **Done**.

4. **Repeat for Remaining Stories**:  
   - Move each task across columns, from **Sprint Backlog** to **Done**, ensuring the workflow is tracked.

---

### **Example User Stories for Sprint 1**
Each user story is written in **Gherkin syntax** to define clear **Given-When-Then** acceptance criteria.

#### **1. Create Product**
- **Story Points**: 5
- **Acceptance Criteria**:
    ```gherkin
    Given an authenticated admin
    When they send a POST request to /products with valid product data
    Then the product is saved in the catalog and a 201 response is returned
    ```
- **CLI Command**:
    ```bash
    curl -X POST http://localhost:3000/products -d '{"name": "Product A", "price": 100}'
    ```

#### **2. Retrieve Product**
- **Story Points**: 3
- **Acceptance Criteria**:
    ```gherkin
    Given a valid product ID
    When a GET request is made to /products/{id}
    Then the system returns the product data with a 200 response
    ```
- **CLI Command**:
    ```bash
    curl -X GET http://localhost:3000/products/1
    ```

#### **3. Update Product**
- **Story Points**: 3
- **Acceptance Criteria**:
    ```gherkin
    Given an authenticated admin and an existing product
    When they send a PUT request to /products/{id} with updated data
    Then the product is updated and a 200 response is returned
    ```
- **CLI Command**:
    ```bash
    curl -X PUT http://localhost:3000/products/1 -d '{"name": "Updated Product", "price": 120}'
    ```

#### **4. Delete Product**
- **Story Points**: 2
- **Acceptance Criteria**:
    ```gherkin
    Given an authenticated admin and a valid product ID
    When they send a DELETE request to /products/{id}
    Then the product is removed from the catalog and a 204 response is returned
    ```
- **CLI Command**:
    ```bash
    curl -X DELETE http://localhost:3000/products/1
    ```

---

## 🔖 Labels

We use **labels** to categorize issues and user stories:

- **Technical Debt**: For tasks that involve addressing technical debt or improving code quality without adding new features.
- **Enhancement**: For tasks that enhance existing functionality.
- **Bug**: For issues that represent bugs or defects in the system.

---

## 📊 Tracking Progress

### **Kanban Board Movement**
Tasks move through the following columns:
- **Icebox → Product Backlog → Sprint Backlog → In Progress → Review/QA → Done**.

### **Burndown Chart**
The **Burndown Chart** is automatically updated as tasks are moved to **Done**, showing the remaining story points for the sprint. This helps visualize progress and ensures the sprint is on track.

---

## 🔄 Sprint Retrospective & Review

### **Sprint Retrospective**
At the end of the sprint, conduct a **Sprint Retrospective** to review:
- **What went well** during the sprint.
- **What could be improved** for the next sprint.
- Any **blockers** or **challenges** faced.

### **Sprint Review**
- Review completed tasks to ensure they meet **acceptance criteria**.
- Ensure that all tasks have passed **Review/QA** and are properly tested.

---

## 🚀 Next Steps

1. **Sprint Review and Retrospective**: Review the results of Sprint 1 and conduct a retrospective meeting to discuss improvements.
2. **Create Sprint 2**: Based on the remaining tasks, plan for the next sprint and move appropriate tasks into the **Sprint Backlog**.
3. **Iterate**: Continue iterating on the product catalog with future sprints.

---

Let me know if you need further adjustments or clarifications!

