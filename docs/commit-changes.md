# Committing changes

## Finishing an exercise or assignment

If you finish an exercise or assignment you need to update the repositories [README.md](../README.md) file. You need to update the ❌ into an ✔️ indicating that you finished that particular exercise or assignment.

## Committing changes using git

Changes can be committed and pushed back to GitHub using the terminal.

Traverse to your local `web-essentials-practical-<username>` directory and type `powershell` in the location bar as done previously in [section Get started](./get-started.md).

1. Add all changed files: `git add .`
2. Commit the files and add a message: `git commit -m "My message goes here"`
3. Push your changes to GitHub: `git push origin master`
  ![Committing and pushing via PowerShell](./img/commit_push_powershell.png)
4. To make sure all is well, you can always issue the command `git status`, even in between other commands.

You can also navigate to your GitHub page of this repo and check if all went well.

Make it a habit of committing regularly. At least after solving each assignment.
