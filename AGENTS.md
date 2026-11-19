# Edu Plugin Maintenance

## Source of truth

- This repository is the maintained source for the personal Edu plugin. Edit the skills under `plugins/edu/`; Codex installs them into a separate cache.
- The manifest is `plugins/edu/.codex-plugin/plugin.json`, using the compatibility format supported by the installed desktop app. Keep the plugin identifier `edu` stable.
- The repository marketplace is `.agents/plugins/marketplace.json`. Register the repository root as a local marketplace so `edu@personal-edu` resolves to `plugins/edu/`.
- Keep author, developer attribution, creator, signature, and equivalent fields empty. Do not add identity bylines to new or edited files.

## Skills

- `plugins/edu/skills/edu-init/SKILL.md`: initialize or update a course workspace's AGENTS.md using its materials and learner preferences.
- `plugins/edu/skills/edu-group-project-init/SKILL.md`: initialize a project child directory or existing project with a shallow layout, add subdirectories only for actual contents, and require explicit user consent for beyond-course solution choices.
- `plugins/edu/skills/edu-teaching/SKILL.md`: teach against original lecture materials, with page references, Chinese explanations and English terminology, concrete examples, process visuals, and paced understanding checks.
- Preserve each skill's scope and the learner's explicit preferences. Adding a plugin does not authorize changing unrelated course files.
- Do not merge all workflows into one long skill. Add a separate `plugins/edu/skills/<skill-name>/SKILL.md` when the learner requests a distinct reusable capability. Give it a precise description so the appropriate workflow can be selected.
- Existing skill names remain `edu-init`, `edu-group-project-init`, and `edu-teaching`. Do not recreate standalone duplicates under the global skills directories.

## Update and validate

1. Read the relevant skill before editing it. Use the skill-creator guidance when adding or changing skills, if available.
2. Add only supporting scripts, examples, or references that the new workflow needs. Keep original course material separate from this plugin.
3. Validate changed skills using the available skill validator. Inspect YAML and JSON files for parse errors and unfinished scaffolding. Ensure manifest paths resolve inside this plugin.
4. Increment the plugin manifest version when a completed update changes the installed behavior: patch for corrections, minor for new compatible skills or capabilities, major for incompatible changes. Read the current version rather than assuming a starting version.
5. Refresh the local installation and verify the installed version and skill contents. Use the desktop app's bundled CLI if another command named `codex` on PATH is an older installation.

For the CLI available at initial setup, the refresh and inspection commands are:

```powershell
& $env:CODEX_CLI_PATH plugin add edu@personal-edu --json
& $env:CODEX_CLI_PATH plugin list --marketplace personal-edu --json
```

Check that `CODEX_CLI_PATH` resolves to the desktop app's CLI; discover its current path if the variable is unavailable. These commands describe a verified local installation route, not a guarantee that every future CLI version uses the same interface.

The app may require a restart or a new chat to refresh its visible plugin and skill catalog. Do not restart the running app or interrupt another chat automatically. Report what installation checks established and what still needs a UI refresh.
