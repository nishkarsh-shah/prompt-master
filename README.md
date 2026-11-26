<p align="center">
  <img src="assets/logo.png" alt="Prompt Master icon" width="214" height="214">
</p>

<h1 align="center">Prompt Master</h1>

<p align="center"><b>Turn a rough prompt into a clear one, and get a model and effort recommendation.</b></p>

<p align="center">
  <a href="LICENSE"><img src="assets/badge-license.svg" alt="MIT license" width="186" height="32"></a>
  <a href="#claude-and-claude-code"><img src="assets/badge-claude.svg" alt="Works with Claude" width="186" height="32"></a>
  <a href="#chatgpt"><img src="assets/badge-chatgpt.svg" alt="Works with ChatGPT and Codex" width="230" height="32"></a>
</p>

<p align="center"><a href="#install">Install</a> · <a href="#commands">Commands</a> · <a href="#presets">Presets</a> · <a href="#models-it-recommends">Models</a> · <a href="#good-to-know">Good to know</a></p>

https://github.com/user-attachments/assets/9bbe621f-aff3-4116-a27e-9cd47a12f054

## Install

Pick the app you use. The commands are the same in both editions.

### Claude and Claude Code

<a href="https://claude.ai/customize/plugins/id/49a4e159-eae9-429b-89f6-4a1df0919c73%40anthropic-plugin-directory?via=directory"><img src="assets/add-to-claude.svg" alt="Add Prompt Master to Claude" width="300" height="48"></a>

Sign in, click **Add**, then type `pm help` in a new chat. Claude Code gets it too when you sign in with the same account, and it updates itself when a new version is out.

### ChatGPT

[Download the zip](https://github.com/nishkarsh-shah/prompt-master/raw/main/chatgpt/prompt-master-chatgpt.zip), then open **Skills → Create → Upload from your computer** and pick it.

### Codex

In Codex, type:

```text
$skill-installer install https://github.com/nishkarsh-shah/prompt-master/tree/main/chatgpt/prompt-master
```

> [!TIP]
> **Link not working, or on a team plan?** See [other ways to install](docs/install.md): zip upload, terminal, updates and admin settings.

Installed? Try the [commands](#commands) next, or type `pm help`.

<br>

<p align="center"><img src="assets/hero.svg" alt="A rough line straightens into a clean line" width="100%"></p>

## Commands

**Make a prompt better**

| You type | You get |
| --- | --- |
| `pm: <rough prompt>` | A rewritten prompt, then the answer to it |
| `pm only: <rough prompt>` | Only the rewritten prompt, in a copy-ready block |
| `pm code:` `pm email:` `pm study:` `pm research:` | Add one of these words after `pm` to shape the rewrite for that kind of task. Example: `pm email: tell my manager I'll be late` |

**Choose a model**

| You type | You get |
| --- | --- |
| `ep: <task>` | A model and effort recommendation for the task as you wrote it |
| `ep claude: <task>` | Claude edition only: the same, plus a short Claude Code plan, plan mode and subagent advice |
| `ep codex: <task>` | ChatGPT edition only: the same, plus a short Codex plan and subagent advice |
| `pm pick: <rough prompt>` | The rewrite, then a model and effort recommendation for it (no answer) |

**Check a prompt**

| You type | You get |
| --- | --- |
| `pm critique: <rough prompt>` | A score out of 10, what's missing, and the one fix to make first (no rewrite) |

Stuck? Type **`pm help`** for every command, with examples.

<br>

### Presets

A preset is a shortcut for a common kind of request. Add its word after `pm`, and Prompt Master makes sure your rewrite covers what that kind of task usually needs, so you don't have to remember it all.

| Type | Good for | It makes sure the rewrite has |
| --- | --- | --- |
| `pm code:` | Programming problems | Your code, the error, and what you expected to happen |
| `pm email:` | Writing emails | Who it's to, what you want, the tone, and the one thing you want them to do |
| `pm study:` | Learning something | Your level, simple examples, then practice questions |
| `pm research:` | Looking something up | Facts kept apart from guesses, how sure it is, and sources |

Example: `pm email: follow up with a client who hasn't replied in a week`

<p align="center"><img src="assets/divider.svg" alt="" width="100%" height="27"></p>

## Models it recommends

Not sure which model to use? `ep:` looks at how hard, big, risky and unclear your task is, then suggests a model and an effort level in two separate steps, so any model can pair with any effort. It's a rule of thumb, not a tested formula, so treat it as a starting point. You always choose.

<img src="assets/ladder.svg" alt="Two-step picker. Step 1, model, from how hard and how big the task is. Claude: score 0 to 1 Haiku, 2 to 6 Sonnet, 7 to 9 Opus. ChatGPT and Codex: 0 to 1 Luna, 2 to 3 Terra, 4 to 6 Sol, 7 to 9 Astra. Step 2, effort, from how hard, risky and unclear the task is, same for both: 0 to 1 low or light, 2 to 4 medium, 5 to 7 high, 8 to 9 extra high." width="100%" height="470">

Simple edits, like a rename or a typo fix, always get the lightest model.

<p align="center"><img src="assets/divider.svg" alt="" width="100%" height="27"></p>

## Good to know

### Using it

| Topic | What to know |
| --- | --- |
| **Quick questions** | If key details are missing, it asks up to three questions first. Reply **go** to use its suggestions. `pm only:`, `pm pick:` and `ep` never ask: they use `[placeholders]`. |
| **Follow-ups** | After a `pm:` answer, type `pm again`, `pm why` or `pm undo`. |
| **Capital letters** | `pm:` and `Pm:` both work, for phone keyboards. All-caps `PM:` is ignored, so notes like "PM: standup" don't start it. |
| **Plain asks** | In Claude, "improve this prompt" or "which model should I use?" works without `pm`. |
| **Advice only** | It never switches models or starts subagents for you. You choose. |
| **ChatGPT Chat** | You pick from fewer models there, so it suggests only an effort level. |
| **Language** | The rewrite uses the same language as your draft. |

### Updates, plans and privacy

| Topic | What to know |
| --- | --- |
| **Updating** | Directory installs update themselves. For a zip, download the new one and upload it again. Terminal installs: see the [install page](docs/install.md). |
| **Your plan** | It can't see your plan, so mention it, like `ep: I'm on the Free plan, …`. Otherwise the Claude edition assumes Pro or Max. |
| **Privacy** | It doesn't collect, store or send anything. Please don't paste real passwords or keys. [Privacy policy](claude/plugin/PRIVACY.md) |

Want to change what it recommends, or add a preset? See [Customize](docs/customize.md).

## Credits

Both editions were built by Nishkarsh Shah with Claude.

A community edition for Muse, built on this project, is available in [MaximusMaxxx’s fork](https://github.com/MaximusMaxxx/prompt-master-muse/tree/c5e413d/muse/prompt-master). I haven’t tested or reviewed it.

## License

MIT. See [LICENSE](LICENSE).
