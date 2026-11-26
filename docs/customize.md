# Customize

[← Back to the README](../README.md)

Each edition is one instruction file:

- **Claude:** [`claude/plugin/skills/prompt-master/SKILL.md`](../claude/plugin/skills/prompt-master/SKILL.md). To change what it recommends, edit the model table, the effort table and the rules under them in section 6. To add a preset, add a row to the table in section 3.
- **ChatGPT and Codex:** [`chatgpt/prompt-master/SKILL.md`](../chatgpt/prompt-master/SKILL.md). The model and effort tables are in section 5. It names models by family (Luna, Terra, Sol, Astra) with no version numbers, so new OpenAI releases don't need an edit.

## Rebuild the zip after a change

From the repo folder, run the commands for the edition you changed, then upload the new zip again.

**Claude** (upload under **Settings → Plugins**):

```bash
cd claude/plugin/skills && rm -f ../../prompt-master-claude.zip && zip -r ../../prompt-master-claude.zip prompt-master -x '*.DS_Store'
```

**ChatGPT and Codex** use the skill zip (for ChatGPT, upload it at chatgpt.com/skills → **Add → Upload a skill**):

```bash
cd chatgpt && rm -f prompt-master-chatgpt.zip && zip -r prompt-master-chatgpt.zip prompt-master -x '*.DS_Store'
```

**OpenAI directory submission** uses the plugin zip. This copies your edited skill into the plugin folder, then zips it:

```bash
cp -R chatgpt/prompt-master/. chatgpt/plugin/skills/prompt-master/ && cd chatgpt/plugin && rm -f ../prompt-master-openai-plugin.zip && zip -r ../prompt-master-openai-plugin.zip . -x '*.DS_Store'
```

After a change, test it in a new chat with `pm help` and one `ep:` task, and make the same change in the other edition so the two stay in step.
