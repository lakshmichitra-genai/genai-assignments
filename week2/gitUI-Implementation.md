Phase 1: Creating the Application & Visual Theme
🎯 Phase Goal
Build the initial layout for a GitHub Code Reviewer dashboard with a sleek developer‑friendly dark theme.

📋 Copy-Paste Prompt
text
Build the foundation for an AI GitHub Code Reviewer dashboard called "CodeMind AI".

Use a modern dark developer theme with a deep charcoal background, subtle grid overlay, and glowing accents in green and purple. Typography should be clean monospace with high‑contrast white text. Add smooth glowing scrollbars in neon green.
🧪 Verification Steps
[ ] Confirm the dashboard loads with a dark charcoal background and subtle grid lines.

[ ] Check glowing green/purple accents around panels and scrollbars.

Phase 2: Sticky Header & Navigation Bar
🎯 Phase Goal
Add a top navigation bar with GitHub branding and workflow indicators.

📋 Copy-Paste Prompt
text
Add a sticky glassmorphic navigation bar pinned to the top.

On the left, display "CodeMind AI" with a glowing GitHub Octocat icon.  
In the middle, add navigation links: "Dashboard" (active), "Repositories", "Pull Requests", "History".  
On the right, show an n8n workflow status badge "Workflow Connected" with a pulsing green dot, plus a circular profile avatar with initials "CR".
🧪 Verification Steps
[ ] Scroll the page — nav bar stays pinned with frosted glass effect.

[ ] Verify Octocat icon glows gently.

[ ] Hover over links — pill highlight animation appears.

Phase 3: Dashboard Layout & Input Controls
🎯 Phase Goal
Create a two‑column layout with PR input controls and metrics.

📋 Copy-Paste Prompt
text
Build a two-column dashboard layout.

Left sidebar: add a card titled "GitHub Reviewer". Include an input field with repo+PR placeholder ("e.g. repo#123"), checkboxes for modules (Code Quality, Security Scan, Documentation Check), and a glowing "Analyze PR" button.  

Right workspace: add 3 metric cards showing "12 PRs Reviewed", "92% Avg Quality Score", "Active GitHub Sync" with glowing icons.
🧪 Verification Steps
[ ] Sidebar shows input + checkboxes + button.

[ ] Metrics cards display stats with glowing icons.

Phase 4: Review Workspace & Loading Effects
🎯 Phase Goal
Design the main review workspace with waiting and loading states.

📋 Copy-Paste Prompt
text
In the right workspace, create a large card titled "Review Workspace".

Default state: show a waiting screen with concentric rings spinning around a GitHub logo, prompting user to enter a PR number.  

Loading state: show a glowing green scan line moving top-to-bottom, plus a progress ticker. Add shake animation for errors.
🧪 Verification Steps
[ ] Waiting screen shows concentric rings around GitHub logo.

[ ] Loading state animates scan line + ticker.

Phase 5: Input Validation, Webhook Connection & Error Handling
🎯 Phase Goal
Connect input to n8n webhook and handle errors gracefully.

📋 Copy-Paste Prompt
text
Make the dashboard interactive and connect to n8n webhook endpoint `/webhook/github_reviewer`.

When user submits a PR key:
1. If empty, highlight input red, shake card, show error message.  
2. If valid, disable input/button, change button text to "Analyzing...", activate scan beam.  
3. Cycle progress messages ("Fetching PR data...", "Analyzing code diff...", "Checking documentation...", "Synthesizing review...") every 1.5s.  
4. Send POST request with repo+PR JSON payload.  
5. Handle errors: show error card if webhook unreachable or invalid response.
🧪 Verification Steps
[ ] Empty input triggers red highlight + shake.

[ ] Valid PR triggers scan beam + progress ticker.

[ ] Network tab shows POST request to /webhook/github_reviewer.

Phase 6: Formatting AI Analysis & Results Display
🎯 Phase Goal
Render LLM review output beautifully with markdown formatting.

📋 Copy-Paste Prompt
text
Format AI review output inside workspace.

Convert markdown into HTML:
- Headings with glowing green titles.  
- Bold text + bullet lists.  
- Code blocks in dark monospace boxes with neon green text.  
- Tables styled with green headers and alternating row colors.  

On completion: show animated "Review Complete" badge, fade in formatted report, re-enable input form.
🧪 Verification Steps
[ ] "Review Complete" badge appears at end.

[ ] Headings, lists, code, tables render cleanly.

[ ] Input resets for next PR.