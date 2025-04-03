<h1>
  <span class="headline">Intro to Bash Scripting Lab</span>
  <span class="subhead">Explore the <code>case</code> Statement in Bash</span>
</h1>

**Learning objective:** By the end of this lesson, students will be able to create more advanced Bash scripts by utilizing the `case` statement.

## Creating a Calculator

In this exercise, you'll create a calculator script that performs foundational arithmetic operations (addition, subtraction, multiplication, and division) using command-line arguments and the `case` statement.

## Steps

1. In your terminal application, ensure you are in the <code class="filepath">intro-to-bash-scripts-lab</code> directory.

2. Create a new file called <code class="filepath">calculator.sh</code> using the `touch` command.

3. Make the <code class="filepath">calculator.sh</code> script executable using the `chmod` command.

4. Also make it so that the script can be executed by those who clone the script from GitHub.

5. Open the new file in VS Code.

6. Add the shebang line.

7. The script should accept three command-line arguments: the first number, the arithmetic operator (`+`, `-`, `*` `/`), and a second number.

8. Research the `case` statement in Bash and use it to evaluate the arithmetic operator and perform the corresponding operation.

   > 💡 Use the `$((expression))` syntax to perform arithmetic operations within Bash. For example, `$((1 + 1))` would evaluate to `2`.

9. Print the result of the arithmetic operation to the screen.

10. Save the file and exit the text editor.

11. Execute the script with command-line arguments:

   ``` bash
   ./calculator.sh 10 + 5
   ./calculator.sh 20 - 7
   ./calculator.sh 4 \* 6
   ./calculator.sh 15 / 3
   ```

Observe how the script performs the specified arithmetic operation based on the provided command-line arguments.

## Conclusion

Congratulations! You've explored command-line arguments and created a simple calculator script. Keep practicing and experimenting with different Bash scripting concepts to enhance your skills. Remember, the more you practice, the more comfortable and proficient you'll become!

*Happy scripting!* 🎉
