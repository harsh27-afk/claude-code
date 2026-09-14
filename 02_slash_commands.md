### Slash commands :

- write a single command and do the repetable mundane task/workflow, no need to write prompt everytime 

- **2 types of slash commands : built in and custome slash commands**

- type / to see all /commands in terminal

- Sessions :
- A single conversation history with claude 

- **sessions are saved automatically to (global directory): ~/.claude/projects/  and can be resumed whenever u want: claude -r : on ui u will see list of session go into any u want**

- **There are 2 locations where /.claude folders are created: global and local project root folder :**

- Project .claude/ (in your repo root)
  - Holds : CLAUDE.md, settings.json, skills, rules, agents — configuration, not history
  - Created when : You run /init, save a local setting, add a skill, etc.

- Global ~/.claude/ (in your home dir) 
  - Holds : Your personal config + all session transcripts across every project
  - Created When : The very first time you ever run claude on your machine

  - Session History is stored at : global ~/.claude/projects/<encoded-project-path>/<session-id>.jsonl

- each session has its own context window like for opus and sonnet 1 million tokens / session is the context window

- rename the session, instead of first ques of session being shown :
  - /rename enter_name

- Asking quick side questions about the concepts u dont know while building a feature :
  - /btw ur_question : ask question, it wont be part of main context window of this session 
  - press SPACE and this quick Q&A disappears

- **exporting the entire chat in a session within the folder u are developing project :**
  - /export file.md : this file will be created, i can provide this files as context to some other session 
  - This will contain the entire chat history message, it will not be the summarized context we use in Context engineering / spec driven development 

- /logout and /login commands to logout and login in claude code account


- use opus for planning and sonnet for implementation : 

- switching models mid session : as i will be mostly switching between sonnet and opus and both have 1miliion context window, there is literally no effect on context window.

- A simple way to understand context window filling up is : i/p token + thinking + o/p token
- but its incremental , not double down for every basic question asked, thats the shit in normal api calling chatbot, prompt caching and all is also used !


---------------------------------------------------------------------------------------

```markdown

/resume - Select and resume a session, can also use `claude -r`
/model - View and change models during a session
/exit - Exit a session
/btw - Chats not taken into context, runs parallely to current tasks
/usage - Shows daily and weekly usage & limits
/stats - Shows useful usage beahviour statistics
/extra-usage - To top up when tokens run out
/insights - Provides html to improve your workflow, current project, usage etc. Nitish recommends this after 10 to 15 sessions
/config - Lets you tweak claude settings
/permissions - Allow, ask or deny permissions given to claude agent, read,write, terminal access etc.
/voice - Enable voice mode 


```





