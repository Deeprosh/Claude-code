# Calude.md file and memory  
Claude.md file is created by the command /init  

A file named CLAUDE.md at the root of your project is read at the start of each session there. It typically contains:  

What the project is and how it is structured  
Build, test, and lint commands  
Code style rules and naming conventions  
Things Claude keeps getting wrong that you want to correct permanently  

**Context**: The messages that you typed everything is considered as Context.Content within the respository.  
**Token**: Token is 3/4th of the word.  

*Hooks*: Hook is used to prevent the sensitive things.These are defined at various levels
- Pre-tool hook executes before claude tries to run a command.  
- Post-tool hoook executes post successfull command execution.
- User prompt hook will verify when user sends a message before the model sees it.It will verify if there is any sensitive kind of information before submitting it.
- 
**How to configure a hook?**
  - Create .claude folder-->move to that folder-->create a settings.json file and edit the file with hook commands.
  
~~~
{
  "hooks": {
    "PostToolUse": [
      {
        "matcher": "Edit|Write",
        "hooks": [
          {
            "type": "command",
            "command": "npx prettier --write \"$CLAUDE_FILE_PATHS\""
          }
        ]
      }
    ]
  }
}
~~~
