<h1>
  <span class="headline">Intro to Bash Scripting Lab</span>
  <span class="subhead">Bash Script Structure and Creation</span>
</h1>

**Learning objective:** By the end of this lesson, students will explore the essential components of a Bash script and utilize command-line arguments and variables in a script.

## Components of a Bash Script

Let's explore the structure of a Bash script. A Bash script is essentially a plain text file containing a series of commands executed sequentially. Scripts have these components:

1. **Shebang line**: The first line of a Bash script should start with `#!/bin/bash`. This line, known as the *shebang*, tells the system which interpreter to use when executing the script. In this case, it specifies that the script should be run by the Bash shell as indicated by `/bin/bash`.

2. **Comments**: Comments are used to add explanatory notes or document your script. In Bash, comments start with the `#` symbol (except for the shebang line). Anything after `#` on a line is considered a comment and is ignored by the interpreter.

3. **Commands**: The main body of the script consists of a series of commands executed in the order they appear. These commands can be any valid Bash commands, including the ones we reviewed, like `ls` and `cd`.

## Write your first Bash script

Let's write our first script! We'll create a script that greets the user and displays the current date and time.

> 🧠 If you encounter problems along the way, check out the **Troubleshooting** section at the bottom of this page!

1. Add the shebang line at the top of the file:

   `first-script.sh`

   ```bash
   #!/bin/bash
   ```

2. Add a comment below the shebang line to describe the purpose of the script. For example:

   `first-script.sh`

   ```bash
   # This is my first Bash script!
   ```

3. Below the shebang line and comment, we'll add a few `echo` commands. The `echo` command is used to display text on the screen. The argument (the text within double quotes) after the command is the message to be displayed. Write the following commands, and we'll explain them afterward:

   `first-script.sh`

   ``` bash
   echo "This is my Bash script!"
   echo "Hello, $(whoami)!"
   echo "Today is $(date)."
   ```

   - The first `echo` command displays exactly what is written in the quotes - `This is my Bash script!`.

   - The second command will display the text `Hello,` followed by the username of the current user. This is accomplished by adding `$(whoami)` to the command. This is called *command substitution*.

     Command substitution works by replacing the command specified within the `$( )` with the output of the command - in this case, the username of the current user.

   - The third command will display the text `Today is` followed by the current date and time, again by using command substitution to replace `$(date)` with the output of the `date` command.

4. Ensure the file is saved.

## Executing your Bash script

Congratulations on writing your first Bash script! Now, let's make it executable and run it from the command line.

1. Return to your terminal. You should still be in the <code class="filepath">intro-to-bash-scripts-lab</code> directory. If you're not, navigate back to it.

2. Make the <code class="filepath">first-script.sh</code> file executable using the `chmod` command:

   ``` bash
   chmod +x first-script.sh
   ```

   The `chmod` command is used to change the permissions of a file.

   - The `+x` option adds execute permissions to the file.
   - The `first-script.sh` argument specifies the file to modify.

   > ⚠️ This does not make the script executable for those that clone the repository. They will need to run the `chmod` command themselves, or you can run a git command to enable execute permissions for anyone that clones the repository from GitHub: `git add --chmod=+x ./first-script.sh`. Run this command now.

3. Execute the script by running the following command:

   ``` bash
   ./first-script.sh
   ```

   The `./` before the script name tells the system to look for the script in the current directory.

Congratulations! You've just created and executed your first Bash script. You should see the greeting message and the current date and time displayed in the terminal.

Using command substitutions, we can dynamically include the output of other commands within our script. This allows us to create more dynamic and informative scripts that adapt to different situations.

## Command-line arguments

Just like the `chmod` and `echo` commands we've used so far, we can also pass arguments to our script when executing it from the command line. These arguments can be used within the script to perform different actions based on the input provided.

Command-line arguments allow you to provide input to your script directly from the command line when executing it. This enables you to create more flexible and reusable scripts that can adapt to different scenarios.

In this exercise, you'll learn how to pass command-line arguments to your Bash script and use them within the script.

1. Return to VS Code and modify the <code class="filepath">first-script.sh</code> script to accept a command-line argument for the user's name:

   `first-script.sh`

   ``` bash
   #!/bin/bash

   echo "This is my Bash script!"
   echo "Hello, $1!"
   echo "Today is $(date)."
   ```

   - The `$1` variable represents the first command-line argument passed to the script. It will be replaced with the value provided when executing the script.

   > 💡 Multiple arguments can be passed to a script. The second argument will be represented by the `$2` variable, the third by the `$3` variable, and so on.

2. Ensure the file is saved.

3. Return to the command line and execute the script with a command-line argument:

   ``` bash
   ./first-script.sh Alice
   ```

   Replace `Alice` with your desired name.

   Observe how the script greets the person with the name provided as a command-line argument. Cool!

## Variables

Wouldn't it be nice if we could refer to the user's name using something more descriptive than `$1`? We can use variables to store values and refer to them by name in our scripts:

1. Return to VS Code and modify the <code class="filepath">first-script.sh</code> script to accept a command-line argument for the user's name:

   `first-script.sh`

   ``` bash
   #!/bin/bash

   name=$1

   echo "This is my Bash script!"
   echo "Hello, $name!"
   echo "Today is $(date)."
   ```

   - The `name=$1` line assigns the value of the first command-line argument to a variable called `name`.

   - The `$name` variable is then used in the `echo` command to display the user's name. Variables in Bash are referenced by prefixing the variable name with a `$`.

2. Ensure the file is saved.

3. Return to the command line and execute the script with a command-line argument:

   ``` bash
   ./first-script.sh Alice
   ```

   Replace `Alice` with your desired name.

   Observe how the script greets the person with the name provided as a command-line argument. Cool!

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
