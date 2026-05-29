# EduAI - Test Cases

## Test Suite Overview
Comprehensive test cases for the EduAI AI-powered learning platform covering authentication, dashboard, syllabus, practice, analytics, and reports modules.

---

## 1. AUTHENTICATION & ENROLLMENT

### TC-AUTH-001: Landing Page Display
**Objective:** Verify landing page loads correctly with all UI elements
- **Steps:**
  1. Open EduAI application
  2. Observe landing page
- **Expected Result:** 
  - Landing page displays with EduAI logo and tagline
  - Two CTA buttons visible: "Login to your account" and "Create new account"
  - Feature pills display correctly (Full Syllabus, AI Questions, Analytics, Progress Tracking)
  - Demo credentials hint visible
- **Status:** ⚪ Ready

### TC-AUTH-002: Login with Valid Credentials
**Objective:** Verify user can login with correct email and password
- **Steps:**
  1. Click "Login to your account"
  2. Enter email: demo@eduai.in
  3. Enter password: demo123
  4. Click "Sign In"
- **Expected Result:**
  - Login form validates input
  - User is authenticated
  - Dashboard loads successfully
  - User profile displays in sidebar
- **Status:** ⚪ Ready

### TC-AUTH-003: Login with Invalid Email
**Objective:** Verify error handling for invalid email format
- **Steps:**
  1. Navigate to login screen
  2. Enter email: invalidemailformat
  3. Enter password: demo123
  4. Click "Sign In"
- **Expected Result:**
  - Error message displayed: "Invalid email format"
  - User not authenticated
  - Remains on login screen
- **Status:** ⚪ Ready

### TC-AUTH-004: Login with Incorrect Password
**Objective:** Verify error handling for wrong password
- **Steps:**
  1. Navigate to login screen
  2. Enter email: demo@eduai.in
  3. Enter password: wrongpassword
  4. Click "Sign In"
- **Expected Result:**
  - Error message displayed: "Invalid credentials"
  - User not authenticated
  - Remains on login screen
- **Status:** ⚪ Ready

### TC-AUTH-005: Demo Credentials Auto-fill
**Objective:** Verify demo credentials button populates login fields
- **Steps:**
  1. Navigate to login screen
  2. Click "Use demo credentials" button
  3. Observe email and password fields
- **Expected Result:**
  - Email field auto-filled with: demo@eduai.in
  - Password field auto-filled with: demo123
  - Both fields are ready for submission
- **Status:** ⚪ Ready

### TC-AUTH-006: Registration Step 1 - Avatar Selection
**Objective:** Verify avatar selection in registration
- **Steps:**
  1. Click "Create new account"
  2. Observe avatar grid
  3. Click on different avatar (e.g., 🐯)
- **Expected Result:**
  - Avatar button shows visual feedback (border/background change)
  - Previous avatar deselected
  - New avatar marked as selected
- **Status:** ⚪ Ready

### TC-AUTH-007: Registration Step 1 - Missing Name
**Objective:** Verify validation for required name field
- **Steps:**
  1. Navigate to registration step 1
  2. Leave name field empty
  3. Enter email: student@example.com
  4. Enter password: securepass123
  5. Click "Continue"
- **Expected Result:**
  - Error message: "Name is required"
  - Form not submitted
- **Status:** ⚪ Ready

### TC-AUTH-008: Registration Step 1 - Password Strength Indicator
**Objective:** Verify password strength meter displays correctly
- **Steps:**
  1. Navigate to registration step 1
  2. Focus on password field
  3. Type: "123" (weak)
  4. Observe strength bar
  5. Clear and type: "MyP@ssw0rd123" (strong)
- **Expected Result:**
  - Weak password shows red bar
  - Strong password shows green bar
  - Strength label updates accordingly
- **Status:** ⚪ Ready

### TC-AUTH-009: Registration Step 2 - Board Selection
**Objective:** Verify board selection in registration
- **Steps:**
  1. Complete registration step 1
  2. Navigate to step 2
  3. Click on board option: "CBSE"
- **Expected Result:**
  - Board button highlights with jade color
  - Class dropdown becomes enabled
  - Step indicator updates to show progress
- **Status:** ⚪ Ready

### TC-AUTH-010: Registration Step 2 - Class Selection
**Objective:** Verify class selection after board selection
- **Steps:**
  1. Complete board selection (TC-AUTH-009)
  2. Observe class grid
  3. Click class "10"
- **Expected Result:**
  - Class button highlights
  - Syllabus preview appears below
  - Subjects for Class 10 displayed
- **Status:** ⚪ Ready

### TC-AUTH-011: Registration Step 3 - Profile Review
**Objective:** Verify registration confirmation screen displays correct data
- **Steps:**
  1. Complete steps 1-2 of registration
  2. Click "Continue" on step 2
  3. Observe step 3 profile summary
- **Expected Result:**
  - Avatar displayed correctly
  - Name shows entered value
  - Email shows entered value
  - Board and class display selected values
  - Subjects listed for that class
- **Status:** ⚪ Ready

### TC-AUTH-012: Complete Registration
**Objective:** Verify successful account creation
- **Steps:**
  1. Complete registration steps 1-3 with all valid data
  2. Click "🚀 Create Account & Start!"
- **Expected Result:**
  - Account created successfully
  - Dashboard page loads
  - Sidebar displays student info
  - Progress bar visible
  - All navigation menu items accessible
- **Status:** ⚪ Ready

---

## 2. DASHBOARD PAGE

### TC-DASH-001: Dashboard Layout
**Objective:** Verify dashboard loads with all sections
- **Steps:**
  1. Login to application
  2. Verify Dashboard is active page
  3. Observe page layout
- **Expected Result:**
  - Greeting message displays with current date
  - KPI cards visible (4 columns)
  - Subject Progress card on left
  - Performance Overview card on right
  - Three cards below: Needs Revision, Strong Areas, Recent Tests
- **Status:** ⚪ Ready

### TC-DASH-002: KPI Cards Display
**Objective:** Verify KPI metrics display correctly
- **Steps:**
  1. View dashboard
  2. Observe KPI row with 4 cards
- **Expected Result:**
  - Cards show: Accuracy %, Chapters Done, Avg Score, Quiz Count
  - Each card has an icon
  - Numbers animate with count-up effect
  - Hover effect applies (card moves up slightly)
- **Status:** ⚪ Ready

### TC-DASH-003: Subject Progress Chart
**Objective:** Verify subject progress displays with progress bars
- **Steps:**
  1. View dashboard
  2. Observe Subject Progress card
- **Expected Result:**
  - Each subject listed (e.g., Math, Science, English)
  - Progress bar for each subject
  - Percentage displayed on right
  - Colors vary by subject
- **Status:** ⚪ Ready

### TC-DASH-004: Performance Overview Radial Charts
**Objective:** Verify radial/circular charts display
- **Steps:**
  1. View dashboard
  2. Observe Performance Overview card
- **Expected Result:**
  - Multiple circular progress charts visible
  - Each chart shows percentage
  - Charts are animated
- **Status:** ⚪ Ready

### TC-DASH-005: Weak Areas List
**Objective:** Verify topics needing revision display
- **Steps:**
  1. View dashboard
  2. Look at "⚠️ Needs Revision" card
- **Expected Result:**
  - List of chapters/topics showing
  - Each item shows topic name
  - Visual indicator (red/coral color)
- **Status:** ⚪ Ready

### TC-DASH-006: Strong Areas List
**Objective:** Verify strong topics display
- **Steps:**
  1. View dashboard
  2. Look at "💪 Strong Areas" card
- **Expected Result:**
  - List of mastered chapters/topics
  - Each item shows topic name
  - Visual indicator (green/jade color)
- **Status:** ⚪ Ready

### TC-DASH-007: Recent Tests List
**Objective:** Verify recent test attempts display
- **Steps:**
  1. View dashboard
  2. Look at "🕐 Recent Tests" card
- **Expected Result:**
  - Recent quiz/test attempts listed
  - Shows test name, date, score
  - Most recent appears first
- **Status:** ⚪ Ready

---

## 3. SYLLABUS PAGE

### TC-SYLAB-001: Syllabus Page Layout
**Objective:** Verify syllabus page loads correctly
- **Steps:**
  1. Login to application
  2. Click "Syllabus" in sidebar
  3. Observe page
- **Expected Result:**
  - Page title "Syllabus" displays
  - Subtitle shows "Class 10 · CBSE Board"
  - Subject tabs appear below header
  - Chapter accordion structure visible
- **Status:** ⚪ Ready

### TC-SYLAB-002: Subject Tab Switching
**Objective:** Verify switching between subjects works
- **Steps:**
  1. View Syllabus page
  2. Click on different subject tabs (e.g., "Physics", "Chemistry")
  3. Observe chapter list
- **Expected Result:**
  - Active tab highlights with jade background
  - Tab count shows number of chapters
  - Chapter list updates for selected subject
  - Smooth animation when switching
- **Status:** ⚪ Ready

### TC-SYLAB-003: Chapter Accordion Expand
**Objective:** Verify chapter details expand on click
- **Steps:**
  1. View Syllabus page
  2. Click on a chapter item
  3. Observe chapter body expand
- **Expected Result:**
  - Chapter expands to show content
  - Arrow icon rotates 180 degrees
  - Topics within chapter display
  - Body animates in smoothly
- **Status:** ⚪ Ready

### TC-SYLAB-004: Chapter Accordion Collapse
**Objective:** Verify expanded chapter collapses
- **Steps:**
  1. Expand a chapter (TC-SYLAB-003)
  2. Click chapter again
- **Expected Result:**
  - Chapter body hides
  - Arrow returns to original position
  - Smooth collapse animation
- **Status:** ⚪ Ready

### TC-SYLAB-005: Chapter Content Display
**Objective:** Verify chapter expanded content shows correctly
- **Steps:**
  1. Expand a chapter
  2. Observe chapter body content
- **Expected Result:**
  - Chapter number badge displays
  - Chapter name shows
  - Topics listed in two columns
  - Tags/concepts displayed
  - Estimated learning time shows (if applicable)
- **Status:** ⚪ Ready

---

## 4. PRACTICE CENTER

### TC-PRAC-001: Practice Page Load
**Objective:** Verify practice center loads with chapter selection
- **Steps:**
  1. Login to application
  2. Click "Practice" in sidebar
  3. Observe page layout
- **Expected Result:**
  - Page shows "Practice Center" title
  - Left panel with chapter list
  - Right panel for quiz display
  - Ready state shows statistics
- **Status:** ⚪ Ready

### TC-PRAC-002: Select Chapter for Practice
**Objective:** Verify chapter selection shows quiz ready state
- **Steps:**
  1. View Practice page
  2. Click on a chapter in left panel
- **Expected Result:**
  - Chapter highlights as selected
  - Right panel updates with "Ready to begin?" state
  - Quiz stats display (questions, topics)
  - "Start Quiz" button visible
- **Status:** ⚪ Ready

### TC-PRAC-003: Start Quiz
**Objective:** Verify quiz starts after clicking start button
- **Steps:**
  1. Select a chapter (TC-PRAC-002)
  2. Click "Start Quiz" button
- **Expected Result:**
  - Quiz interface loads
  - Progress bar appears at top
  - Question number displays (e.g., 1/10)
  - Question text displays
  - Answer options visible
- **Status:** ⚪ Ready

### TC-PRAC-004: Answer Question
**Objective:** Verify user can select answer option
- **Steps:**
  1. Start a quiz (TC-PRAC-003)
  2. Click on one of the answer options
- **Expected Result:**
  - Option highlights with jade border
  - Option background changes
  - Option becomes selected state
  - "Next" button enabled (if not auto-advance)
- **Status:** ⚪ Ready

### TC-PRAC-005: Incorrect Answer Feedback
**Objective:** Verify feedback for wrong answer
- **Steps:**
  1. Start quiz
  2. Select incorrect answer
  3. Observe feedback
- **Expected Result:**
  - Selected option shows coral/red border
  - Correct answer highlights in jade
  - Feedback message displays explanation
  - User cannot change answer
- **Status:** ⚪ Ready

### TC-PRAC-006: Correct Answer Feedback
**Objective:** Verify feedback for correct answer
- **Steps:**
  1. Start quiz
  2. Select correct answer
  3. Observe feedback
- **Expected Result:**
  - Selected option shows jade border
  - Option background highlights green
  - Success message or checkmark appears
  - Next question available
- **Status:** ⚪ Ready

### TC-PRAC-007: Quiz Progress Tracking
**Objective:** Verify progress bar updates during quiz
- **Steps:**
  1. Start a quiz (10 questions assumed)
  2. Answer questions and progress
  3. Observe progress bar
- **Expected Result:**
  - Progress bar fills as questions answered
  - Question counter updates (e.g., "2/10")
  - Visual animation on bar fill
- **Status:** ⚪ Ready

### TC-PRAC-008: Quiz Completion - Results Page
**Objective:** Verify results display after quiz completion
- **Steps:**
  1. Complete all quiz questions
  2. Observe results screen
- **Expected Result:**
  - Score displays prominently (large font)
  - Status badge shows (Excellent/Good/Average/Needs Work)
  - Background color matches performance level
  - Results breakdown available
- **Status:** ⚪ Ready

### TC-PRAC-009: Review Quiz Answers
**Objective:** Verify user can review answers after completion
- **Steps:**
  1. Complete quiz and view results
  2. Click "Review Answers" or similar button
- **Expected Result:**
  - Questions display with selected answer
  - Correct answer highlighted
  - Explanation visible for each question
  - Can navigate between questions
- **Status:** ⚪ Ready

### TC-PRAC-010: Retake Quiz
**Objective:** Verify user can retake quiz
- **Steps:**
  1. Complete quiz and view results
  2. Click "Retake Quiz" button
- **Expected Result:**
  - Quiz reloads with fresh questions
  - Progress bar resets
  - Previous answers not visible
  - First question displayed
- **Status:** ⚪ Ready

---

## 5. ANALYTICS PAGE

### TC-ANAL-001: Analytics Page Load
**Objective:** Verify analytics page loads with visualizations
- **Steps:**
  1. Login to application
  2. Click "Analytics" in sidebar
  3. Observe page
- **Expected Result:**
  - Page title "Analytics" displays
  - Multiple chart/visualization sections visible
  - Heatmap grid displays
  - Timeline charts visible
  - Filters or time period selector available
- **Status:** ⚪ Ready

### TC-ANAL-002: Heatmap Display
**Objective:** Verify activity heatmap displays correctly
- **Steps:**
  1. View Analytics page
  2. Observe heatmap grid
- **Expected Result:**
  - Grid of cells showing activity
  - Cells color-coded by intensity
  - Hover shows activity details
  - Legend displays color scale
  - Time period labels visible
- **Status:** ⚪ Ready

### TC-ANAL-003: Timeline Chart
**Objective:** Verify timeline/progress chart displays
- **Steps:**
  1. View Analytics page
  2. Look for timeline chart section
- **Expected Result:**
  - Timeline shows multiple chapters/topics
  - Horizontal bars show accuracy/speed metrics
  - Color coding distinguishes metrics
  - Numbers/percentages displayed
- **Status:** ⚪ Ready

### TC-ANAL-004: Performance By Subject
**Objective:** Verify subject-wise performance breakdown
- **Steps:**
  1. View Analytics page
  2. Locate subject performance section
- **Expected Result:**
  - Each subject listed with metrics
  - Accuracy percentage shown
  - Chapters completed indicator
  - Time spent visible
- **Status:** ⚪ Ready

### TC-ANAL-005: Time Period Filter
**Objective:** Verify analytics filter by time period
- **Steps:**
  1. View Analytics page
  2. Select different time period filter (Week/Month/All-time)
  3. Observe data update
- **Expected Result:**
  - Selected period highlights
  - Charts update with filtered data
  - Heatmap regenerates for period
  - All metrics recalculate
- **Status:** ⚪ Ready

---

## 6. REPORTS PAGE

### TC-REPORT-001: Reports Page Load
**Objective:** Verify reports page loads with report types
- **Steps:**
  1. Login to application
  2. Click "Reports" in sidebar
  3. Observe page
- **Expected Result:**
  - Page title "Reports" displays
  - Report type cards visible
  - Multiple report categories available
  - Report content area ready
- **Status:** ⚪ Ready

### TC-REPORT-002: Select Report Type
**Objective:** Verify report type selection updates content
- **Steps:**
  1. View Reports page
  2. Click on different report type card
- **Expected Result:**
  - Selected report type highlights
  - Report content updates
  - AI badge visible for AI-generated content
  - Report text loads
- **Status:** ⚪ Ready

### TC-REPORT-003: AI Performance Summary
**Objective:** Verify AI-generated performance report displays
- **Steps:**
  1. Navigate to Reports
  2. Select "Performance Summary" report type
  3. View report content
- **Expected Result:**
  - AI badge displays
  - Report shows subject-wise performance
  - Recommendations included
  - Typing animation for AI response (if applicable)
- **Status:** ⚪ Ready

### TC-REPORT-004: Weak Areas Report
**Objective:** Verify weak areas identified and reported
- **Steps:**
  1. Navigate to Reports
  2. Select "Weak Areas" or similar report
  3. View content
- **Expected Result:**
  - Topics where performance is low listed
  - Severity indicators shown
  - Recommendations for improvement
  - Related resources linked
- **Status:** ⚪ Ready

### TC-REPORT-005: Personalized Recommendations
**Objective:** Verify AI recommendations for improvement
- **Steps:**
  1. View any AI-generated report
  2. Observe recommendations section
- **Expected Result:**
  - Recommendations are personalized
  - Actionable steps provided
  - Topics to focus on listed
  - Estimated time to improvement shown
- **Status:** ⚪ Ready

---

## 7. SIDEBAR & NAVIGATION

### TC-NAV-001: Sidebar Display
**Objective:** Verify sidebar displays student information
- **Steps:**
  1. Login to application
  2. Observe sidebar
- **Expected Result:**
  - Logo and app name visible at top
  - Student avatar displays
  - Student name shows
  - Class and board display
  - Progress percentage visible
  - Progress bar with gradient
  - Chapter completion count shown
- **Status:** ⚪ Ready

### TC-NAV-002: Navigation Items Highlight
**Objective:** Verify active navigation item highlights
- **Steps:**
  1. View sidebar navigation
  2. Click on different pages
  3. Observe active state
- **Expected Result:**
  - Active item shows jade background
  - Active item shows jade dot indicator
  - Border color changes
  - Only one item active at a time
- **Status:** ⚪ Ready

### TC-NAV-003: User Menu Dropdown
**Objective:** Verify user menu opens and closes
- **Steps:**
  1. View sidebar footer
  2. Click user menu button
  3. Observe dropdown
- **Expected Result:**
  - Dropdown appears above menu
  - Menu options visible (Update Profile, Logout)
  - Click elsewhere closes menu
  - Chevron icon rotates
- **Status:** ⚪ Ready

### TC-NAV-004: Update Profile Modal
**Objective:** Verify update profile form opens
- **Steps:**
  1. Click user menu
  2. Click "Update Profile"
  3. Observe modal
- **Expected Result:**
  - Modal opens with fadeUp animation
  - Current profile data pre-filled
  - All fields editable
  - Save and Cancel buttons visible
- **Status:** ⚪ Ready

### TC-NAV-005: Save Profile Changes
**Objective:** Verify profile updates save correctly
- **Steps:**
  1. Open Update Profile modal (TC-NAV-004)
  2. Change name field
  3. Click "Save"
- **Expected Result:**
  - Modal closes
  - Sidebar updates with new name
  - Success message displays
  - Changes persist on page reload
- **Status:** ⚪ Ready

### TC-NAV-006: Logout Confirmation
**Objective:** Verify logout modal displays
- **Steps:**
  1. Click user menu
  2. Click "Logout"
  3. Observe confirmation modal
- **Expected Result:**
  - Modal appears with logout confirmation
  - Student summary displays
  - Progress saved message shown
  - "Cancel" and "Logout" buttons visible
- **Status:** ⚪ Ready

### TC-NAV-007: Confirm Logout
**Objective:** Verify successful logout
- **Steps:**
  1. Open logout confirmation (TC-NAV-006)
  2. Click "Logout" button
  3. Observe result
- **Expected Result:**
  - Modal closes
  - "See you soon!" success screen displays
  - After 3 seconds or manual click, returns to login
  - Session cleared
- **Status:** ⚪ Ready

---

## 8. UI/UX & RESPONSIVENESS

### TC-UX-001: Password Visibility Toggle
**Objective:** Verify password field visibility can be toggled
- **Steps:**
  1. Navigate to login or registration
  2. Focus on password field
  3. Click eye icon to show/hide
- **Expected Result:**
  - Password hides/shows correctly
  - Eye icon changes visual state
  - Text remains in field
- **Status:** ⚪ Ready

### TC-UX-002: Form Input Focus States
**Objective:** Verify form inputs show focus visual feedback
- **Steps:**
  1. View any form (login, registration, etc.)
  2. Click on input field
  3. Observe focus state
- **Expected Result:**
  - Input border highlights in jade
  - Background subtle change
  - Cursor visible in field
- **Status:** ⚪ Ready

### TC-UX-003: Animations Play Smoothly
**Objective:** Verify animations are smooth and not janky
- **Steps:**
  1. Navigate between pages
  2. Expand/collapse accordions
  3. Open/close modals
  4. Observe animation smoothness
- **Expected Result:**
  - Fade transitions smooth
  - Slide animations fluid
  - No stuttering or jumps
  - GPU acceleration utilized
- **Status:** ⚪ Ready

### TC-UX-004: Button Hover Effects
**Objective:** Verify hover effects on buttons
- **Steps:**
  1. Navigate to any page
  2. Hover over different buttons
  3. Observe hover state
- **Expected Result:**
  - Button moves up slightly
  - Color transitions smoothly
  - Box shadow increases
  - Cursor shows pointer
- **Status:** ⚪ Ready

### TC-UX-005: Card Hover Effects
**Objective:** Verify card hover effects
- **Steps:**
  1. View Dashboard or any card grid
  2. Hover over cards
  3. Observe effects
- **Expected Result:**
  - Card border highlights
  - Card shadow increases
  - Slight upward movement
  - Smooth transition
- **Status:** ⚪ Ready

### TC-UX-006: Scrollbar Styling
**Objective:** Verify custom scrollbars display correctly
- **Steps:**
  1. View a page with scrollable content
  2. Observe scrollbar
- **Expected Result:**
  - Scrollbar styled with theme colors
  - Thumb shows jade color when hovering
  - Track matches background
  - Width is 4px
- **Status:** ⚪ Ready

### TC-UX-007: Loading Spinner
**Objective:** Verify loading spinner displays during async operations
- **Steps:**
  1. Trigger an operation with loading state
  2. Observe spinner animation
- **Expected Result:**
  - Spinner rotates smoothly
  - Jade color with transparency
  - Border animation visible
  - Centered in container
- **Status:** ⚪ Ready

---

## 9. DATA PERSISTENCE

### TC-DATA-001: Student Profile Persistence
**Objective:** Verify student profile saves after login
- **Steps:**
  1. Login to application
  2. Complete registration or update profile
  3. Refresh page
  4. Observe student data
- **Expected Result:**
  - Student name persists
  - Avatar selection saved
  - Board and class retained
  - Sidebar shows saved data
- **Status:** ⚪ Ready

### TC-DATA-002: Quiz Progress Persistence
**Objective:** Verify quiz attempts save
- **Steps:**
  1. Complete a quiz with known score
  2. Refresh page
  3. Check dashboard and analytics
- **Expected Result:**
  - Quiz score appears in recent tests
  - Analytics updated
  - Statistics reflect completed quiz
- **Status:** ⚪ Ready

### TC-DATA-003: Chapter Expansion State
**Objective:** Verify chapter expanded/collapsed state persists
- **Steps:**
  1. Expand a chapter in Syllabus
  2. Navigate away and back to Syllabus
  3. Observe chapter state
- **Expected Result:**
  - Chapter remains expanded if preference saved
  - Or defaults to collapsed on fresh load (acceptable)
- **Status:** ⚪ Ready

---

## 10. ERROR HANDLING

### TC-ERROR-001: Invalid Email Format
**Objective:** Verify validation for email format
- **Steps:**
  1. Try to register with invalid email: "notanemail"
  2. Observe validation
- **Expected Result:**
  - Error message: "Please enter a valid email"
  - Form not submitted
- **Status:** ⚪ Ready

### TC-ERROR-002: Password Too Short
**Objective:** Verify minimum password length validation
- **Steps:**
  1. Try to register with password: "123"
  2. Observe validation
- **Expected Result:**
  - Error message: "Password must be at least 6 characters"
  - Form not submitted
  - Strength bar shows weak
- **Status:** ⚪ Ready

### TC-ERROR-003: Required Field Validation
**Objective:** Verify required fields cannot be empty
- **Steps:**
  1. Try to register without entering name
  2. Click continue
- **Expected Result:**
  - Error highlights name field
  - Error message displays
  - Form not submitted
- **Status:** ⚪ Ready

### TC-ERROR-004: Network Error Handling
**Objective:** Verify graceful handling of network errors
- **Steps:**
  1. Disconnect internet
  2. Try to login or load page
  3. Observe error handling
- **Expected Result:**
  - Error message displays to user
  - "Retry" button available
  - App doesn't crash
- **Status:** ⚪ Ready

---

## 11. ACCESSIBILITY

### TC-A11Y-001: Keyboard Navigation
**Objective:** Verify keyboard navigation works
- **Steps:**
  1. Use Tab key to navigate form fields
  2. Use Tab to navigate buttons
  3. Press Enter to activate
- **Expected Result:**
  - Tab order is logical
  - Focus visible on elements
  - Enter activates buttons
  - Escape closes modals
- **Status:** ⚪ Ready

### TC-A11Y-002: Color Contrast
**Objective:** Verify text contrast meets accessibility standards
- **Steps:**
  1. Check all text elements
  2. Verify against WCAG AA standards
- **Expected Result:**
  - All text has sufficient contrast
  - Readable in light and dark
- **Status:** ⚪ Ready

### TC-A11Y-003: Font Sizing
**Objective:** Verify font sizes are readable
- **Steps:**
  1. Observe all font sizes
  2. Zoom in/out to test scalability
- **Expected Result:**
  - All text readable at default size
  - Zoom functionality works
  - No text overflow issues
- **Status:** ⚪ Ready

---

## Test Execution Summary

| Module | Total Cases | Ready | In Progress | Blocked |
|--------|-----------|-------|-------------|---------|
| Authentication | 12 | 12 | 0 | 0 |
| Dashboard | 7 | 7 | 0 | 0 |
| Syllabus | 5 | 5 | 0 | 0 |
| Practice | 10 | 10 | 0 | 0 |
| Analytics | 5 | 5 | 0 | 0 |
| Reports | 5 | 5 | 0 | 0 |
| Navigation | 7 | 7 | 0 | 0 |
| UI/UX | 7 | 7 | 0 | 0 |
| Data Persistence | 3 | 3 | 0 | 0 |
| Error Handling | 4 | 4 | 0 | 0 |
| Accessibility | 3 | 3 | 0 | 0 |
| **TOTAL** | **68** | **68** | **0** | **0** |

---

## Notes

- All test cases use the demo account: **demo@eduai.in** / **demo123** unless specified
- Tests assume standard desktop browser resolution
- Responsive design tests to be conducted separately
- Performance and load testing not included in this suite
- Security testing should be conducted by specialized team
- API testing should verify backend endpoints separately

---

## Version History

| Version | Date | Changes |
|---------|------|---------|
| 1.0 | 2026-05-29 | Initial test cases created |

