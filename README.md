# recall-vault

**Claude Code gets persistent memory.**

Claude Code is brilliant, but it's amnesiac. `recall-vault` bridges that gap by connecting it to an Obsidian-based knowledge base. Now, Claude can remember project decisions, past errors, user preferences, and patterns across sessions.

## How it works

1. **Before any task:** Claude Code searches your Obsidian vault for relevant memory indexed with QMD.
2. **During the task:** It operates using that context.
3. **After any task:** Claude Code reflects on the outcome and updates the vault with what's worth saving (patterns, project decisions, patterns, or new errors).

## Setup

1. Clone this repo: `git clone https://github.com/seko121/recall-vault.git`
2. Run the setup script: `./setup.sh`
3. Point your Claude Code configuration to the `vault` directory.
4. Add the provided `SKILL.md` to your Claude Code skills directory.

## Use Cases

- **Pattern Persistence:** Never explain the same architecture pattern twice.
- **Error Remediation:** Stop repeating debugging cycles for known issues.
- **Preference Alignment:** Automatically adhere to Seko's coding style and preferred tools.
- **Decision Tracking:** Keep a clean record of why decisions were made, not just what was built.
