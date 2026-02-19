# 🤖 Copilot Agents — Setup Guide

This folder contains three custom **GitHub Copilot agents** built specifically for this curriculum. They turn Copilot into a specialised teaching assistant for HTML/CSS, JavaScript, and Git.

---

## What Are Copilot Agents?

Agents are custom AI modes you activate inside VS Code's Copilot Chat. Instead of a general-purpose assistant, each agent has a specific teaching personality, focus area, and set of guidelines.

---

## Requirements

- [Visual Studio Code](https://code.visualstudio.com/) (latest version)
- [GitHub Copilot extension](https://marketplace.visualstudio.com/items?itemName=GitHub.copilot)
- [GitHub Copilot Chat extension](https://marketplace.visualstudio.com/items?itemName=GitHub.copilot-chat)
- A GitHub account with Copilot access

---

## Installation — Two Options

### Option A: Install for Just This Project (Recommended)

VS Code will automatically discover `.agent.md` files placed in your user prompts folder.

1. Find your VS Code user prompts folder:
   - **macOS:** `~/Library/Application Support/Code/User/prompts/`
   - **Windows:** `%APPDATA%\Code\User\prompts\`
   - **Linux:** `~/.config/Code/User/prompts/`

2. Copy the three agent files into that folder:

**macOS / Linux:**
```bash
# Run this from the repository root
cp .github/copilot-agents/frontend-mentor.agent.md ~/Library/Application\ Support/Code/User/prompts/
cp .github/copilot-agents/javascript-coach.agent.md ~/Library/Application\ Support/Code/User/prompts/
cp .github/copilot-agents/git-guide.agent.md ~/Library/Application\ Support/Code/User/prompts/
```

**Windows (PowerShell):**
```powershell
$dest = "$env:APPDATA\Code\User\prompts"
Copy-Item .github\copilot-agents\frontend-mentor.agent.md $dest
Copy-Item .github\copilot-agents\javascript-coach.agent.md $dest
Copy-Item .github\copilot-agents\git-guide.agent.md $dest
```

3. Reload VS Code (Cmd+Shift+P → "Reload Window")

---

### Option B: Open Directly in VS Code

1. Open the `.github/copilot-agents/` folder in your file explorer
2. Open any `.agent.md` file in VS Code
3. Click **"Use Agent"** in the editor toolbar (if available in your version)

---

## How to Use the Agents

Once installed, open Copilot Chat in VS Code:

1. Press **Cmd+Shift+I** (macOS) or **Ctrl+Shift+I** (Windows/Linux) to open Copilot Chat
2. Click the **mode selector** (shows "Ask" or "Edit" by default)
3. Select the agent you want from the dropdown

Or type `@` in the chat input and select the agent by name.

---

## The Three Agents

### 🎨 `frontend-mentor` — HTML & CSS Teacher

**Best for:** Learning HTML structure, CSS styling, layout debugging, responsive design

**Use it when:**
- You're stuck on why your layout looks wrong
- You want feedback on your HTML structure
- You don't understand why a CSS property isn't working
- You want to learn Flexbox or Grid concepts

**Example prompts:**
```
Why is my div not centred on the page?
Can you review the HTML structure of my navigation?
How should I approach making this card responsive?
```

---

### 💛 `javascript-coach` — JavaScript Learning Coach

**Best for:** Learning JavaScript concepts, debugging JS code, understanding errors

**Use it when:**
- You get a JavaScript error you don't understand
- You want to learn a JS concept (arrays, functions, DOM, etc.)
- You're not sure how to approach a JavaScript problem
- You want hints rather than the full solution

**Example prompts:**
```
I'm getting "TypeError: cannot read properties of undefined" — help me understand it
Can you give me a hint (not the answer) for how to loop through this array?
Explain how addEventListener works with a simple example
```

---

### 🔧 `git-guide` — Git & Version Control Guide

**Best for:** Learning Git commands, fixing Git mistakes, understanding the workflow

**Use it when:**
- You're confused by a Git error message
- You accidentally committed to the wrong branch
- You have a merge conflict you don't understand
- You want to understand what a Git command actually does

**Example prompts:**
```
I committed to main by mistake — how do I fix this?
What's the difference between git fetch and git pull?
I have a merge conflict — walk me through resolving it
```

---

## Tips for Getting the Most Out of the Agents

- **Describe your goal, not just your error** — "I'm trying to make my navbar horizontal" is more useful than just pasting an error
- **Show your code** — paste the relevant HTML/CSS/JS/Git output alongside your question
- **Ask for hints before answers** — these agents are built to teach, not just solve. Ask "give me a hint" or "help me think through this"
- **Follow up** — if an explanation isn't clear, ask it to explain differently or give a simpler example

---

## Troubleshooting

**Agents don't appear in the dropdown:**
- Make sure the files are in the correct prompts folder (see paths above)
- Check the file has a `.agent.md` extension (not `.md`)
- Reload VS Code: Cmd+Shift+P → "Reload Window"

**"GitHub Copilot is not available":**
- Make sure you are signed in to GitHub in VS Code
- Verify your GitHub account has Copilot access

**The agent gives full code answers instead of teaching:**
- Remind it with: "Please guide me with hints rather than giving me the full answer"
- These agents are configured to teach, but you can always reinforce that mode
