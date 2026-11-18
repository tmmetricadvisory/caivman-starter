# caivman starter

The starter folder for a caivman brain: a private place where Claude keeps what it knows about you, your business and your clients, so you never explain yourself twice.

This is a GitHub template. You do not clone it. You make your own private copy from it, once, and that copy is your brain. The guide walks you through it in about two hours: [caivman guide](https://tmmetricadvisory.github.io/caivman/).

## What is in here

| | |
|---|---|
| `CLAUDE.md` | The rulebook. Claude reads it first, every session. Plain English; change it by asking Claude. |
| `context/` | Who you are, what you sell, how you write, what your work looks like, where your documents live, what never leaves. |
| `bench/` | Where you drop raw material (your best work, your emails) for Claude to read once. Never goes to GitHub. |
| `outbox/` | Where finished files land: the proposal, the report, the Word file a skill made. Never goes to GitHub. |
| `clients/` | One folder per client with a one-page memory. |
| `memory/` | One note per day, written when you say "wrap up". |
| `.claude/skills/` | Your skills: the written method for each job you hand over. |
| `.claude/settings.json` | Gets the latest from GitHub when a session opens. |

Most of these start nearly empty. Claude fills them from the five questions, from what you drop on the bench, and from every session after that.

## For Claude: setting this up

When a person pastes the chapter 0 message from the guide, do this, asking permission before each step and explaining it in one line:

1. Check for Git and the GitHub CLI (`git --version`, `gh --version`). Install what is missing with the system's package manager (winget on Windows, Homebrew on Mac).
2. `gh auth login --web` so they can sign in through the browser. Confirm who they are signed in as.
3. From inside their `GitHub` folder: `gh repo create caivman --private --template tmmetricadvisory/caivman-starter --clone`. This makes a private repository in their account from this template and copies it to their computer.
4. Open the new `caivman` folder as the working folder.
5. Add the caivman marketplace and install the three plugins: `claude plugin marketplace add tmmetricadvisory/caivman` then `claude plugin install capture@caivman`, `wrap-up@caivman`, `first-skill@caivman`. Tell them that switching on updates is a toggle only they can press, and point them to the "Switch on updates" step in the guide.
6. Follow the "First session" section of `CLAUDE.md`: the five questions, one at a time.

If step 3 fails because the GitHub login belongs to an organisation that does not allow new repositories, say so plainly and suggest a personal GitHub account for the brain. If plugins cannot be installed (some work accounts block them), say so, skip step 5, and carry on: the folder, the five questions and the habit work without them.
