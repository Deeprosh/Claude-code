# Claude Modes
Claude has 4 Modes
- Manual or default mode
- Edit Mode
- Plan Mode  
- Auto Mode
  
**Manual Mode**: By default, whatever you want to perform in this mode, it wont do it without our permission and it will give warning before doing or performing anything.Most safest mode.  
**Edit Mode**: In this mode, File edits are approved automatically, but commands still ask for the permission.Like if you want to execute something like to do git commit, it will do it but before executing this commit by doing the necessary changes it will ask permission.  
**Plan Mode**: It can only read and analyze.It produces the plan and once its done you can do whatever you want like to execute the plan or not.  
**Auto Mode**: In this mode, it wont ask for permissions, once you provide any instruction or prompt it will execute it directly.  

## How to customize the permissions?
Using */permissions* command we can customize the permissions
~~~
/permissions-enter
Go to deny->click on "Add a new rule"
Here you can paste the permission rule.
~~~
