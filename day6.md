# Day 6 - Process Management & Job Control (Chapter 6)

## Commands learned:

- `ps` - show running processes (snapshot)
- `ps aux` - show all processes with details
- `top` - real-time process viewer
- `msfconsole` - Metasploit framework launcher (hacking tool)
- `nice` - start a process with a priority level (-20 to 19)
- `renice` - change priority of an existing process
- `kill` - send signals to processes (e.g., kill -9 PID)
- `fg` - bring a background job to foreground
- `at` - schedule a one-time task at a specific time

## Examples:

```bash
# See all processes
ps aux

# Run a process with low priority (10)
nice -n 10 ./script.sh

# Change priority of PID 1234 to 15
sudo renice 15 -p 1234

# Force kill a process
kill -9 1234

# Put a process in background with &
./long_task.sh &

# Bring job 1 to foreground
fg 1

# Schedule a command at 3pm today
at 15:00
at> echo "Reminder" >> /tmp/note
at> Ctrl+D
```

Notes:

. ps aux is your first step for finding
  suspicious processes.
. msfconsole loads Metasploit; you'll use it
  later for exploitation.
. nice/renice are useful when you don't want
  a tool to slow down your system.
. at is simpler than cron for one-time tasks.
