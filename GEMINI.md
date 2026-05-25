# Super PM: Universal Compatibility

This file provides the necessary instructions and tool mappings to ensure the **Super PM** extension functions seamlessly across different AI CLI platforms, including Gemini CLI, Claude Code, and Codex.

## 🛠 Tool Mapping

This extension uses the industry-standard "Claude Code" tool naming convention. The following table identifies how these tools map to different platforms:

| Standard Tool Name | Gemini CLI Equivalent | Codex / Copilot CLI Equivalent |
| :--- | :--- | :--- |
| `Read` | `read_file` | `read` |
| `Write` | `write_file` | `write` |
| `Edit` | `replace` | `edit` |
| `Bash` | `run_shell_command` | `bash` |
| `Grep` | `grep_search` | `grep` |
| `Glob` | `glob` | `glob` |
| `Skill` | `activate_skill` | `skill` |
| `AskUser` | `ask_user` | `ask_user` |

## 🚀 Execution Instructions

1.  **Platform Detection:** When this extension is loaded, the agent should identify the host platform.
2.  **Mapping:** Use the table above to translate commands found in `SKILL.md` or any reference files.
3.  **Path Resolution:** All internal references to `skills/super-pm/references/` should be resolved relative to the extension root.

## 📁 Agent Skills Standard

This extension adheres to the [Agent Skills](https://agentskills.io) standard. Skills are located in the `skills/` directory. For tools that expect an `.agents/skills/` directory, this should be treated as a functional alias for the `skills/` folder in this repository.

---
*For more information on the extension logic, see the [README.md](./README.md) or the core [SKILL.md](./skills/super-pm/SKILL.md).*
