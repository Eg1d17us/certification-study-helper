# ISTQB CTFL Study Helper

An **ISTQB Certification Study Helper** turns Claude into a dedicated study coach for **ISTQB** certifications. This copy is configured for the **Certified Tester Foundation Level (CTFL), syllabus v4.0**.

The skill is deliberately scoped: it only teaches from material you attach (the official syllabus) rather than relying on Claude's general/pretrained knowledge of software testing, so explanations and practice questions stay traceable to the real exam content.

## What it does

Once active, Claude acts as a precise, Socratic tutor and offers eight study modes:

| Mode | What it does |
|------|------------------|
| **Concept Explainer** | Explains a syllabus topic with a citation, plain-language definition, real-world example/analogy, and a common exam trap. |
| **Exam Question Simulator** | Generates multiple-choice questions tagged by K-level (K2–K4) and syllabus section; withholds the rationale until you answer. |
| **Gap Analyser** | Runs a short mixed-topic quiz, scores it, and maps wrong answers back to syllabus sections to rank your weak areas. |
| **Mind Map Builder** | Breaks a chapter into a subtopic hierarchy — outputs a text outline plus a standalone HTML mind map you can open in a browser. |
| **Scenario Coach** | Poses a realistic K3/K4 agile-testing scenario and works through your reasoning Socratically instead of just giving the answer. |
| **Glossary Driller** | Flashcard-style drilling of syllabus glossary terms, tracking which ones you keep missing. |
| **Study Planner** | Builds a day-by-day or week-by-week schedule around your exam date and available study time. |
| **Mock Exam Review** | Reviews a completed practice set question by question and aggregates a per-chapter score breakdown. |

## Requirements

This skill needs reference material attached as a project/session file to work. It will not guess or fabricate syllabus content:

- The official **ISTQB CTFL v4.0 syllabus** converted to `*.md` format (for better token economy) has to be attached in the Project's Files (Point 5 in the below installation instructions).

**Where to download the syllabus:** the CTFL v4.0 syllabus is a free PDF from ISTQB. Get it from either:
- The official ISTQB site → [istqb.org](https://www.istqb.org/) → *Certifications → Certified Tester Foundation Level (CTFL)*, or directly from the ISTQB downloads/documents page.
- Your national/regional ISTQB member board (e.g. ASTQB in the US, UKITB in the UK), which host the same official PDF.

Always use the latest official **v4.0** release rather than third-party reproductions, so the content matches the current exam.

If the syllabus is missing, Claude will say so explicitly instead of proceeding. K1–K6 level *definitions* and Learning Objective examples, used for K-level tagging and mapping on practice questions, are bundled in [`references/k-levels.md`](references/k-levels.md) and work without any additional files.

## Installation

1. Download this repo as a ZIP and extract it
2. Open `SKILL.md` and adjust the description and the `metadata` values to match the certification exam you're preparing for
3. Re-zip the folder, then go to claude.ai → Sidebar → Customize → Skills → Add → Upload a skill → Drag and drop the edited certification-study-helper.ZIP file
4. Go to claude.ai → Sidebar → Projects → New project and create a project
5. Attach the relevant ISTQB syllabus in Files inside your newly created Project. **NOTE:** converting it from `*.PDF` to `*.md` saves a significant number of tokens
6. Start a conversation. You can invoke the certification-study-helper skill with the `/certification-study-helper` command, then write your prompt mentioning the study mode you want to use (e.g. `/certification-study-helper Use concept explainer mode. Explain the concept from syllabus section [section]. section=<add a section name of the Syllabus here>`)

## Repo structure

```
certification-study-helper/
├── SKILL.md              # Skill definition (metadata, persona, rules, output formats)
└── references/
    └── k-levels.md        # ISTQB K1–K6 cognitive-level definitions and Learning Objective examples
```

## Notes

- Claude will never claim personal professional experience or credentials while this skill is active — it sticks to tone/behavior defined in `SKILL.md` rather than an invented backstory.
- Study plan "Resources" only ever point to the attached syllabus — never to external books, courses, or links Claude can't verify.
- This is a community/personal skill and is not affiliated with or endorsed by ISTQB.
