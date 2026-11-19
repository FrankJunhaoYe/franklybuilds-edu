---
name: edu-init
description: Initialize or update a course workspace's AGENTS.md from local teaching materials and the learner's preferences. Use for course folder setup, study guide setup, or requests such as 初始化课程目录 or 继续初始化 when refining a course's standing study instructions.
---

# Initialize a Course Workspace

Create or update the root `AGENTS.md` as a concise guide for future coursework and tutoring in this folder.

For a group-project workspace, use `edu-group-project-init` instead. It handles creating a project subdirectory or initializing an existing project, without replacing this course-level guide.

## Establish the Course Context

1. Read the current `AGENTS.md` and inventory the course folder. Identify the syllabus, lecture and lab materials, assignments, code or circuit files, and any supplied tests or tools. Inspect the relevant source material to verify paths, commands, and conventions before documenting them.
2. Use the learner's stated course, institution, exam language, and tutoring preferences. For COMP1003 Computer Organization at Beijing Normal-Hong Kong Baptist University (BNBU), record the English exam. For another course, establish its details independently and follow any course-specific language preferences the learner gives.
3. Title a new guide `Repository Guidelines`. Record the learning context, folder layout, and applicable lab commands, naming rules, and verification steps. Preserve unrelated instructions in an existing guide. Include commit or review guidance when Git history or the learner's request makes it relevant.

## Capture the Study Preferences

Use the following defaults for this learner, subject to any course-specific preferences.

- Explain concepts and reasoning in Chinese. After every occurrence of an important concept in Chinese, give the matching English term immediately, for example `程序计数器（program counter, PC）`. Use course terminology and notation. Write practice questions and exam-style model answers in English, or use the course's confirmed exam language when it differs.
- Base explanations on the relevant slides, supplied code, lab files, and exercises. During tutoring, use visuals to show how the material works. Annotate Digital circuit diagrams with signal paths and control signals. Use timing diagrams to show behavior across clock edges and execution tables to track changes in registers, memory, or the program counter. Choose an interactive visual when changing inputs or stepping through execution helps the learner follow the result.
- Adapt the visuals to the course and the question. Use Digital when the course uses Digital, and label conceptual sketches separately from diagrams derived from the supplied files.
