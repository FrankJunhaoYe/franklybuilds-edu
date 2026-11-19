# Edu

Edu 是一个 Codex 插件，包含三个技能。

- [edu-init](plugins/edu/skills/edu-init/SKILL.md) 为课程目录建立学习规则。
- [edu-group-project-init](plugins/edu/skills/edu-group-project-init/SKILL.md) 建立课程小组项目目录并整理资料。
- [edu-teaching](plugins/edu/skills/edu-teaching/SKILL.md) 对照课件逐页讲解并检查理解。

## 本地开发

在仓库根目录运行以下命令。使用支持 `plugin` 命令的 Codex CLI。

```powershell
codex plugin marketplace add .
codex plugin add edu@personal-edu
codex plugin list --marketplace personal-edu --json
```

技能源码位于 `plugins/edu/skills/`。修改插件功能后，按 [维护说明](AGENTS.md) 更新版本并重新安装验证。
