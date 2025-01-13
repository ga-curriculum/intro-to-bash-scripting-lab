<h1>
  <span class="headline">Intro to Bash Scripting</span>
  <span class="subhead">Level Up: Exploring Advanced Bash Scripting Concepts (Optional)</span>
</h1>

**Learning objective:** By the end of this lesson, students will be able to create more advanced Bash scripts.

If you're up for a challenge and want to explore more advanced Bash scripting concepts, try these level-up exercises.

# Level Up Exercise 1: Introducing Command-Line Arguments

In this exercise, you'll learn how to pass command-line arguments to your Bash script and use them within the script.

Command-line arguments allow you to provide input to your script directly from the command line when executing it. This enables you to create more flexible and reusable scripts that can adapt to different scenarios.

## Steps

1. Open the `first_script.sh` file in a text editor.
2. Modify the script to accept a name as a command-line argument:

``` bash
#!/bin/bash

name=$1

echo "Hello, $name!"
echo "Today is $(date)."
```

- `$1` represents the first command-line argument passed to the script.

- The value of `$1` is assigned to the variable name using the assignment operator `=`.

3. Save the file and exit the text editor.

4. Execute the script with a command-line argument

``` bash
./first_script.sh Alice
```

- Replace `Alice` with your desired name.

Observe how the script greets the person with the name provided as a command-line argument.

# Level Up Exercise 2: Creating a Calculator

In this exercise, you'll create a calculator script that performs foundational arithmetic operations using command-line arguments.

## Steps

1. Create a new file called `calculator.sh` in the `bash_scripts` directory.
2. Open the `calculator.sh` file in a text editor and add the following content:

``` bash
#!/bin/bash

num1=$1
operator=$2
num2=$3

case $operator in
    +)
        result=$((num1 + num2))
        ;;
    -)
        result=$((num1 - num2))
        ;;
    \*)
        result=$((num1 * num2))
        ;;
    /)
        result=$((num1 / num2))
        ;;
    *)
        echo "Invalid operator!"
        exit 1
        ;;
esac

echo "Result: $result"
```

- The script accepts three command-line arguments: `num1` (first number), `operator` (arithmetic operator), and `num2` (second number).

- The `case` statement is used to evaluate the `operator` and perform the corresponding arithmetic operation.
- The `$((expression))` syntax is used to perform arithmetic operations within Bash.

3. Save the file and exit the text editor.

4. Make the `calculator.sh` script executable using the `chmod` command:

``` bash
chmod +x calculator.sh
```

5. Execute the script with command-line arguments:

``` bash
./calculator.sh 10 + 5
./calculator.sh 20 - 7
./calculator.sh 4 \* 6
./calculator.sh 15 / 3
```

Observe how the script performs the specified arithmetic operation based on the provided command-line arguments.

## Conclusion

Congratulations on completing the level-up exercises! You've explored command-line arguments and created a simple calculator script. Keep practicing and experimenting with different Bash scripting concepts to enhance your skills. Remember, the more you practice, the more comfortable and proficient you'll become!

_Happy scripting!_