# Habit Tracker - Project Guidelines

## 📋 Project Overview

A web application to help users build positive habits by tracking daily progress, viewing streaks, and analyzing patterns over time.

---

## 🎯 Core Features (MVP)

### Phase 1: Foundation
- [ ] **Add Habits** - Create new habits with name, description, and frequency
- [ ] **Daily Tracking** - Mark habits as complete/incomplete for each day
- [ ] **Habit List** - View all habits with current status
- [ ] **Persistence** - Save data to localStorage (or database later)

### Phase 2: Enhancement
- [ ] **Streak Counter** - Track consecutive days completed
- [ ] **Progress Dashboard** - Visual overview of completion rates
- [ ] **Habit Details** - View history and statistics for each habit
- [ ] **Edit/Delete** - Modify or remove habits

### Phase 3: Advanced
- [ ] **Charts & Analytics** - Weekly/monthly completion graphs
- [ ] **Reminders** - Time-based notifications
- [ ] **Categories** - Organize habits by type (health, learning, fitness)
- [ ] **Export Data** - Download habits and statistics

---

## 🏗️ Project Structure

```
HabbitTracker/
├── index.html              # Main entry point
├── README.md               # This file
├── css/
│   ├── styles.css          # Main stylesheet
│   └── responsive.css      # Mobile/responsive styles
├── js/
│   ├── app.js              # Main application logic
│   ├── habitController.js  # Habit management logic
│   ├── storageManager.js   # Data persistence
│   └── utils.js            # Helper functions
├── Controller/
│   ├── HabitManager.js     # Business logic for habits
│   ├── DataManager.js      # Data operations
│   └── UIManager.js        # UI updates
├── Pages/
│   ├── dashboard.html      # Dashboard view
│   ├── habits.html         # Habits list view
│   ├── statistics.html     # Stats/analytics view
│   └── settings.html       # Settings page
└── assets/
    ├── icons/              # SVG icons
    └── images/             # Images
```

---

## 🔧 Technical Stack

| Layer | Technology |
|-------|-----------|
| **Frontend** | HTML5, CSS3, Vanilla JavaScript |
| **Storage** | localStorage (Phase 1) → IndexedDB/Database (Phase 2) |
| **Architecture** | MVC Pattern |
| **Styling** | CSS Grid/Flexbox, Responsive Design |
| **Version Control** | Git |

---

## 💾 Data Model

### Habit Object
```javascript
{
  id: "uuid-string",
  name: "Morning Exercise",
  description: "30 minutes workout",
  frequency: "daily",           // daily, weekly, etc.
  color: "#FF6B6B",
  createdAt: "2026-05-13",
  completedDates: ["2026-05-13", "2026-05-12"],
  streak: 2,
  lastCompleted: "2026-05-13"
}
```

### Completion Log
```javascript
{
  id: "uuid-string",
  habitId: "habit-uuid",
  date: "2026-05-13",
  completed: true,
  notes: "Optional notes"
}
```

---

## 🚀 Development Phases

### **Phase 1: MVP (Week 1-2)**
- Create basic UI layout
- Implement add habit functionality
- Daily tracking system
- localStorage integration
- Habit list display

### **Phase 2: Core Features (Week 3-4)**
- Streak calculation
- Edit/delete habits
- Basic statistics
- Dashboard view
- Responsive design

### **Phase 3: Polish & Advanced (Week 5+)**
- Charts and graphs
- Categories system
- Data export
- Advanced filtering
- Dark mode

---

## 📋 Development Checklist

### UI/UX
- [ ] Design mockups/wireframes
- [ ] Create responsive layouts
- [ ] Plan color scheme and typography
- [ ] Design icons for habits

### JavaScript Logic
- [ ] Habit CRUD operations
- [ ] Streak calculation algorithm
- [ ] Completion tracking logic
- [ ] Data validation

### Storage
- [ ] localStorage implementation
- [ ] Data export/import
- [ ] Backup mechanism

### Testing
- [ ] Unit tests for logic
- [ ] Manual UI testing
- [ ] Mobile responsiveness testing
- [ ] Cross-browser compatibility

---

## 🎨 UI/UX Best Practices

1. **Clear Visual Hierarchy** - Make it obvious what habits need attention today
2. **Minimal Friction** - One-click habit completion
3. **Motivational Design** - Show streaks, progress, achievements
4. **Mobile-First** - Optimize for mobile usage (checking habits on phone)
5. **Accessible** - Proper colors, contrast, keyboard navigation
6. **Dark Mode** - Reduce eye strain for evening use

---

## 💡 Key Implementation Tips

### Streak Algorithm
```javascript
// Traverse backwards from today, count consecutive completed days
// Break streak if any day is missed
// Reset to 0 if broken
```

### Storage Strategy
```javascript
// Save to localStorage after each action
// Use JSON.stringify/parse for data
// Implement data versioning for migrations
```

### UI Updates
```javascript
// Re-render only affected components
// Use event delegation for dynamic elements
// Update streaks in real-time
```

---

## 🔍 File Responsibilities

| File | Purpose |
|------|---------|
| **index.html** | Main page structure |
| **app.js** | Application initialization & routing |
| **HabitManager.js** | Business logic for habits |
| **DataManager.js** | CRUD operations & persistence |
| **UIManager.js** | DOM manipulation & rendering |
| **utils.js** | Date helpers, validators, utilities |

---

## 🌐 Sample Features Timeline

```
Week 1: Foundation
└─ Add habit, list habits, mark complete/incomplete

Week 2: Persistence
└─ Save to localStorage, load on page refresh

Week 3: Streaks
└─ Calculate and display streaks

Week 4: Dashboard
└─ Overview page with statistics

Week 5: Polish
└─ UI improvements, animations, responsiveness
```

---

## 📱 Key Metrics to Track

- **Completion Rate** - % of habits completed per day
- **Longest Streak** - Best consecutive days for each habit
- **Current Streak** - Active streak counter
- **Weekly Stats** - Overview of the week
- **Total Habits** - Active habit count

---

## 🚦 Getting Started

1. **Plan** - Sketch UI mockups and plan the data structure
2. **Build HTML** - Create static page structure
3. **Style** - Add CSS for layout and design
4. **Script** - Implement JavaScript logic incrementally
5. **Test** - Manual testing across devices and browsers
6. **Optimize** - Performance, accessibility, UX

---

## 📚 Learning Resources

- JavaScript Date manipulation
- localStorage API
- MVC architecture patterns
- CSS Grid & Flexbox
- Responsive design principles

---

## ✅ Success Criteria

- [x] Users can add habits
- [x] Users can track daily completion
- [x] Data persists between sessions
- [x] Streaks are calculated correctly
- [x] UI is mobile-responsive
- [x] No bugs on first use

---

## 📝 Next Steps

1. Create wireframes for the main views
2. Set up folder structure and starter files
3. Implement Phase 1 features
4. Test thoroughly before moving to Phase 2

Good luck building! 🎯
