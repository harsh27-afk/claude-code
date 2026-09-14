- use @src/main.py , the @ symbol to mention files, so that claude can refer to exact file we want it too see

- for big projects its not possible to refine ur raw prompts with some other web llm like chatgpt (because it also needs to have context to form prompt, which is an issue), so just be raw in such cases

## Context Window :

- **context window and usage are 2 seperate things, sonnet and opus has 1 million context window , both context window gets filled incrementally , like if u are at 200k tokens and ask new question, so the Q and A the new ones are only added to context window not the entire 200k previous tokens again making it 400k !!**


- if u use a big session for coding and tomorrow u restart the session then it will be bit costly to catcup, the context window remains same though, so the TTL for cache is 1 hr after u close the session  using /quit 

- staying within the context window while working on big code base is a skill


## Key Points Regarding Context Window :

- each new session gets a fresh context window 

#### Most Imp Point :

- **as the terminal agent is sending entire previous conversation history every time u ask it do something, so its better to make seperate sessions for each feature , that way u will consume very less tokens !! but to give context to new sessions , create .md file, so that new session can get idea/ overview of what happened coding wise in previous session !!**

- **Bigger context windows give not so good o/p** 

- u can spawn sub-agents for specific tasks u want, sub-agents have their own context windows and they return a summary to the main agent !!

- u dont get full empty 1 million token context window, so part is already occupied by things like 
  - System Prompt 6k defined by anthropic team
  - Tool Schemas 8k 
  - claude.md tiny
  - skills + mcp  , etc
  - auto-compact 33k

- /context : to look at current sessions context info


---------------------------------------------------------------------------------------------------------------

## Auto-compaction :

- **once ur session`s C.W reaches 95% of 1 million limit ( for sonnet and opus ) , claude summarizes session in 33k tokens reserved , then ur C.W becomes significantly empty and starts again from system_prompt + tools + ... + 33k reserved tokens !!**

- **but the o/p is pretty bad hence forth, so its better once ur session CW reaches 900k tokens, just form another .md file summarizing**

- I am at 500k tokens still want to compact the session : 
  - **command :/compact focus on keeping the auth refactor decisions and drop the file exploration**

**One of the imp points below !!**

- **I am at 500k tokens i ask a new question , so now 500k + new asked question tokens are sent to the llm , so is there any limit to how much i/p we can send to the LLM ?? yes the ans is C.W itself !!! u cant send more tokens at a time than the context window length !! thats the reason auto-compaction thing exists !!!**


-----------------------------------------------------------------------------------------------------------------

- To make sure claude code does not read ur personal files like env or unneccessay bulky folder 
  - .claude/settings.json 
  -   {
  "permissions": {
    "deny": [
      "Read(.env)",
      "Read(secrets/**)",
      "Read(*.pem)"
    ]
  }
}


 









