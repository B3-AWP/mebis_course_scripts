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

**Filter & Navigation**
- Dynamic filter buttons generated from first character of each tile title (e.g. `1`, `2`, `3`, `P`)
- Button sorting: numbers first (ascending), then letters (alphabetical)
- "Alle" button to show all tiles
- Group headers inserted between tile groups in "Alle" view (e.g. "1 FRONTEND", "2 PHP")
- Course index (left sidebar navigation) filtered in sync with tile filter
- Old Moodle filter buttons and filter icon removed

**Title & Prefix Cleanup**
- Prefix removed from tile titles (h3): `PREFIX-1 Title` → `1 Title`
- Prefix removed from modal/section headings (h2)
- Prefix removed from activity titles in subtiles (h5): `1.2 Pflicht: Title` → `Title`

**Subtile Layout (Quadrat → Horizontal)**
- Subtiles rendered as full-width horizontal rows instead of square tiles
- Activity icon left-aligned, title in the middle, completion status on the right
- Background image overlay hidden
- Page width increased to 1280px

**Mandatory Task Badge**
- Activities containing "Pflicht" in their title get a red "Pflicht" badge
- Badge turns green when the activity is marked as completed

**Completion Status Labels**
- Each subtile shows a completion label: `Erledigt` (green), `Offen` (grey), or `Als erledigt markieren` (grey dashed, for manual completion)
- Manual completion toggle button styled as clickable (dashed border, hover state)
- Responsive: label text hidden on viewports below 540px, only checkmark shown

**Dynamic Phases**
- Phase labels (paragraphs starting with "Phase N") act as section dividers
- Each phase shows a status dot and progress counter (e.g. `3/5`)
- Status: `done` (green), `active` (grey with pen icon), `todo` (grey, faded), `empty` (dashed)
- Subtiles within a phase get a colored left border matching their phase status
- Phase-specific icons for active state (Phase 3 → clipboard, Phase 4 → lock)
- Spacing added above each phase except the first

**Live Updates**
- MutationObserver watches the page content for DOM changes (e.g. tile/modal opens)
- All functions (prefixes, badges, completion labels, phases) re-run on relevant DOM mutations
- Debounce guard prevents update loops

### knowledge_base_chapter_edit.html
For **Moodle Book** editing view. Insert into a text block.

**Features:**
- Full chapter names shown (text-truncate removed)
- Table of Contents block width increased by 60%
- Font size scaled down for text and icons
- List item vertical spacing fixed
- Icon alignment and padding fixes
- Edit icons moved below chapter title for better visibility

### assignment_redirect.html
For **Assignments**. Insert into the assignment description field (not a course text block).

**Features:**
- After submitting an assignment, redirects directly to the course section instead of showing the assignment again
- Extracts section URL from breadcrumb navigation (2nd entry, must be `/course/section.php`)
- Uses `sessionStorage` to bridge Moodle's server-side redirect: URL is stored on submit click, redirect fires on the next page load when no submit button is present (= submission accepted)
- No redirect on failed submissions (form with submit button still visible)
- Clears stored URL when cancel button is clicked
- 300ms delay before checking for submit button, to allow AJAX-rendered forms to load

## Instructions
1. Open mebis course
2. Open block bar on the right
3. Add a new text block
4. In the Tools -> Source code section, select
![grafik](https://github.com/user-attachments/assets/c66dbe7b-9c07-4552-81bd-11c947de332e)
5. Insert source code from the desired HTML file
![grafik](https://github.com/user-attachments/assets/48894524-62a3-4cf9-8292-523a68cea494)
6. Save changes
