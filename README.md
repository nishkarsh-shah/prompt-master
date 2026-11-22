<p align="center">
  <img src="assets/logo.png" alt="Prompt Master icon" width="214" height="214">
</p>

<h1 align="center">Prompt Master</h1>

<p align="center"><b>Turn a rough prompt into a clear one, and get a model and effort recommendation.</b><br>One skill, two editions: Claude, and ChatGPT/Codex.</p>

<p align="center">
  <a href="LICENSE"><img src="assets/badge-license.svg" alt="MIT license" width="186" height="32"></a>
  <a href="#claude-edition"><img src="assets/badge-claude.svg" alt="Claude edition" width="186" height="32"></a>
  <a href="#chatgpt-edition"><img src="assets/badge-chatgpt.svg" alt="ChatGPT and Codex edition" width="186" height="32"></a>
</p>

<p align="center"><a href="#pick-your-install">Install</a> · <a href="#commands">Commands</a> · <a href="#models-it-recommends">Models</a> · <a href="#good-to-know">Good to know</a></p>

https://github.com/user-attachments/assets/27a8a5e7-c70a-47d0-95b8-8ed3b9e2f5e4

## Pick your install

The two editions have the same commands. Download the one you use, or both.

| You use | Do this | Details |
| --- | --- | --- |
| Claude chat and Claude Code | Add it from the Claude directory, or download [`prompt-master-claude.zip`](https://github.com/nishkarsh-shah/prompt-master/raw/main/claude/prompt-master-claude.zip) and upload it under **Settings → Capabilities → Skills**. Claude Code gets either automatically, or install it from the [terminal](docs/terminal-install.md). | [Install](#install-claude-and-claude-code) · [Claude Code](#using-claude-code) |
| ChatGPT and ChatGPT Work | Download [`prompt-master-chatgpt.zip`](https://github.com/nishkarsh-shah/prompt-master/raw/main/chatgpt/prompt-master-chatgpt.zip) and upload it in **Skills → Create**. | [Install](#install-chatgpt-and-chatgpt-work) |
| Codex | Run `$skill-installer`, or [link the repo](docs/terminal-install.md) to stay up to date. | [Install](#install-codex) |

> [!TIP]
> **Check it works:** start a new chat or session and type `pm help`. It shows every command with examples, so use it any time you forget one. An existing chat keeps the instructions it already loaded.

<br>

<p align="center"><img src="assets/hero.svg" alt="A rough line straightens into a clean line" width="100%"></p>

## Commands

**Make a prompt better**

| You type | You get |
| --- | --- |
| `pm: <rough prompt>` | A rewritten prompt, then the answer to it |
| `pm only: <rough prompt>` | Only the rewritten prompt, in a copy-ready block |
| `pm code:` `pm email:` `pm study:` `pm research:` | Use one of these words in place of `pm:` to shape the rewrite for that kind of task. Example: `pm email: tell my manager I'll be late` |

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

If key details are missing (numbers, an attached file, a vague goal), it asks up to three quick questions first, and **go** accepts its suggestions. `pm only:`, `pm pick:` and the `ep` commands never ask: they use `[placeholders]` instead.

### What the presets do

Presets are shortcuts for common kinds of requests. Normally Prompt Master works out what your request needs. A preset tells it what to cover for that kind of task, so you don't have to remember. Type the preset word in place of `pm:`.

- **code** is for programming problems. It makes sure your code, your error message and what you expected to happen are included. Example: `pm code: my script crashes when the file is empty`
- **email** is for writing emails. It makes sure it knows who the email is to, what you want, the tone, and the one thing you want them to do. Example: `pm email: ask my landlord to fix the heater`
- **study** is for learning something. It starts from your level, explains with simple examples, then gives you practice questions. Example: `pm study: explain how interest rates work`
- **research** is for looking something up. It keeps facts apart from guesses, says how sure it is, and lists sources. Example: `pm research: how has remote work changed productivity`

<p align="center"><img src="assets/divider.svg" alt="" width="100%" height="27"></p>

## Claude edition

<a href="https://github.com/nishkarsh-shah/prompt-master/raw/main/claude/prompt-master-claude.zip"><img src="assets/claude-edition.svg" alt="For Claude chat and Claude Code. Download the Claude zip." width="100%" height="84"></a>

### Install (Claude and Claude Code)

**Only choose one option.** Installing both shows Prompt Master twice.

<img src="assets/option-1.svg" alt="Option 1, recommended" width="260" height="36">

**Add it from the Claude directory.** It updates itself when a new version is published.

1. In Claude on the web or desktop, open **Customize → Plugins → Discover**.
2. Search for **Prompt Master**, check that the author is **Nishkarsh Shah**, and click **Add**.

<br>

<img src="assets/option-2.svg" alt="Option 2, upload the zip" width="260" height="36">

**Use this if you can't find it in the directory.** It also works on mobile. A zip doesn't update itself: when a new version comes out, download the new zip and upload it again.

1. Download the zip above, then in **Settings → Capabilities**, turn on **Code execution and file creation**.
2. Under **Skills**, choose **Upload skill**, pick the zip and switch it on.

On Team and Enterprise plans, an admin may need to allow plugins and skills first.

### Using Claude Code

- **Signed in with the same Claude account:** Prompt Master appears there automatically, in the desktop app and in the terminal. A zip upload also runs as `/prompt-master`.
- **Using an API key, or want it without Claude chat:** use the [terminal install](docs/terminal-install.md).

Installed? Try the [commands](#commands) next, or type `pm help`.

<br>

## ChatGPT edition

<a href="https://github.com/nishkarsh-shah/prompt-master/raw/main/chatgpt/prompt-master-chatgpt.zip"><img src="assets/chatgpt-edition.svg" alt="For ChatGPT, ChatGPT Work and Codex. Download the ChatGPT zip." width="100%" height="84"></a>

### Install (ChatGPT and ChatGPT Work)

- Download the zip above, then in ChatGPT open **Skills → Create → Upload from your computer** and pick it.

On workspace plans, an admin may need to allow skill uploads first.

### Install (Codex)

In Codex, type:

```text
$skill-installer install https://github.com/nishkarsh-shah/prompt-master/tree/main/chatgpt/prompt-master
```

This puts the skill in `~/.agents/skills/prompt-master`. Restart Codex if `pm help` doesn't respond. To update, delete that folder and run the install command again.

Installed? Try the [commands](#commands) next, or type `pm help`.

<p align="center"><img src="assets/divider.svg" alt="" width="100%" height="27"></p>

## Models it recommends

The picker scores how hard, broad, risky and vague the task is. Then it picks the model and the effort in two separate steps, so any model can pair with any effort. How hard and how big the task is sets the model. How hard, risky and unclear it is sets the effort. The picker is a rule of thumb, not a tested algorithm, and each column is its own ladder: rows show similar difficulty, not equal models.

<img src="assets/ladder.svg" alt="Two-step picker. Step 1 picks the model from how hard and how big the task is. Step 2 picks the effort from how hard, risky and unclear it is. The same lists are in the tables below." width="100%" height="600">

<details>
<summary>The same lists as tables</summary>

**Step 1, model:** score = 2 × how hard + how big (0–9)

| Model score | Claude | ChatGPT and Codex |
| --- | --- | --- |
| 0–1 | Haiku | Luna |
| 2–3 | Sonnet | Terra |
| 4–6 | Sonnet | Sol |
| 7–9 | Opus | Astra |

**Step 2, effort:** score = how hard + how risky + how unclear (0–9)

| Effort score | Effort |
| --- | --- |
| 0–1 | Low |
| 2–4 | Medium |
| 5–7 | High |
| 8–9 | Extra high |

</details>

- **Both:** a mechanical change to one file or item, such as a rename or a typo fix, always gets the lightest model at low effort. Max is never the first pick: it shows up only as the "More careful" option after extra high.
- **Claude:** an unclear or high-risk task moves from Sonnet to Opus, and a task that would need Sonnet at extra high gets Opus at high instead. The hardest, longest tasks add "(or Fable)" for plans that include it.
- **ChatGPT and Codex:** it names the current version of each model, such as GPT-6.1 Sol. Screenshots, charts, app actions and writing go to Terra. Ultra comes up only for work that splits into independent parts. Names checked Nov 21, 2026.

<p align="center"><img src="assets/divider.svg" alt="" width="100%" height="27"></p>

## Good to know

| Topic | What to know |
| --- | --- |
| **Updating** | An uploaded skill doesn't pull changes from GitHub. Download the new zip and upload it again. Directory installs update when a new version is published. Terminal installs update with the command on the [terminal install page](docs/terminal-install.md). |
| **Follow-ups** | After a `pm:` answer, it ends with a line telling you to type `pm again`, `pm why` or `pm undo`. |
| **Capital letters** | `pm:` and `Pm:` both work, since phone keyboards capitalize the first letter. All-caps `PM:` and `EP:` are ignored, so notes like "PM: standup" don't start it. |
| **Plain asks** | In Claude, asking "improve this prompt" or "which model should I use for this?" without typing `pm` also works. It runs `pm only:` or `ep:` and adds a tip to type `pm:` next time. |
| **Advice only** | The skill never switches models or starts subagents for you. `ep claude:` and `ep codex:` only suggest a plan. Pick the model and the effort yourself. |
| **ChatGPT Chat** | You pick from fewer models there, so Prompt Master suggests an effort level and leaves the model to you. |
| **Your plan** | It can't see your plan, so say it in the task, like `ep: I'm on the Free plan, …`. On Free it won't recommend a paid-only model, and on pay-per-token API it suggests a lower effort when the stakes are low. Without a plan named, the Claude edition assumes Pro or Max. |
| **Privacy** | Prompt Master doesn't collect, store or send any data. The skill is told to replace passwords, API keys and card or ID numbers with `[redacted]` in the rewrite, but don't paste real secrets: the AI provider has already received your text. See the [privacy policy](claude/plugin/PRIVACY.md). |
| **Language** | The rewrite uses the same language as your draft. |

Want to change what it recommends, or add a preset? See [Customize](docs/customize.md).

## Credits

Both editions were built by Nishkarsh Shah with Claude.

A community edition for Muse, built on this project, is available in [MaximusMaxxx’s fork](https://github.com/MaximusMaxxx/prompt-master-muse/tree/c5e413d/muse/prompt-master). I haven’t tested or reviewed it.

## License

MIT. See [LICENSE](LICENSE).
