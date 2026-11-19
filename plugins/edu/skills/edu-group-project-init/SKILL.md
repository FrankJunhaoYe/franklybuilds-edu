---
name: edu-group-project-init
description: Initialize a lightweight course group-project workspace inside a course folder or an existing project directory. Organize references, work, and submissions with shallow folders created as needed, write project-local AGENTS.md, and require explicit consent for beyond-course methods. Use for group project initialization or 小组项目初始化; use edu-init for whole-course study instructions.
---

# Initialize a Course Group Project

Initialize a project workspace from the actual course materials and assignment.
Use English directory names and project documentation. Preserve captured source
materials in their original language and preserve the learner's conversation preferences.

## Select the workspace mode

Inspect the current directory, applicable `AGENTS.md` files, nearby course
materials, assignment instructions, and existing project files before choosing.

- **Course-directory mode:** When working in the course-materials directory, create a separate project child directory and initialize inside it. Use the requested name or a suitable English name such as `Project` or a topic-specific kebab-case name. Reuse an identifiable existing project directory instead of creating `Project/Project/`. Keep lectures, labs, textbooks, and the course-level `AGENTS.md` in the course directory. Move only materials clearly belonging to this project; link shared course references.
- **Existing-project mode:** When the user has already created or selected a project directory, initialize directly there. Keep its established layout when usable and add only missing organization and guidance. Identify the parent course through nearby materials, applicable instructions, or user-provided paths.
- If multiple candidate projects or courses make the target ambiguous, inventory what is available and ask one concise clarification before moving files or creating the project in a guessed location. Do not block independent read-only work.

Project-local instructions belong in the selected project's `AGENTS.md` in both
modes. Do not rewrite the course-level guide as a side effect of project setup.

## Establish the assignment and course baseline

Read the relevant project brief, rubric, supplied examples, and course guide.
Inspect the relevant lecture and lab sections to ground substantive claims about
what the course covers. Record source paths or page/slide references where useful.
Distinguish materials available locally from content the learner has already studied.

Extract requirements, deliverables, milestones, naming rules, runtime expectations,
and submission formats without inventing missing details. Mark conflicting or
unconfirmed instructions explicitly. Label archived deadlines and status with
their capture dates; do not describe them as newly verified.

Record topic, group identifier, technology choices, and task allocation only when
established. Initialization does not authorize selecting a topic, introducing a
framework, executing supplied code, deploying, or submitting coursework.

## Organize the three material categories

Start with a small, shallow layout based on the files actually present. These
three directories are a useful default, not a mandatory framework:

| Category | Typical English directories | Purpose |
| --- | --- | --- |
| Original references | `references/` | Supplied briefs, examples, supporting materials, and course snapshots |
| Work in progress | `work/` | Plans, decisions, editable drafts, implementation, and validation evidence |
| Submission content | `submissions/` | Reviewed exports and packages for course milestones |

Keep files directly in these directories until real contents justify a split.
Do not pre-create empty planning, design, report, presentation, frontend, backend,
database, test, or milestone folders. Create a subdirectory when an actual file
group or a selected implementation needs it. A supplied archive of related page
snapshots can retain its own folder. Ordinary initialization should usually have
only one category-directory level; deeper structure needs a concrete use.

For an existing workspace, preserve useful organization. When asked to simplify,
flatten unnecessary categories, remove empty scaffolding and zero-byte
placeholders, and keep all substantive files. Do not replace one large directory
template with another.

Preserve original source filenames and contents. Prefer lowercase English
kebab-case for new general names, with course-required filenames and language
conventions taking precedence. Check for collisions before relocating files;
verify moved files with hashes and repair local links. Keep historical manifests
and utilities distinguishable from current verification tools. Do not run an old
cleanup script merely to initialize a workspace.

Keep working sources outside submission packages. Do not add `.gitkeep` files
just to preserve speculative directories; use them only if an actual versioning
requirement makes them necessary.
Repeated initialization should update missing guidance without duplicating
directories, moving files unnecessarily, or resetting existing decisions and tasks.

## Apply the course-scope rule

This is a user-required approval boundary for project work. Write it explicitly
into the project's `AGENTS.md` so it continues to apply after initialization:

- Normally complete the project using concepts, notation, methods, and implementation techniques established by this course's materials and assignment. Prefer course-provided tools and examples for implementation choices.
- Before adopting a substantive beyond-course concept, algorithm, framework, architecture, service, or implementation approach, explain what exceeds the baseline, its purpose and impact, and an in-course alternative when feasible. Ask whether to include it. Adopt it only after the user explicitly agrees; a general request to build, improve, or initialize the project is not that agreement.
- Reuse explicit approval already given for the same extension and scope. Record the approved extension, the evidence of consent, and its limits in the project planning documentation without adding personal attribution. Approval for one extension does not approve unrelated extensions.
- If course coverage is unclear, inspect the relevant materials. If still unclear, mark the item as pending and ask before adopting it. Continue work that fits the confirmed baseline while awaiting an answer. Silence and elapsed time do not count as consent.
- Optional assignment bonuses and the availability of a tool are not evidence of consent to additional beyond-course techniques. Conversely, an optional topic demonstrably covered by course materials is not automatically beyond-course. Ordinary file organization and verification tools do not, by themselves, add subject matter to the project's solution.

Do not turn this rule into an approval gate for routine initialization. Preparing
the workspace and documenting unchosen alternatives can proceed immediately.

## Write project-local guidance

Create or update concise guidance, preserving unrelated existing content:

- `AGENTS.md`: course and assignment context, directory ownership, relevant parent instructions, course-scope and approval rules, naming and language conventions, attribution rules, and verified build/test commands if available.
- `README.md`: directory map, how sources become working files and submission exports, actual milestones and formats, and current setup status.
- Put a short plan or scope record in `README.md` or an existing working document. Create a separate file in `work/` only when its content warrants it. Do not require a separate document, folder, or approval log for every kind of information.
- Preserve supporting course paths, pending coverage questions, and any explicit extension approvals in the relevant guide or working document. An empty approval record means no extension is approved; do not fabricate consent.

Leave visible bylines, author headers, signatures, and supported editable author,
creator, last-modified-by, and equivalent attribution fields empty. Explicitly
clear supported document attribution fields and inspect saved metadata when
generating or editing formats that support it.

Check directory placement, source preservation, relative links, and agreement
between the guide and the actual tree. Report what was initialized and any
unresolved scope questions. Do not claim implementation, tests, or submission
occurred unless they actually did.
