## **Product Requirements Document: Serenity Notes**

**Version:** 1.6

**Date:** July 14, 2025

**Author:** \[Your Name/Team\]

**Status:** Professional Feature Set

### **1\. Introduction**

Serenity Notes is a desktop application built with Electron that seamlessly integrates a powerful **ActionHub** for task management and a private, reflective **Journal**. In a world of digital noise, Serenity Notes aims to be a focused and calming space for users to organize their actions and thoughts. The application will prioritize a clean, intuitive user interface and a delightful user experience.

### **2\. Vision and Strategy**

The core vision for Serenity Notes is to provide a minimalist, efficient, and flexible tool that helps users achieve productivity and mindfulness. Many users juggle multiple apps for task management and journaling. Serenity Notes will consolidate these two essential functions into a single, beautifully designed application.

Our strategy is to build a high-quality, **open-source** application that empowers users with full control over their data by allowing them to connect to their own database infrastructure, while providing professional-grade features for power users.

### **3\. User Personas**

*(No changes in this section)*

### **4\. Features**

The application's functionality is divided into two main components: the ActionHub and the Journal.

#### **4.1. ActionHub**

* **Task Creation:**  
  * Quick-add tasks with a title and optional description.  
  * Set due dates and reminders.  
  * Assign priority levels to tasks (e.g., High, Medium, Low).  
  * Create recurring tasks (daily, weekly, monthly).  
* **Task Organization:**  
  * Organize tasks into projects or categories.  
  * Use tags for flexible filtering.  
  * Drag-and-drop to reorder tasks.  
* **Views:**  
  * **Standard Views:** "Today," "Upcoming," "Project," and "Completed" views are available by default.  
  * **Custom Saved Views:** Users can create and save their own filtered views. For example, a user could create a view named "Urgent Work" that shows all tasks with a "High" priority from their "Work" projects that are due this week.  
* **Daily Progress Indicator:**  
  * A circular progress bar will be prominently displayed in the 'Today' view, visually representing the percentage of completed tasks for the current day to motivate users.  
* **ActionHub Templates:**  
  * Users can create project templates. For instance, a "New Blog Post" template could automatically generate a project with predefined tasks like "Research," "Outline," "Draft," and "Publish."

#### **4.2. Journal**

* **Entry Creation:**  
  * A rich-text editor that supports basic formatting (bold, italics, underline, lists).  
  * The ability to add images to entries.  
* **Task Tagging:**  
  * Users can create tasks directly within a journal entry by using a specific syntax (e.g., @task name). This will automatically create the task in the ActionHub and create a live, two-way link between the journal entry and the task.  
* **Journal Templates:**  
  * Users can create templates for recurring entry types like "Daily Standup," "Weekly Review," or "Meeting Notes." Selecting a template would pre-populate the journal entry with a defined structure.  
* **Organization and Navigation:**  
  * A calendar view to easily navigate between entries.  
  * Search functionality to find entries by keyword.  
  * Tagging for categorizing entries (e.g., \#gratitude, \#work, \#personal).  
* **Privacy and Security:**  
  * Password protection for the journal section (local application lock).

#### **4.3. General Application Features**

* **Command Palette:**  
  * A universal command palette, accessible via a keyboard shortcut (e.g., Cmd/Ctrl \+ K), will allow users to instantly perform actions like jumping to a project, creating a new task, finding a journal entry, or switching themes.  
* **Data Portability:**  
  * **Advanced Import:** An import tool will allow users to migrate their data from other popular services (e.g., Todoist, Trello, Apple Notes) to make switching to Serenity Notes seamless.  
  * **Export:** Ability to export ActionHub lists (as CSV) and journal entries (as Markdown or PDF).  
* **Database Connection & Sync:**  
  * A guided onboarding flow for database setup.  
  * Hourly sync with offline support and a clear status indicator.  
  * Robust conflict resolution UI.  
* **Themes:** Light and Dark mode options.  
* **Keyboard Shortcuts:** Comprehensive keyboard shortcuts for all major actions.

### **5\. UI/UX Best Practices**

*(No changes in this section)*

### **6\. Technical Requirements**

* **Frontend Framework:** **React with TypeScript**.  
* **Core Framework:** Electron.  
* **CSS Framework:** The UI will be built using the **Tailwind CSS** utility-first framework.  
* **Platform:** Cross-platform (macOS, Windows, and Linux).  
* **Database:** **PostgreSQL (user-hosted)**.  
* **Schema Management:** Automated schema migration with transactional safety.  
* **Credential Storage:** Secure storage via the native OS keychain (keytar).  
* **Performance:**  
  * **UI Virtualization:** UI Virtualization (e.g., via TanStack Virtual) for all long lists.  
  * **Search Optimization:** Local search index (e.g., via lunr.js) for instant full-text search.  
* **Installation:** A straightforward installation process.

### **7\. Release Criteria**

*(No changes in this section)*

### **8\. Success Metrics**

*(No changes in this section)*