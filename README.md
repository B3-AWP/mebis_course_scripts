# mebis_course_scripts
Scripts to improve the user experience in the mebis learning platform.

## Scripts

### main.html
For courses with **OneTopic format** (tab-based). Insert into a text block.

**Features:**
- Logo height reduced
- Activity separators hidden
- Padding after activities removed
- Border radius from alt-content images removed
- Chevron-down icons removed
- Active tab marker removed
- Sticky tab navigation (desktop/tablet only)
- Scroll-padding fix for anchor links
- Styling for optional items (green tag + border)
- Styling for mandatory items (red tag + border, turns green when completed)
- Heading styling for checklist headings
- Button text in white for primary buttons
- Smooth scroll to content area on page load
- "Next section" button href copy helper

### filter_grid_layout.html
For courses with **Tiles format** (grid/kachel layout). Insert into a text block.

**Features:**
- Dynamic filter buttons generated from first character of each tile title (e.g. `1`, `2`, `3`, `P`)
- Button sorting: numbers first (ascending), then letters (alphabetical)
- "Alle" button to show all tiles
- Group headers inserted between tile groups in "Alle" view (e.g. "1 FRONTEND", "2 PHP")
- Course index (left sidebar navigation) filtered in sync with tile filter
- Old Moodle filter buttons and filter icon removed

### knowledge_base_chapter_edit.html
For **Moodle Book** editing view. Insert into a text block.

**Features:**
- Full chapter names shown (text-truncate removed)
- Table of Contents block width increased by 60%
- Font size scaled down for text and icons
- List item vertical spacing fixed
- Icon alignment and padding fixes
- Edit icons moved below chapter title for better visibility

## Instructions
1. Open mebis course
2. Open block bar on the right
3. Add a new text block
4. In the Tools -> Source code section, select
![grafik](https://github.com/user-attachments/assets/c66dbe7b-9c07-4552-81bd-11c947de332e)
5. Insert source code from the desired HTML file
![grafik](https://github.com/user-attachments/assets/48894524-62a3-4cf9-8292-523a68cea494)
6. Save changes
