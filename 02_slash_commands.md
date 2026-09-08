### Slash commands :

- write a single command and do the repetable mundane task/workflow, no need to write prompt everytime 

- **2 types of slash commands : built in and custome slash commands**

- Sessions :
- A single conversation history with claude 
- **sessions are saved automatically to ~/.claude/projects/  and can be resumed whenever u want: claude -r : on ui u will see list of session go into any u want**
- each session has its own context window like for opus and sonnet 1 million tokens / session is the context window

- rename the session, instead of first ques of session being shown :
  - /rename enter_name

- Asking quick side questions about the concepts u dont know while building a feature :
  - /btw ur_question : ask question, it wont be part of main context window of this session 
  - press SPACE and this quick Q&A disappears

- exporting the entire chat in a session within the folder u are developing project :
  - /export file.md : this file will be created, i can provide this files as context to some other session 

- /logout and /login commands to logout and login in claude code account


- use opus for planning and sonnet for implementation : 

- switching models mid session : as i will be mostly switching between sonnet and opus and both have 1miliion context window, there is literally no effect on context window.

- A simple way to understand context window filling up is : i/p token + thinking + o/p token
- but its incremental , not double down for every basic question asked, thats the shit in normal api calling chatbot, prompt caching and all is also used !







