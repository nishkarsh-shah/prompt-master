# Other ways to install

The quickest install is the button in the [README](../README.md#install). This page is for everything else: a zip upload, the terminal, team plans and updates.

[← Back to the README](../README.md)

> [!IMPORTANT]
> **Use one way per app.** Installing twice shows Prompt Master twice. To switch, [remove the old copy](#remove-an-old-copy) first.

## Find your way

| Your situation | Go to |
| --- | --- |
| The directory link doesn't work, or you're on mobile | [Claude: upload the zip](#claude-upload-the-zip) |
| You use Claude Code with an API key, or want it without Claude chat | [Claude Code: terminal](#claude-code-terminal) |
| You want Codex without `$skill-installer` | [Codex: terminal](#codex-terminal) |
| You're on a Team, Enterprise or workspace plan | [Team and workspace plans](#team-and-workspace-plans) |
| You already have it and want the new version | [Updating](#updating) |

<p align="center"><img src="../assets/divider.svg" alt="" width="100%" height="27"></p>

## Claude: upload the zip

Works on the web, desktop and mobile apps.

1. Download [`prompt-master-claude.zip`](https://github.com/nishkarsh-shah/prompt-master/raw/main/claude/prompt-master-claude.zip).
2. In **Settings → Capabilities**, turn on **Create and edit files**.
3. Go to **Settings → Plugins → Browse plugins**, click **Add**, choose **Upload plugin**, and pick the zip.

It also shows up in Claude Code when you sign in there with the same account.

## Claude Code: terminal

Claude Code only gets your Claude chat installs when you sign in with a Claude account. With an API key or a cloud provider login, pick one of these.

**Option 1: link the repo** (Mac or Linux, needs git). Updates with one `git pull`.

```bash
git clone -b main-staging https://github.com/nishkarsh-shah/prompt-master.git ~/prompt-master
mkdir -p ~/.claude/skills && ln -sfn ~/prompt-master/claude/plugin/skills/prompt-master ~/.claude/skills/prompt-master
```

**Option 2: download it** (no git). Run it again to update.

Mac or Linux:

```bash
mkdir -p ~/.claude/skills && curl -fsSL -o /tmp/prompt-master-claude.zip https://github.com/nishkarsh-shah/prompt-master/raw/main/claude/prompt-master-claude.zip && unzip -o /tmp/prompt-master-claude.zip -d ~/.claude/skills
```

Windows (PowerShell):

```powershell
New-Item -ItemType Directory -Force "$HOME\.claude\skills" | Out-Null
Invoke-WebRequest https://github.com/nishkarsh-shah/prompt-master/raw/main/claude/prompt-master-claude.zip -OutFile "$env:TEMP\prompt-master-claude.zip"
Expand-Archive "$env:TEMP\prompt-master-claude.zip" -DestinationPath "$HOME\.claude\skills" -Force
```

## Codex: terminal

**Option 1: link the repo** (Mac or Linux, needs git). If you already cloned it for Claude Code, skip the first line.

```bash
git clone -b main-staging https://github.com/nishkarsh-shah/prompt-master.git ~/prompt-master
mkdir -p ~/.agents/skills && ln -sfn ~/prompt-master/chatgpt/prompt-master ~/.agents/skills/prompt-master
```

**Option 2: download it** (no git). Run it again to update. For one project only, unzip into that project's `.agents/skills` folder instead.

Mac or Linux:

```bash
mkdir -p ~/.agents/skills && curl -fsSL -o /tmp/prompt-master-chatgpt.zip https://github.com/nishkarsh-shah/prompt-master/raw/main-staging/chatgpt/prompt-master-chatgpt.zip && unzip -o /tmp/prompt-master-chatgpt.zip -d ~/.agents/skills
```

Windows (PowerShell):

```powershell
New-Item -ItemType Directory -Force "$HOME\.agents\skills" | Out-Null
Invoke-WebRequest https://github.com/nishkarsh-shah/prompt-master/raw/main-staging/chatgpt/prompt-master-chatgpt.zip -OutFile "$env:TEMP\prompt-master-chatgpt.zip"
Expand-Archive "$env:TEMP\prompt-master-chatgpt.zip" -DestinationPath "$HOME\.agents\skills" -Force
```

<p align="center"><img src="../assets/divider.svg" alt="" width="100%" height="27"></p>

## Team and workspace plans

On Claude Team and Enterprise plans, and on ChatGPT workspace plans, an admin may need to allow plugins or skill uploads first. If you can't see the option, ask your admin.

## Updating

| You installed with | To update |
| --- | --- |
| The Claude directory button | Nothing to do. It updates itself |
| A zip upload (Claude or ChatGPT) | [Remove the old copy](#remove-an-old-copy), then download the new zip and upload it |
| A marketplace in the ChatGPT desktop app | Refresh the marketplace under **Plugins**, then update Prompt Master |
| `$skill-installer` in Codex | Delete `~/.agents/skills/prompt-master`, run the install command again, then restart Codex |
| A linked repo | `git -C ~/prompt-master pull` |
| A terminal download | Run the same command again |

## Remove an old copy

Before switching to a different way, remove the one you have:

- **Claude chat:** open **Settings → Plugins**, find Prompt Master, and remove it.
- **ChatGPT:** open [chatgpt.com/skills](https://chatgpt.com/skills), find Prompt Master, and use its **⋯** menu to remove it.
- **Claude Code terminal:** `rm -rf ~/.claude/skills/prompt-master`
- **Codex:** `rm -rf ~/.agents/skills/prompt-master`
