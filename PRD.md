## **Product Requirements Document: Serenity Notes**

**Version:** 1.8

**Date:** July 14, 2025

**Author:** \[Your Name/Team\]

**Status:** Final

### **1\. Introduction**

Serenity Notes is a **cross-platform application for desktop and mobile** that seamlessly integrates a powerful **ActionHub** for task management and a private, reflective **Journal**. In a world of digital noise, Serenity Notes aims to be a focused and calming space for users to organize their actions and thoughts, with a consistent experience across all their devices.

### **2\. Vision and Strategy**

The core vision for Serenity Notes is to provide a minimalist, efficient, and flexible tool that helps users achieve productivity and mindfulness. Our strategy is to build a high-quality, **open-source ecosystem** that provides a unified and consistent experience, allowing users to seamlessly switch between their desktop and mobile devices while maintaining full control over their data, and providing professional-grade features for power users.

### **3\. User Personas**

* **"Productive Professional" (Priya):** A 30-year-old marketing manager who needs to manage a demanding workload, track project deadlines, and jot down meeting notes. She values efficiency, keyboard shortcuts, and a clean, distraction-free interface.  
* **"Mindful Student" (Sam):** A 22-year-old university student who wants to stay organized with his assignments and also cultivate a daily journaling habit to manage stress and self-reflect. He appreciates a visually appealing and customizable interface and values the control of hosting his own data.

### **4\. Features**

The application's functionality is divided into two main components: the ActionHub and the Journal. All features are expected to be available and consistent across both desktop and mobile platforms, optimized for each form factor.

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
  * Robust conflict resolution UI, including handling for deletion conflicts.  
* **Image Management:**  
  * Client-side image optimization before upload.  
  * A Least Recently Used (LRU) cache policy with a configurable size limit.  
* **Themes:** Light and Dark mode options.  
* **Keyboard Shortcuts:** Comprehensive keyboard shortcuts for all major actions.

### **5\. UI/UX Best Practices**

The design must be responsive and adaptive, ensuring a consistent brand identity and intuitive user experience on both desktop and mobile. The design system (components, typography, spacing) will be shared across both platforms.

### **6\. Technical Requirements**

* **Platform Architecture:** The project will be developed within a **monorepo** to maximize code sharing and ensure consistency between the desktop and mobile applications. This structure will contain:  
  * **Shared Core Logic (core package):** All business logic, database interactions, sync logic, conflict resolution, and state management will reside in a shared package used by both client apps.  
  * **Desktop Application:** Built with **Electron**, using **React** and **TypeScript**.  
  * **Mobile Application:** Built with **React Native** and **TypeScript**.  
* **Frontend Framework:** **React** (for Electron) and **React Native** (for mobile) will be used.  
* **CSS Framework:** The UI will be built using the **Tailwind CSS** ecosystem, which supports both web (for Electron) and React Native (via nativewind), ensuring a consistent, minimalistic design.  
* **Database:** **PostgreSQL (user-hosted)**.  
* **Schema Management:** Automated schema migration with transactional safety. If a migration fails, it will be automatically rolled back, and a specific error message will be shown to the user.  
* **Credential Storage:** Secure storage via the native OS keychain (keytar on desktop, equivalent secure storage on mobile), with a graceful fallback and user warning if the keychain is inaccessible.  
* **Performance:**  
  * **UI Virtualization:** UI Virtualization for all long lists on both platforms.  
  * **Search Optimization:** Local search index for instant full-text search.  
* **Installation:** A straightforward installation process for all target platforms (macOS, Windows, Linux, iOS, Android).

### **7\. Release Criteria**

* All core features of the ActionHub and Journal are fully implemented and functional on both desktop and mobile.  
* The monorepo architecture is correctly set up with a shared core logic package.  
* Database connection, automatic schema migration, and hourly sync are working reliably.  
* Offline caching and the conflict resolution UI are fully functional.  
* The application is stable and free of critical bugs.  
* The UI is polished and adheres to the defined design principles across all platforms.  
* Comprehensive user documentation, especially regarding database setup and connection.

### **8\. Success Metrics**

* **Community Engagement:** Number of downloads, forks, and contributions on its repository (e.g., GitHub).  
* **User Adoption:** Number of active users (this may be hard to track directly, so we'd rely on community feedback).  
* **User Satisfaction:** Positive feedback, issue reporting, and feature requests from the community.