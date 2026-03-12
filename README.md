# Introduction to Academic Research

**An interactive HTML presentation for library instruction at Tulane University.**

Presented by **Kay P Maye**
Scholarly Engagement Librarian & Resources/Data Analyst
Howard-Tilton Memorial Library · Tulane University

---

## Overview

This is a single-file, self-contained HTML presentation designed for in-person and self-paced library instruction sessions. It teaches undergraduate students how to find, evaluate, and use library resources for academic research. No server, framework, or internet connection is required to run it — just open the HTML file in any modern browser.

**Live link:** `https://bit.ly/research_TUL_maye`

---

## Features

### Adaptive Learning Paths
The presentation opens with three learning mode options so the instructor and class can choose their approach:

- **Option A — Guided walkthrough:** Skip the pretest, go straight to content slides.
- **Option B — Pretest together:** Take the knowledge pretest as a class, discuss answers, then review content.
- **Option C — Small group exploration:** Groups work through the pretest and slides at their own pace with periodic instructor check-ins.

### Knowledge Pretest (16 Questions)
A built-in diagnostic quiz covering five topic clusters. Answer positions are randomized across all four options (balanced distribution: 4 questions each at positions A, B, C, D). Each question provides immediate feedback with an explanation. Topics assessed:

| Cluster | Questions | Content Covered |
|---------|-----------|-----------------|
| Source Types & Evaluation | 4 | Scholarly vs. credible, Wikipedia, peer review |
| Boolean Search & Strategies | 4 | AND/OR/NOT, truncation, narrowing/broadening |
| Databases, Tools & Google Scholar | 4 | Subject databases, Google Scholar setup, A-Z list |
| ILL & Getting Help | 2 | Interlibrary Loan, research consultations |
| Tulane Library Resources | 2 | Library locations, LibGuides, Media Services |

### Personalized Results
After the pretest, students see a results dashboard with per-cluster scores and recommended slides. Students who already know a topic area can skip ahead; students who need review get directed to the right content.

### Interactive Activities (4)
1. **Evaluate a Source** — Students pick from six real sources (CDC, PMC, Psychology Today, Wikipedia, APA, Nature) and classify them as scholarly, credible, or questionable. Instant feedback compares their answer to the correct classification.
2. **Build Your Search** — An interactive Boolean search string builder. Students enter concepts and synonyms; the tool generates a properly formatted Boolean query in real time.
3. **Choose Your Databases** — Students select databases for their research area, aided by a built-in subject-to-database reference lookup.
4. **Research Plan** — A capstone activity that auto-fills from earlier responses. Students compile their topic, search string, databases, and source types into a single plan.

### Additional Tools
- **Database Finder:** A dropdown selector covering 17 subject areas, each with recommended databases and descriptions.
- **Search Troubleshooting Panel:** Expandable FAQ for common search problems (too many results, too few, irrelevant, no full text).
- **Activity Tracker:** Fixed-position dots showing completion status of all four activities.
- **Export Options:** Copy all responses to clipboard, download as a text file, or print/save as PDF.
- **Email Panel:** Students can email their compiled activity responses to themselves via a mailto link.

---

## Content Slides

| # | Slide | Description |
|---|-------|-------------|
| 1 | Title Slide | Session overview, presenter info, access link |
| 2 | How Would You Like to Learn? | Three learning mode options for the class |
| 3 | Knowledge Pretest | 16-question diagnostic quiz |
| 4 | Pretest Results | Personalized scores and slide recommendations |
| 5 | Why Use the Library? | Google vs. library comparison |
| 6 | Tulane Library Locations | Howard-Tilton, Latin American Library, Matas, Special Collections |
| 7 | Understanding Your Sources | Source types table: scholarly, credible, not citable |
| 8 | Media Services & Equipment | Streaming collections, equipment loans (6th floor) |
| 9 | Activity 1: Evaluate a Source | Hands-on source classification with feedback |
| 10 | Search Terms & Boolean Operators | AND, OR, NOT, quotes, truncation |
| 11 | Activity 2: Build Your Search | Interactive Boolean search builder |
| 12 | The Search Ecosystem & Databases | Comparison table + subject database finder |
| 13 | Research Guides & Google Scholar | LibGuides, Google Scholar Tulane setup, troubleshooting |
| 14 | Activity 3: Choose Your Databases | Database selection with subject reference |
| 15 | Interlibrary Loan (ILL) | How to request, turnaround times |
| 16 | Getting Help | Chat, email, research consultations, find your librarian |
| 17 | Activity 4: Research Plan | Auto-filled capstone plan from all previous activities |
| 18 | Discussion & Reflection | Discussion prompts + exit reflection |
| 19 | Summary & Next Steps | Five key takeaways, action items, export tools |

---

## Technical Details

### Requirements
- Any modern web browser (Chrome, Firefox, Safari, Edge)
- No server, build step, or dependencies required
- No external libraries or CDN calls — fully self-contained

### Navigation
- **Dropdown selector** in the top nav bar for direct slide access
- **Previous/Next buttons** and keyboard shortcuts:
  - `←` / `→` or `PageUp` / `PageDown` to navigate
  - `Home` / `End` to jump to first or last slide
  - Keyboard navigation is disabled on the pretest slide and inside form inputs
- **Progress bar** at the bottom of the viewport

### Responsive Design
- Adapts to mobile/tablet screen sizes (grid layouts collapse to single column)
- Activity tracker hides on small screens
- Print stylesheet included (all slides visible, nav/controls hidden)

### Branding
Uses Tulane University's official color palette:
- **Tulane Green:** `#285C4D`
- **Tulane Blue:** `#71C5E8`
- **Storm Shutters:** `#00778B`
- **Medallion (Gold):** `#CC9900`
- **Olive Branch:** `#658D1B`

---

## Customization

### Editing Pretest Questions
All pretest questions are defined in the `pretestQuestions` JavaScript array near the top of the `<script>` block. Each question object includes:

```javascript
{
  id: 0,                    // Sequential ID
  cluster: 'sources',       // Topic cluster key (matches `clusters` object)
  topic: 'Source Types',    // Display label for the topic badge
  q: 'Question text...',    // The question stem
  options: ['A', 'B', 'C', 'D'],  // Four answer choices
  correct: 2,               // Zero-indexed position of the correct answer
  explanation: '...'         // Feedback shown after answering
}
```

### Editing Database Recommendations
The `databaseInfo` object maps subject keys to recommended databases. Add or modify entries to update the database finder dropdown on Slide 12 and the quick reference on Slide 14.

### Editing Topic Clusters
The `clusters` object defines how pretest questions map to content slides. Each cluster specifies its display name, associated slide indices, slide names, and accent color.

---

## Contact

**Kay P Maye**
Scholarly Engagement Librarian & Resources/Data Analyst
Howard-Tilton Memorial Library · Tulane University
📧 kmaye@tulane.edu
