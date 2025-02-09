# Changelog - Mood Tracker  

## [1.2.0] - 2025-02-09  

### 🚀 New Features  
#### 📅 Year Selection Dropdown  
- Added a **year selection dropdown** in the header to easily switch between different years (from **2020** to the current year).  
- Users can now view mood data for previous or future years, depending on availability.  

#### 📜 Historical Data Support  
- **Historical mood data** is now supported.  
- Days from previous years are marked as:  
  - **Historical Day**: A mood was recorded for that day.  
  - **Historical Empty**: No mood rating was recorded for that day.  
- Historical days are non-interactive (`pointer-events: none`) to preserve past data integrity.  

#### 🔄 Dynamic Grid Update  
- The mood grid now dynamically updates when the user changes the selected year from the dropdown.  
- Mood data is stored and retrieved based on the selected year (e.g., `moodData_2023`).  

---

### 🎨 UI/UX Improvements  
#### 🖥️ Header Layout  
- The header now features a **container** that aligns the **title** and **year dropdown** horizontally.  
- Improved layout and spacing for a cleaner design.  

#### 🏛️ Historical Day Styling  
- Introduced new CSS classes for historical days:  
  - `.historical-day` for days with mood data.  
  - `.historical-empty` for days without mood data.  
- These days are styled with a **lighter background** for better differentiation.  

#### 🕰️ Future Day Styling  
- Future days are now visually distinct with a **lighter background** and are **non-interactive**.  

#### 📅 Current Day Highlight  
- The **current day** is highlighted with a **white background** for easy identification.  

---

### 🛠️ Code Changes  
#### 🔄 Year Selection Logic  
- Introduced a **year selection dropdown** with options ranging from **2020** to the current year.  
- The selected year is tracked in `selectedYear`, and the grid updates accordingly.  

#### 💾 Local Storage Key Update  
- Mood data is now stored with year-specific keys (e.g., `moodData_2023`) in **localStorage**.  
- This ensures data is segmented by year.  

#### 🔄 Grid Update Function  
- Refactored the grid creation logic into a reusable function, **updateGrid()**, called upon page load or year change.  

#### 🏛️ Historical Day Handling  
- Added logic to correctly apply the **historical-day** or **historical-empty** class based on the year.  

#### 🕰️ Future Day Handling  
- Improved the logic to identify and style **future days** appropriately.  

---

### 🐛 Bug Fixes  
#### 🖱️ Popup Positioning  
- Fixed an issue where the popup was misaligned with the selected day.  
- The popup now properly aligns with the selected day when clicked.  

#### ⏳ Future Day Interaction  
- Ensured that future days remain **non-interactive** (`pointer-events: none`) to avoid accidental mood ratings.  

#### 🏛️ Historical Data Consistency  
- Fixed an issue where historical days were incorrectly styled or could be interacted with.  
- Historical days are now consistently styled and non-interactive.  

---

## 📌 Summary  
The **1.2.0 update** brings exciting new features, including:  
- A **year selection dropdown** to track mood data across multiple years.  
- **Historical data support** to view past entries with updated styling.  
- **Dynamic grid updates** when changing years.  

This release makes **Mood Tracker** even more powerful by enabling users to explore their mood history over multiple years while improving the overall user interface. Stay tuned for more! 🚀 

---

## [1.1.0] - 2025-02-07  
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
