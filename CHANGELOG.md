# 🚀 OneTouch Notes Pro AI – Changelog

All notable changes to this project will be documented in this file.

---

# [4.0.0] - Major Architectural Upgrade

## 🔥 Overview

Version 4.0.0 is a complete architectural redesign of OneTouch.

This release introduces:

- AI integration
- GitHub Gist cloud sync
- Subcategory-based data model
- Settings system
- Help documentation
- Schema migration logic
- UI/UX overhaul
- Responsive redesign

This is a foundational release and not a minor update.

---

# 🧱 Core Architecture Changes

## 🔄 Data Model Redesign (Breaking Change)

### OLD (v3.17)
- `categories = []`
- `sentences = { categoryName: [...] }`
- Sentences belonged directly to categories

### NEW (v4.0)
- `categories = [{ name, subcategories: [{ name, sentences: [] }] }]`
- Sentences now belong to subcategories
- Every category must contain at least one subcategory

### Added:
- Automatic schema detection
- Automatic migration from old storage format
- Self-healing logic (ensures at least one subcategory exists)
- Removed legacy `sentences` object

This is the largest structural change in the project.

---

# 🆕 Added

## 📁 Subcategory System
- Add subcategory
- Rename subcategory
- Delete subcategory
- Drag & drop subcategories
- Scrollable independent subcategory column
- Selected state styling
- Subcategory move/copy modal

---

## 🔀 Subcategory Move/Copy Modal
- When dragging subcategory to another category:
  - Prompt: Move or Copy?
  - Move option
  - Copy option
  - Cancel option

---

## 🤖 Full AI Integration

### AI Modal
- Standalone AI Helper window
- Output box with copy button
- AI provider label display

### AI Inside Add Note Modal
- Split view layout
- Make it better
- Grammar correct
- Custom prompt
- Rewrite suggestion
- Apply suggestion
- Disregard suggestion

### AI Inside Edit Modal
- Same split AI system
- Inline editing workflow
- Smart suggestion handling

---

## ☁️ Cloud Sync System (GitHub Gist)

- GitHub Personal Access Token input
- Gist ID management
- Unified Sync button
- Save credentials system
- Sync success toast
- Sync error toast
- Status indicator
- Backup reminder system

---

## 🛟 Backup Reminder System
- Reminder interval slider (1–15 days)
- Configurable interval
- Dedicated reminder modal
- UI feedback

---

## 💾 Local Backup System (Improved)
- JSON export backup
- JSON restore
- Integrated inside Sync Settings tab

---

## ⚙️ Settings System (New Architecture)

### Multi-Tab Settings Modal:
- Sync Settings
- Appearance
- AI Helper
- Help

### Features:
- Sidebar navigation
- Active tab styling
- Scrollable settings body
- Close button repositioned

---

## 📖 Help Section (New)

Added full in-app documentation:

- How to get GitHub token
- How to get Hugging Face API key
- How to get OpenAI API key
- Step-by-step instructions
- External links
- Security warnings

---

## 🎨 Appearance Customization

- Background image grid
- Custom background support
- Background deletion
- Selected tile highlighting
- Blur slider (0–20px)
- Real-time blur preview

---

## 🔁 Copy / Edit Interaction Mode

- Segmented toggle
- Animated slider
- Default mode: Copy
- Switchable edit mode
- State-driven interaction behavior

---

## 🧠 Undo System

- Undo deletion toast
- Countdown timer display
- Restore capability
- Auto-hide animation

---

## 🔔 Toast Notification System

- Sync success
- Sync error
- Non-intrusive UI
- Smooth animation

---

## 🔄 Move System (Enhanced)

- Move note to another subcategory
- Slide-in animations
- Back navigation
- Clean UI transitions

---

## 🎛 Top Control Bar (Redesigned)

Centralized UI controls:
- Add Note
- AI Helper
- Copy/Edit toggle
- Expand toggle
- Search input
- Sync button
- Settings button

---

## 🔍 Search Improvements

- Searches across subcategories
- Dynamic result rendering
- Works with expanded and collapsed blocks
- Respects heading format

---

## ✏️ Add Note Modal Redesign

- Split layout with AI
- Large textarea
- Clean input fields
- Better spacing
- Improved save workflow

---

## 📝 Edit Modal Redesign

- Split AI view
- ZWSP (zero-width space) handling for colon logic
- Smart heading detection
- Improved UX flow

---

## 🎭 UI & Styling Improvements

- Glassmorphism layout
- Sticky sidebar
- Dual-column sidebar
- Scroll indicators
- Drag visual feedback
- Modern modal styling
- Rounded corners everywhere
- Shadow depth improvements

---

## 📱 Responsiveness Improvements

- Improved mobile layout
- Top control bar wrapping
- Sidebar stacks on small screens
- Modal responsive scaling
- Better search layout on small screens

---

# 🔄 Changed

- Title renamed to **OneTouch Notes Pro AI**
- Background handling redesigned (local image support)
- Removed bottom backup panel
- Removed inline add form
- Removed old schema logic
- Removed legacy overlay behavior
- Expanded animation system
- Improved CSS structure
- Reduced inline style dependencies

---

# ❌ Removed

- Old `sentences` storage object
- Inline Add Sentence form
- Bottom layout backup section
- Standalone toggle container
- Standalone search container
- Legacy modal styling
- Basic popup layout

---

# 🛠 Internal Improvements

- Automatic schema migration system
- Data validation guard
- Modular AI execution functions
- Unified sync handler
- Cleaner state management
- Reduced redundant DOM operations
- Organized CSS sections
- Better drag event isolation
- Zero-width space escape logic for heading parsing
- Self-healing data structure logic

---

# [3.17] - Previous Stable Version

- Category-only data model
- LocalStorage persistence
- Manual backup & restore
- Basic modal editing
- Expand toggle
- Search feature
- Drag & drop notes
- No AI
- No subcategories
- No cloud sync
- No schema migration
- No settings system

---
