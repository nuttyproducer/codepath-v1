# Using Copilot Mentor Agents in VS Code

This guide explains how to load the CodePath mentor agent instructions into **GitHub Copilot Chat** inside VS Code and get the most out of them.

---

## What Are These Agents?

The files in [`agents/`](../../agents/) contain custom **system-prompt instructions** that turn Copilot Chat into a focused teaching assistant for this curriculum. Instead of getting direct answers, you get guided hints, Socratic questions, and coaching — without full solutions.

There are three agents:

| File | Best For |
|------|----------|
| [`agents/frontend-html-css-mentor.md`](../../agents/frontend-html-css-mentor.md) | HTML structure, CSS layout, responsive design, DevTools debugging |
| [`agents/javascript-mentor.md`](../../agents/javascript-mentor.md) | DOM scripting, event listeners, debugging JS errors, introductory SQL |
| [`agents/git-mentor.md`](../../agents/git-mentor.md) | Branching, committing, pull requests, resolving merge conflicts |

---

## Requirements

- [Visual Studio Code](https://code.visualstudio.com/) (latest)
- [GitHub Copilot extension](https://marketplace.visualstudio.com/items?itemName=GitHub.copilot)
- [GitHub Copilot Chat extension](https://marketplace.visualstudio.com/items?itemName=GitHub.copilot-chat)
- A GitHub account with Copilot access

---

## How to Load an Agent into Copilot Chat

Copilot Chat supports **custom instructions** that you paste at the start of a conversation.

### Step 1 — Open the agent file

Open the relevant file from the `agents/` folder in VS Code, for example:

```
agents/frontend-html-css-mentor.md
```

Select all the text (**Ctrl+A** / **Cmd+A**) and copy it (**Ctrl+C** / **Cmd+C**).

### Step 2 — Open Copilot Chat

Press **Ctrl+Shift+I** (Windows/Linux) or **Cmd+Shift+I** (macOS) to open the Copilot Chat panel.

### Step 3 — Paste the instructions

Start a **new conversation**, then type or paste the agent instructions as your first message. Prefix it with a short instruction to set context:

```
Please act as the following mentor for the rest of this conversation:

[paste the full contents of the agent file here]
```

Send the message. Copilot will confirm the role and you can begin asking questions.

### Step 4 — Ask your question

Now describe your problem using the format below.

---

## What to Include When Asking a Question

Good questions get better coaching. Include:

1. **The assignment** — which folder/series you're working on (e.g., `01-wireframe`, `05-cards`)
2. **Your goal** — what the code is supposed to do or look like
3. **What you've tried** — paste the relevant code snippet
4. **What happened** — describe the unexpected result or paste the error message
5. **What you've already checked** — e.g., "I checked DevTools and the element has no width"

### Example question format

```
I'm working on 04-navigation (Enhancement level).

Goal: Make the nav links sit in a horizontal row.

My CSS:
.nav-list {
  display: flex;
}

What happened: The links are still stacking vertically.

I checked: The `.nav-list` class is applied in the HTML.
```

---

## Learning Policy Reminder

> **This curriculum does not provide full solutions.**

The mentor agents are configured to give hints and ask questions — not to write your assignment code. If Copilot starts providing a complete solution, you can redirect it:

```
Please don't give me the full answer. Give me a hint or a guiding question instead.
```

This keeps the learning effective. Struggle is part of the process — the agents are here to make that struggle productive, not to remove it.

---

## Tips

- **One problem at a time** — ask about one issue per conversation for clearer guidance.
- **Follow up** — if a hint isn't clear, say "Can you explain that differently?" or "Give me a simpler example."
- **Show your work** — always paste your actual code; the agent can't help with hypotheticals.
- **Use DevTools first** — for HTML/CSS questions, open browser DevTools and inspect the element before asking. Tell the agent what you saw.
- **Use `console.log()` first** — for JS questions, log your variables before asking. Tell the agent what you saw.
- **Use `git status` first** — for Git questions, run `git status` and paste the output.
