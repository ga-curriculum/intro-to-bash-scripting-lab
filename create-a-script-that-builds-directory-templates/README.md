<h1>
  <span class="headline">Introduction to Bash Scripting Lab</span>
  <span class="subhead">Create a Script That Builds Directory Templates</span>
</h1>

**Learning objective:** By the end of this exercise, students will be able to create a Bash script that builds a directory structure for a project.

## Create a new script

You now know enough to create a new script from scratch! Start with some setup:

1. Working in the <code class="filepath">intro-to-bash-scripts-lab</code> directory, create a new file called <code class="filepath">build-project.sh</code> using the `touch` command.

2. Open the file in VS Code.

3. Add the shebang line.

4. Ensure the file can be executed, both for yourself and for anyone that might clone this script from GitHub.

### Add functionality

In this exercise, you'll create a script that automates the process of building a directory structure for a bash script project. The script will take a single command line argument - this will be the name of the project.

> 🧠 Remember, if you encounter problems along the way, check out the **Troubleshooting** section at the bottom of this page!

When the script is run, it should do the following:

1. Create a new directory that matches the name of the project.

2. Move into the new directory.

3. Create a new file called <code class="filepath">README.md</code> in the new directory. If you used this template to build an actual script, this file would briefly describe the project and any important information about how to use it.

4. Create a new file that matches the project's name in the new directory and give it the `.sh` extension to specify that it is a script file. If you used this template to build an actual script, this file would contain the main script code.

5. Initialize a new Git repository in the project directory.

6. Make the new script file executable, both for yourself, and for anyone that might clone this script file from GitHub.

Test out the script and confirm it does what you want!

Don't forget to push your new script to GitHub when you're done:

```bash
git add .
git commit "add build-project.sh script"
git push origin main
```

> 🚀 Optionally, take this script a bit further - prefill the `README.md` file with the name of the project as a heading, and add the shebang line to the script file so that it's ready to be used.

## Troubleshooting

If you encounter any issues while working on this lab, here are a few troubleshooting tips:

1. **If you receive a `permission denied` error when executing the script**:

   - Make sure you have added execute permissions to the script using the `chmod +x` command.

   - Verify that you are using the correct path to the script file when executing it.

2. **If the script doesn't execute or displays an error message**:

   - Double-check the shebang line (`#!/bin/bash`) at the top of your script.

   - Make sure it is spelled correctly and has no spaces before or after it.

   - Check for any syntax errors in your script, such as missing quotation marks or incorrect command usage.

3. **If the script execution hangs or takes a long time**:

   - Ensure that your script doesn't contain any infinite loops or long-running commands that may cause it to hang.

   - If you suspect a command is causing the issue, try running that command separately in the terminal to see if it behaves as expected.

Remember, troubleshooting is a valuable skill in Bash scripting. Don't be discouraged if you encounter challenges along the way. With practice and persistence, you'll develop the ability to identify and resolve issues effectively!
