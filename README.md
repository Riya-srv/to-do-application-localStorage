
**Project Description: To-Do List Application**
**Overview**
This application is built using vanilla JavaScript, HTML, and CSS, and leverages the browser's local storage to persist tasks across page refreshes. Users can add new tasks, mark them as completed, and delete tasks as needed.

**Key Features**
**Add Tasks:**

Users can enter tasks through a text input field. By clicking the "Add Task" button, the application creates a new task object and displays it in the task list.
**Toggle Task Completion:**

Clicking on a task (not the delete button) toggles its completion status, visually marking it as completed by applying a CSS class.
**Delete Tasks:**

Each task has a "Done" button that, when clicked, removes the task from the list and updates the local storage to reflect this change.
**Persistent Storage:**

All tasks are stored in the browser's local storage, ensuring that users' tasks are saved even after refreshing the page.

**Code Breakdown**
Event Listener for DOMContentLoaded:

The application starts by waiting for the DOM to fully load before executing the main logic. This ensures that all elements are accessible.
**Task Management:**

The application initializes with existing tasks from local storage or an empty array if none are found. It then renders these tasks immediately upon loading.
**Adding New Tasks:**

Users can add tasks by inputting text and clicking the "Add Task" button. The application checks for empty inputs and prevents adding blank tasks.
**Rendering Tasks:**

Each task is represented by an <li> element, which includes the task text and a "Done" button. The renderTask function handles creating and appending these elements to the DOM.
**Toggle Completion:**

Tasks can be marked as completed by clicking on the task itself. This toggles a completed class that visually indicates the task's status.
**Deleting Tasks:**

The "Done" button allows users to delete tasks. Clicking this button stops the click event from bubbling up to the task itself, preventing unintended toggling of completion status.
**Saving Tasks:**

The saveTasks function updates local storage every time a task is added, toggled, or deleted, ensuring data integrity.
