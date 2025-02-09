# Changelog - Mood Tracker  

## [1.1.0] - YYYY-MM-DD  
### 🚀 New Features  
#### 🎹 Keyboard Shortcuts for Mood Rating  
- Users can now rate their mood using **keyboard shortcuts (0-9)**.  
- Pressing `0` sets the mood rating to **10**, while `1-9` correspond to ratings **1 through 9**.  
- This feature activates when a day is selected, and the popup is displayed.  

#### 🔘 Toggle Rating Popup Button  
- A new button has been added to **enable or disable** the rating popup.  
- Positioned at the **bottom-left corner** of the screen.  

#### 🎭 Rating Popup Animation  
- The rating popup now features a **bobbing animation** (`@keyframes bobbing`) for a smoother visual effect.  

#### 🖱️ Rating Hover Popup  
- A new **hover popup** displays the **mood rating** when hovering over a day.  
- Example: `"5/10"` if a mood has been set for that day.  
- This feature can be enabled/disabled using the **toggle button**.  

---

### 🎨 UI/UX Improvements  
#### ✍️ Font Styling in Popup Buttons  
- Mood rating buttons now use **IBM Plex Mono (weight: 600)** for improved readability.  

#### 📍 Popup Positioning Adjustments  
- The **rating popup** has been repositioned for better alignment with the selected day.  

#### 🎨 Toggle Button Styling  
- The **toggle button** now visually matches the overall **app design**.  

---

### 🛠️ Code Changes  
#### ✨ JavaScript Enhancements  
- Introduced `selectedDay` to track the currently selected day for keyboard input.  
- Added **event listeners** for `keydown` to handle mood rating shortcuts.  
- Implemented **dynamic logic** for enabling/disabling the rating popup.  

#### 🎞️ New CSS Animation  
- Introduced a **bobbing animation (`@keyframes bobbing`)** to the popup for a subtle motion effect.  

#### 🏗️ Dynamic Popup Creation  
- Added a **new `ratingPopup` element** to display the mood rating on hover.  
- The `ratingPopup` **follows the mouse movement** for better positioning.  

#### 🎛️ Toggle Button Logic  
- Implemented logic to toggle `popupEnabled` state and dynamically update the button text.  

---

### 🐛 Bug Fixes  
#### 🏁 Popup Display Logic  
- Fixed an issue where the **popup would not close properly** when clicking outside of it.  
- Improved logic for **displaying and hiding** the popup based on user interactions.  

#### ⏳ Future Day Interaction  
- Ensured that **future days remain non-interactive** (`pointer-events: none`) to prevent premature mood ratings.  

---

## 📌 Summary  
The **1.1.0 update** brings several **new features and refinements**, including:  
- **Keyboard shortcuts** for mood rating  
- **A toggle button** for enabling/disabling the rating popup  
- **A hover popup** to display mood ratings  
- **Improved animations, UI adjustments, and code enhancements**  

This release makes **Mood Tracker** more intuitive, visually engaging, and user-friendly. Stay tuned for future updates! 🚀  
