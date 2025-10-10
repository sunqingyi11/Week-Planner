# Week Plan - Task Management Web App

A beautiful and functional task management application built with HTML, Tailwind CSS, and vanilla JavaScript. Based on a custom Figma design with drag-and-drop functionality.

## Features

### 📋 Task Management
- **Create Tasks**: Click "添加任务" (Add Task) button to open the drawer and create new tasks
- **Edit Tasks**: Click the edit icon (pencil) on any task in the accordion to modify it
- **Delete Tasks**: Click the delete icon (trash) on any task to remove it and all its calendar instances
- **Task Properties**:
  - Name (required)
  - Quadrant (4 options: 重要不紧急, 重要紧急, 不重要但紧急, 不重要不紧急)
  - Color (6 color options)

### 🎨 Task Organization
- **Planning Section (计划中)**: Tasks organized by quadrants (Eisenhower Matrix)
  - Important & Not Urgent
  - Important & Urgent
  - Not Important but Urgent
  - Not Important & Not Urgent
- **This Week Section (本周要务)**: Tasks for the current week
- **Finished Section (已完成)**: Completed tasks

### 📅 Calendar View
- **Weekly Calendar**: 7-day view from Sunday to Saturday
- **Hourly Blocks**: 16 time slots from 7 AM to Night
- **30-Minute Intervals**: Each hour divided into two 30-minute blocks

### 🎯 Drag & Drop Functionality

#### From Accordion to Calendar
1. Drag any task from the accordion sidebar
2. Drop it onto any calendar time block
3. This creates a **duplicate** (child) of the task in the calendar
4. You can create unlimited duplicates

#### Within Calendar
- Drag calendar tasks to reposition them
- Move tasks within the same day or across different days
- Double-click a calendar task to toggle between 30-minute and 1-hour duration
- Right-click a calendar task to delete it

### 👨‍👦 Father-Son Relationship

**Important Concept**: Tasks follow a parent-child relationship model.

- **Father (Parent)**: Tasks in the accordion sidebar
  - Can be edited
  - Can be deleted
  - Properties: name, quadrant, color
  
- **Son (Child)**: Tasks in the calendar
  - Created by dragging from accordion
  - Cannot be edited directly
  - Automatically updated when parent is edited
  - Can be moved, resized, or deleted independently
  - Deleting parent removes all children

**Example**:
1. Create task "Team Meeting" in accordion
2. Drag it to Monday 9 AM → creates child #1
3. Drag it to Wednesday 2 PM → creates child #2
4. Edit "Team Meeting" to "Weekly Sync"
5. Both calendar instances update automatically!

### ⌨️ Keyboard Shortcuts
- `ESC`: Close the drawer

### 💾 Data Persistence
- All tasks are automatically saved to browser's localStorage
- Data persists between sessions
- No backend required

## How to Use

### Getting Started
1. Open `index.html` in a modern web browser
2. Click "添加任务" to create your first task
3. Fill in the task details and click "保存"

### Creating Tasks
1. Click the "添加任务" button (appears when empty or at top when tasks exist)
2. Enter task name (required)
3. Select quadrant from dropdown
4. Choose a color by clicking on a color option
5. Click "保存" to save

### Editing Tasks
1. Hover over a task in the accordion
2. Click the pencil icon
3. Modify any field
4. Click "保存"
5. All calendar instances update automatically

### Scheduling Tasks
1. Find the task in the accordion
2. Click and hold to start dragging
3. Drag to the desired calendar time slot
4. Release to create a calendar instance

### Managing Calendar Tasks
- **Move**: Drag and drop to new time slot
- **Resize**: Double-click to toggle between 30min and 60min
- **Delete**: Right-click and confirm deletion

### Tips & Tricks
- Use colors to categorize tasks visually
- Organize tasks by quadrants for better priority management
- Create multiple calendar instances for recurring activities
- Edit the parent task to update all scheduled instances at once

## Technical Details

### Technologies
- HTML5
- Tailwind CSS (via CDN)
- Vanilla JavaScript
- LocalStorage API
- HTML5 Drag and Drop API

### Browser Compatibility
- Chrome (recommended)
- Firefox
- Safari
- Edge

### File Structure
```
Week plan/
├── index.html          # Main application file
└── README.md          # This file
```

### Data Structure

**Task Object**:
```javascript
{
  id: "unique-id",
  name: "Task Name",
  quadrant: "重要不紧急",
  color: "violet",
  section: "planning"
}
```

**Calendar Task Object**:
```javascript
{
  id: "unique-id",
  taskId: "parent-task-id",
  name: "Task Name",
  color: "violet",
  day: 0-6,           // 0 = Sunday
  hour: 0-15,         // 0 = 7 AM
  half: 0-1,          // 0 = first 30min, 1 = second 30min
  duration: 1-2       // 1 = 30min, 2 = 60min
}
```

## Design Credits

This application is based on a custom Figma design with the following components:
- Task Component (4 states)
- Accordion Component (3 states)
- Drawer Component (2 modes)
- Calendar View

## Future Enhancements

Potential features for future versions:
- Task descriptions/notes
- Due dates and reminders
- Task priorities
- Recurring tasks
- Export/Import functionality
- Multiple week views
- Task completion tracking
- Analytics and insights
- Mobile responsive design
- Dark mode

## License

This project is open source and available for personal and commercial use.

## Support

For issues, questions, or suggestions, please refer to the project documentation or contact the development team.

---

Built with ❤️ using modern web technologies

