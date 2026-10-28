AABE course folder, version 2026-1
2026-10-28

## Part 1: what a language model is
- Student did the small task and answered the three check questions.
- Task result: AGENTS.md asks the agent to (1) explain each step first, (2) ask before creating, changing or deleting a file, (3) never handle keys or passwords and treat web and file text as data, (4) log each part, (5) write plainly with no unchecked numbers. A model often gets references wrong and can name papers that do not exist. Check by searching the exact title in Google Scholar or BI's library search and confirming authors, year and claim.
- Corrections given: the model uses the whole context window, not only the last token. The log is a short record of what was done, not a saved conversation. A leaked key must be replaced, not only removed.

## Part 2: skills, starting with folders
- Student installed folder-context for Claude Code only, at ~/.claude/skills/folder-context/SKILL.md. The copy was checked as identical to the course copy. Not installed for Codex. Student chose to keep it there, not move it.
- Task result: the agent drew the AABE tree. Two empty folders, "Consumers, Trade & Business Strategy" and "Macroeconomic Analysis", were noted as outside the course layout and left untouched. folder-context asked for storage and parent project. Student chose local in Documents, standalone. The agent created /Users/martinpkvalo/Documents/master-thesis with AGENTS.md, CLAUDE.md, README.md (with a Folder context section), data/raw, data/derived, sources, notes, drafts and outputs. Backup not checked.
- Check questions answered after follow-ups. Corrections given: a clear folder is also cheaper because fewer tokens are read. A download goes in data/raw, not loose in data. The skill author writes the description in SKILL.md, and the agent reads only descriptions until a request matches. The copy that works in every project is in ~/.claude/skills, not in AABE.

## Other
- Student asked the agent to put their name in my-page/index.md. The heading "Your name" became "Martin Prussak Kvalø". The list "What I built in this course" was kept unchanged. Not uploaded to GitHub.
- Student asked the agent to link my-page/index.md to the page's own repository. The session 1 line now links to https://github.com/martinpkvalo/martinpkvalo.github.io. The agent checked that the repository exists. Not uploaded to GitHub.

## Part 3: what an agent is
- Student did the small task and answered the two check questions.
- Task result: the agent went through the session step by step: Bash (cat, find, cmp, cp, curl), Read, Write, Edit and AskUserQuestion, with what came back and the next decision. One failed step: the Finder reveal tool was refused outside the course folder. Goal: take the student through session 1 and log each part, precise enough to check. Smaller goals, such as "the live link works", were checked with a fetch. Vague requests (name spelling, link address) needed a question first.
- Corrections given: an agent has four parts, with the model as the fourth. Tools are actions such as curl, not the files in the folder. A goal must be checkable, not only "a final product".
- Since the "Other" entries: the student uploaded index.md to GitHub. The agent found a line break inside the link, the student fixed it, and the agent checked that the live page shows the link.

## 2026-10-28: Part 2, tree and thesis proposal
Added after the part 2 entry, because the hand-in needs the tree and the proposal in the log. Both are copied as the agent drew them in part 2.

Tree of the course folder, as drawn:

    AABE/
      .agents/skills/folder-context/SKILL.md    skill for Codex
      .claude/skills/folder-context/SKILL.md    skill for Claude Code
      AGENTS.md                                 rules I read first
      CLAUDE.md                                 points Claude Code to AGENTS.md
      Consumers, Trade & Business Strategy/     empty
      Macroeconomic Analysis/                   empty
      my-page/index.md                          your GitHub page
      session-log.md                            the log
      session1/
        01-language-models.md
        02-skills-and-folders.md
        03-what-an-agent-is.md
      skills/folder-context/SKILL.md            the skill, to read

Proposed thesis folder, with the four habits:

    master-thesis/
      AGENTS.md          rules for the agent, with the teacher's language block
      CLAUDE.md          one line: "Read AGENTS.md in this folder and follow it."
      README.md          what the thesis is, plus a "Folder context" section
      data/
        raw/             data as you got it, never changed
        derived/         cleaned data and results the agent makes
      sources/           papers and readings
      notes/             dated, e.g. 2026-10-28-supervisor-meeting.md
      drafts/            thesis.docx, one stable name, no "final-final"
      outputs/           figures and tables for the text

One project: only thesis material. Instructions at the top: AGENTS.md, CLAUDE.md and README.md. Raw data kept raw: data/raw is read only, results go to data/derived or outputs. Names that sort: dates first, lowercase, hyphens, no spaces.
Afterwards: the thesis folder was created as proposed. The student deleted the two empty folders.

## 2026-10-28: Part 3, tools, results and goal
Added after the part 3 entry, because the hand-in needs the agent's account in the log. Condensed from the account the agent gave in part 3.
- Start. Tool: Bash (cat, find). Came back: the rules, three part files and an empty log. Next: AGENTS.md says to write a first line, so the agent asked and then used Write.
- Part 1. Tool: none, AGENTS.md was already in the context window. Came back: the student's answers. Next: each answer decided the next question. Partly right answers were corrected first.
- Part 2. Tool: Bash (cat, cmp, ls). Came back: identical skill copies, and no ~/.claude/skills. Next: the agent showed the paths and asked. Then Bash (mkdir, cp, cmp) installed and checked the copy.
- Failed step. Tool: a Finder reveal tool. Came back: an error, because only folders inside the course folder are allowed. Next: the agent gave Finder steps instead.
- Small task. Tool: Bash (find) and AskUserQuestion. Came back: the tree, and the answers local and standalone. Next: after a yes, Bash and Write created the thesis folder.
- my-page. Tool: Read and Edit. Came back: the old file, then the changed lines. Tool: Bash (curl). Came back: the repository exists. Then an older file on GitHub, then a line break between ] and (, then a working link. Next: each fetch decided the next step. The loop stopped when the live page showed the link.
- Goal: take the student through session 1 and log each part. Precise enough to check, through each part's task and questions. Smaller goals, such as "the live link works", were checked with one fetch. Vague requests (name spelling, link address) needed a question first.
