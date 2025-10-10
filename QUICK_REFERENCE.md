# Quick Reference - New Features

## 🎯 What's New in v2.1

### 1. Undo Button ↩️
**When:** Drag task to "已完成"  
**What:** Toast shows with "撤销" button  
**Duration:** 5 seconds to undo  
**Action:** Click "撤销" to restore task  

---

### 2. Full Screen Height 📏
**All sections:** Now fill vertical space properly  
**Scroll:** Content scrolls when overflow  
**Responsive:** Adapts to window size  

---

### 3. Add Task Button ➕
**Location:** Inside "本周要务" section  
**Style:** Same as main button  
**Function:** Opens task creation drawer  

---

### 4. Quadrant Groups 📊
**Sections:** 计划中, 本周要务, 已完成  
**Groups:**
- 重要不紧急
- 重要紧急  
- 不重要但紧急
- 不重要不紧急

---

### 5. Calendar Colors 🎨
**Weekends:** Light gray  
**Weekdays:** White  
**All rows:** Consistent colors  

---

## 🚀 Quick Actions

| Action | How To |
|--------|--------|
| Undo finished task | Drag to 已完成 → Click 撤销 |
| Add task to 本周要务 | Open section → Click 添加任务 |
| View by priority | Check quadrant groups |
| Scroll content | Use mouse wheel in sections |

---

## 💡 Pro Tips

1. **Undo Window**: You have 5 seconds to undo
2. **Section Height**: One section open = full height
3. **Quadrants**: Empty groups hidden automatically
4. **Colors**: Weekends are visually distinct

---

## 🎨 Visual Guide

```
Left Panel Structure:
┌────────────────────┐
│ 计划中 (5) [v]     │ ← Click to expand
├────────────────────┤
│ [添加任务]         │
│                    │
│ 重要不紧急         │
│  • Task 1          │
│  • Task 2          │
│                    │
│ 重要紧急           │
│  • Task 3          │
│    ↓               │
│  (Scrolls)         │
│                    │
└────────────────────┘
│ 本周要务 (3) [>]   │ ← Collapsed
├────────────────────┤
│ 已完成 (2) [>]     │ ← Collapsed
└────────────────────┘
```

```
Toast with Undo:
┌──────────────────────────────┐
│ 任务已移至已完成  [撤销]      │
└──────────────────────────────┘
     ↑              ↑
   Message      Click to undo
```

---

## 📱 Keyboard & Mouse

- **ESC**: Close drawer
- **Click**: Open/close section
- **Drag**: Move tasks
- **Right-click**: Delete (calendar tasks)
- **Double-click**: (removed from accordion tasks)

---

## ✅ All Features Working

- ✓ Create tasks with quadrants
- ✓ Edit tasks (updates all instances)
- ✓ Delete tasks (with confirmation)
- ✓ Drag between sections (with hover feedback)
- ✓ Drag to calendar (max 2 per slot)
- ✓ Undo moves to finished
- ✓ Quadrant organization
- ✓ Full screen layout
- ✓ Data persistence

---

## 🎉 Ready to Use!

Open `index.html` and enjoy your polished task manager!

All features are:
- ✨ Working perfectly
- 🎨 Beautifully designed  
- 🚀 Smooth & responsive
- 💾 Auto-saving

Happy planning! 📅✨

