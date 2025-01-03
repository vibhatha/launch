# Project Mangement 

LDF will be using a close-to-code approach for project management. And our goal is to map what is in the state
of the art project management tools to what already exists in Github to the closest possible level. 

---

### **1. GitHub Features Overview**
- **Issues**: Represent individual work items or tasks.
- **Labels**: Categorize and prioritize issues (e.g., Epic, Task, Bug, High Priority).
- **Milestones**: Group issues into deliverable units or sprints.
- **GitHub Projects**: A Kanban-style board to organize issues visually.
- **Comments & Discussions**: Collaborate and add updates.

---

### **2. Mapping EPICs, Tasks, and Subtasks**
#### **Epics**
- **Definition**: High-level objectives or large features broken into smaller tasks.
- **Implementation**:
  - Create a **GitHub Issue** for each Epic.
  - Use a label, e.g., `Epic`, to differentiate from other issues.
  - List all related tasks as a checklist in the Epic's issue description, linking to individual task issues (e.g., `#123`, `#124`).
  - Example:
    ```
    ### Epic: Build User Authentication
    **Description**: Implement the authentication module with login, registration, and password reset.
    - [ ] #123 Task: Create Login Page
    - [ ] #124 Task: Set Up Backend Authentication
    - [ ] #125 Task: Implement Password Reset
    ```

#### **Tasks**
- **Definition**: Individual, actionable work items under an Epic.
- **Implementation**:
  - Create a **GitHub Issue** for each task.
  - Link the task issue to the Epic by referencing the Epic’s issue number (e.g., `See Epic #101`).
  - Use labels like `Task` for categorization.

#### **Subtasks**
- **Definition**: Smaller, granular steps within a task.
- **Implementation**:
  - Add subtasks as checklists in the Task issue description.
  - Example:
    ```
    ### Task: Set Up Backend Authentication
    - [ ] Install authentication library
    - [ ] Write unit tests
    - [ ] Configure JWT tokens
    ```

---

### **3. Organizing Workflows**
#### **GitHub Projects**:
- Use **Projects** to visualize work progress.
  - **Columns**: To Do, In Progress, Review, Done.
  - **Cards**: Add issues (Epics, Tasks) as cards in the project board.

#### **Labels**:
- Define and apply labels to classify and prioritize work.
  - Examples:
    - `Epic`
    - `Task`
    - `Bug`
    - `High Priority`
    - `In Progress`

#### **Milestones**:
- Use milestones to group issues by deadlines or sprints.
  - Example:
    - Milestone: "Sprint 1 - User Authentication"
    - Linked Issues: #101, #123, #124, etc.

---

### **4. Tracking and Collaboration**
- **Cross-Issue References**: Mention related issues within descriptions or comments.
  - Example: In Task #123, write *"Depends on completion of #101 (Epic)."*
- **Automations** (Optional with GitHub Actions):
  - Automatically move cards in Projects when issues are closed.
  - Example: Move a task to the "Done" column upon issue closure.
- **Pull Requests**:
  - Link PRs to tasks using keywords (e.g., `Closes #123`) to track development progress.

---

### **Example Workflow**
1. **Create Epic**: "Build User Authentication" (#101) with a checklist of tasks (#123, #124).
2. **Create Tasks**: Each task as an issue with linked subtasks.
3. **Use Labels**: Assign labels like `Epic`, `Task`, or `High Priority`.
4. **Organize in Projects**: Add all issues to a GitHub Project board with relevant columns.
5. **Track Progress**: Update checklists and close issues as work completes.

This workflow keeps your project management tightly integrated into GitHub, eliminating the need for external tools.