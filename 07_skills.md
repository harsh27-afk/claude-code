## Skills in Agentic coding :

- wanna get high quality output on specialized tasks !!

- skills are reusable file based resource with domain specific expertise context which helps general llm give high quality output 

- where skills live :
  - .claude/skills/review_skill.md 

  - skills are automatically loaded when time comes for that specific task

```

.claude/skills/
├── security-review/
│   ├── SKILL.md
│   └── checklist.md
├── deploy/
│   └── SKILL.md
├── pdf-extract/
│   ├── SKILL.md
│   ├── extract_text.py
│   └── templates/
│       └── summary.html
└── csv-analyze/
    ├── SKILL.md
    ├── analyze.py
    └── utils/
        └── parser.py

```

- SKILL.md is mandatory name , also it cant be : skills/frontend/deploy/SKILL.md

- /skill k andar ek folder usme SKILL.md and supporting files !! Allowed as per now

- u can call skills explicity just like custom slash commands !!

/pdf-extract

- supporting files play a huge role , u can add the scripts and all here 