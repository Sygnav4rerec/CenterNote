# Centered Notes - Distraction-Free Notes App

## Overview

Centered Notes is a minimalist, distraction-free notes application designed to provide a calm writing experience with zero visual noise. The app features a unique centered input design where the text editor remains vertically centered above a bottom toolbar, with a history feed that scrolls upward when new lines are committed. The application prioritizes keyboard-driven workflows, inline editing capabilities, and local persistence while maintaining a clean, dark aesthetic.

The core philosophy centers around removing friction during note-taking and meta-cognitive journaling by keeping the cursor visually centered and eliminating unnecessary chrome or navigation elements.

## User Preferences

Preferred communication style: Simple, everyday language.

## System Architecture

### Frontend Architecture
The application is built as a single-page application using vanilla HTML, CSS, and JavaScript with no external frameworks or dependencies. This architectural decision prioritizes simplicity, fast loading times, and zero setup requirements.

**Layout Design:**
- Grid-based layout with three main sections: scrolling history area, fixed center input, and bottom toolbar
- CSS Grid provides precise control over the centered input positioning
- Responsive design using CSS custom properties and clamp functions for scalability

**Component Structure:**
- Monospace contenteditable editor as the primary input mechanism
- History feed displaying previously committed lines with smooth scrolling animations
- Bottom glyph toolbar organized in three rows for easy symbol insertion
- Minimal top menu system without left navigation rails

### Data Management
**Local Persistence Strategy:**
- localStorage-based data persistence eliminates need for backend infrastructure
- Session-based storage allows for immediate data availability without network dependencies
- Export functionality provides .txt file generation for data portability

**State Management:**
- Simple JavaScript object model for managing application state
- Real-time updates between input, history, and toolbar interactions
- Inline editing system with double-click activation and blur/Enter saving

### User Interaction Model
**Keyboard-Driven Workflow:**
- Enter key commits current line to history and creates new input line
- Escape key cancels inline editing operations
- Font size controls via keyboard shortcuts
- Help dialog system for discoverability

**Editing Features:**
- Contenteditable-based input for rich text handling
- Inline editing of historical entries via double-click activation
- Glyph insertion at current caret position
- Smooth scrolling animations for visual continuity

## External Dependencies

The application is designed with zero external dependencies to maintain simplicity and eliminate potential points of failure:

**Runtime Dependencies:** None - Pure vanilla web technologies
**Build Tools:** None - Direct HTML file execution
**Fonts:** System fonts only (ui-sans-serif, ui-monospace fallback chains)
**Icons/Assets:** Unicode glyphs and symbols (no external icon libraries)
**Storage:** Browser localStorage API (no external database)
**Export:** Browser File API for download functionality

This dependency-free architecture ensures the application can run in any modern web browser without internet connectivity after initial load, supporting the distraction-free philosophy by eliminating external service interruptions.