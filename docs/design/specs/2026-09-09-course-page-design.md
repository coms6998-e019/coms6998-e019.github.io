# Course page design — COMS 6998-019, Fall 2026

## Goal

Public course website for COMS 6998-019, Design of Production Agentic Systems,
served at `coms6998-e019.github.io` and modeled on the Stanford CS336 page
(`https://cs336.stanford.edu`): one static page with a fixed top navbar,
header, staff, logistics, content, coursework, and schedule.

## Decisions

- **Static files only.** `index.html` and `style.css` at the repo root, served
  by GitHub Pages with no build step and no JavaScript. The only external
  request is IBM Plex Sans from Google Fonts.
- **IBM Carbon Design System, hand-written.** Carbon White-theme color tokens
  as custom properties, the productive type scale, the 8px spacing scale,
  square corners, a gray-100 UI shell header, Carbon's data table for the
  schedule, and Carbon tags for the out, due, and exam markers. Values are
  transcribed from the published tokens rather than pulling the Carbon
  packages, which keeps the site two files. The earlier Bootstrap 3 clone of
  CS336's stylesheet is gone.
- **CS336 granularity is the target.** Schedule rows carry a one-line topic, a
  short reading list, and deadline markers. Homework is three bullets per
  assignment, not the assignment brief. Grading is one small table plus one
  sentence on the rubric. No units table, no readings table.
- **Detail lives outside this repository.** The full course structure, the
  week-by-week table with its instructor-only grading column, the homework
  briefs, and the grading guide stay in the sibling `instructor-materials`
  repository. Nothing instructor-only appears on the page or in this
  repository.
- **Reading links live in the schedule row that assigns them**, the way CS336
  puts materials next to the lecture. Rows carry a colored band for their
  course unit, and the legend names each unit's week range so unit membership
  never depends on color alone.
- **No headshots or logos yet.** Staff cards use CSS initials avatars; the
  header carries no institutional logos until image files are supplied.
- **Placeholders** marked "TBA": the teaching assistant and the course
  discussion channel. Homework topics and the HW2 and HW3 deadlines are marked
  tentative on the page rather than hidden.

## Verification

Preview locally at mobile, tablet, and desktop widths. Check the page against
the course structure for missing rows, altered dates or weights, broken links,
and instructor-only leakage, and check the stylesheet against the published
Carbon token values.
