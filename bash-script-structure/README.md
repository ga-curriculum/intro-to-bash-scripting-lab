<h1>
  <span class="headline">Intro to Bash Scripting</span>
  <span class="subhead">Understanding the Structure of a Bash Script</span>
</h1>

**Learning objective:** By the end of this lesson, students will learn about the essential components of a Bash script and understand their purpose. Then you'll write and execute a simple Bash script that greets the user and displays the current date and time.

Now that we've reviewed the common commands, let's explore the structure of a Bash script. A Bash script is essentially a plain text file containing a series of commands that are executed sequentially.

## Components of a Bash Script

1. **Shebang line:** The first line of a Bash script should start with #!/bin/bash. This line, known as the "shebang," tells the system which interpreter to use when executing the script. In this case, it specifies that the script should be run by the Bash shell.

2. **Comments:** Comments are used to add explanatory notes or document your script. In Bash, comments start with the # symbol (except for the shebang line). Anything after # on a line is considered a comment and is ignored by the interpreter.

3. **Commands:** The main body of the script consists of a series of commands that are executed in the order they appear. These commands can be any valid Bash commands, including the ones we reviewed.

## Practice

1. Open the `first_script.sh` file in a text editor.

2. Add the shebang line `#!/bin/bash` at the top of the file.

3. Add a comment below the shebang line to describe the purpose of the script, e.g., `# This is my first Bash script`.

4. Save the file and exit the text editor.

# Your First Bash Script

Let's write our first script! We'll create a script that greets the user and displays the current date and time.

## Steps

1. Open the `first_script.sh` file in a text editor.
2. Below the shebang line and comment, add the following commands:

``` bash
echo "Hello, $(whoami)!"
echo "Today is $(date)."
```

- The `echo` command is used to display text on the screen.
- `$(whoami)` is a command substitution that returns the current user's username.
- `$(date)` is a command substitution that returns the current date and time.

3. Save the file and exit the text editor.

# Executing Your Bash Script

Congratulations on writing your first Bash script! Now, let's make it executable and run it from the command line.

## Steps

1. Open a terminal and navigate to the bash_scripts directory.
2. Make the `first_script.sh` file executable using the `chmod` command:

``` bash
chmod +x first_script.sh
```

- The `chmod` command is used to change the permissions of a file.
- The `+x` option adds execute permissions to the file.

3. Execute the script by running the following command:

``` bash
./first_script.sh
```

- The `./` before the script name tells the system to look for the script in the current directory.

Congratulations! You've just created and executed your first Bash script. You should see the greeting message and the current date and time displayed in the terminal.

# Command Explanation and Logic

Let's break down the commands used in our script and understand the logic behind them:

**`echo "Hello, $(whoami)!"`:**

- The echo command prints the specified text to the screen.
`$(whoami)` is a command substitution that executes the `whoami` command and returns the current user's username. The resulting username is inserted into the greeting message.

**`echo "Today is $(date)."`:**

- Similar to the previous command, `echo` prints the specified text to the screen.
`$(date)` is a command substitution that executes the `date` command and returns the current date and time. The resulting date and time are inserted into the message.

By using command substitutions, we can dynamically include the output of other commands within our script. This allows us to create more dynamic and informative scripts that adapt to different situations.
