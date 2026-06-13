# Day 7 - Managing User Environment Variables (Chapter 7)

Environment variables are dynamic values that affect how programs and processes behave in Linux. They're crucial for configuring your hacking environment.

## Key Commands & Concepts:

- `env` - Show all environment variables
- `set` - Show all variables (including shell functions)
- `export` - Make a variable available to child processes
- `$VARIABLE` - Access the value of a variable (e.g., `echo $HOME`)
- `PATH` - Critical variable that tells the shell where to find executables
- `PS1` - Defines your command prompt's appearance
- `HISTSIZE` - Controls how many commands Bash remembers in the current session history list. Default is usually 500 or 1000. Setting `HISTSIZE=2000` increases it; setting `HISTSIZE=-1` removes the limit entirely (though this can impact performance).

## Practical Examples:

```bash
# View all environment variables
env

# Check specific variable (e.g., user's home directory)
echo $HOME
Output: /home/kali

# Add a custom directory to PATH temporarily
export PATH=$PATH:/my/custom/scripts

# Verify it's added
echo $PATH

# Change your shell prompt to show current directory
export PS1='\w $ '

# Check current history size limit
echo $HISTSIZE
```

Notes:

· PATH is everything in hacking. If a command isn't found, it's usually a PATH issue.
· Adding directories to PATH allows you to run your own scripts from anywhere.
· export is essential when writing scripts that call other scripts.
· HISTSIZE is often forgotten, but it's critical for not losing command history in longer sessions; it's a silent lifesaver.
