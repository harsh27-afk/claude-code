## CLAUDE.md file :

- This file lives in project folder root, its an optional file

- This file is automatically read by the agent, no need to explicitly mention it

- Run : /init : claude will scan ur entire project and create this file , edit this as u wish
   - contains project structure, commands to run project, architecture , etc

- **There are 2 locations where /.claude folders are created: global and local project root folder :**

- Project .claude/ (in your repo root)
  - Holds : CLAUDE.md, settings.json, skills, rules, agents — configuration, not history
  - Created when : You run /init, save a local setting, add a skill, etc.

- Global ~/.claude/ (in your home dir) 
  - Holds : Your personal config + all session transcripts across every project
  - Created When : The very first time you ever run claude on your machine

  - Session History is stored at : global ~/.claude/projects/<encoded-project-path>/<session-id>.jsonl

- **Both contain configurations like /skills , /commands, /agents ,etc**

- A lot of different folders wihtin a project can contain CLAUDE.md file , when agent works in them, these are automatically read !!

