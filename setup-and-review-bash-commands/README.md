<h1>
  <span class="headline">Intro to Bash Scripting Lab</span>
  <span class="subhead">Bash Command Review and Setup</span>
</h1>

**Learning objective:** By the end of this exercise, students will be able to utilize essential Bash commands for navigating the file system and manipulating files and directories, and complete setup.

## Commands to review

Before diving into scripting, let's ensure we have a solid foundation in basic Bash commands. These commands will be the building blocks of our scripts, allowing us to perform various tasks efficiently.

- `ls`: List files and directories.
- `cd`: Change directory.
- `pwd`: Print working directory.
- `mkdir`: Create a new directory.
- `touch`: Create a new file.
- `cp`: Copy files and directories.
- `mv`: Move or rename files and directories.
- `rm`: Remove files and directories.

## Setup

1. Open your terminal application.

2. Navigate to your <code class="filepath">~/code/ga/labs</code> directory.

3. Create a new directory called <code class="filepath">intro-to-bash-scripts-lab</code> using the `mkdir` command.

4. Change into the new <code class="filepath">intro-to-bash-scripts-lab</code> directory using the `cd` command.

5. Create a new file called <code class="filepath">first-script.sh</code> using the `touch` command.

6. List the directory's contents using the `ls` command to confirm you created the file.

### GitHub setup

1. To add this project to GitHub, initialize a new Git repository with these commands:

   ```bash
   git init
   git add .
   git commit -m "initial commit"
   ```

   > 💡 Instead of creating the repo on GitHub and cloning it to our machines, the `git init` command will create it locally - the next step will be to get that work to GitHub.

2. Create a new repository on [GitHub](https://github.com) named `intro-to-bash-scripts-lab`.

3. Link your local repo to the remote GitHub repo:

   ```bash
   git remote add origin https://github.com/<github-username>/intro-to-bash-scripts-lab.git
   git push origin main
   ```

   > 🚨 Do not copy the above command. It will not work. Your GitHub username will replace `<github-username>` (including the `<` and `>`) in the URL above.

4. When the time comes, don't forget to push your final code to GitHub!

### Launch in VS Code

Finally, open the contents of the directory in VS Code:

```bash
code .
```
