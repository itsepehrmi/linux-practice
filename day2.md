# Day 2 -  Linux Basics for Hackers (Chapter 2)

Today I learned text filtering and viewing commands. These are essential for examining log files, configuration files, and output of other commands in penetration testing.

## Commands I practiced:

### Viewing file content partially
- `head` - Show first 10 lines of a file (use `-n` to specify number)
- `tail` - Show last 10 lines of a file (useful for logs; `-f` follows new lines live)
- `nl` - Display file content with line numbers

### Searching and filtering
- `grep` - Search for patterns inside files (supports regex)
- `sed` - Stream editor; find and replace text without opening the file

### Paged viewing
- `more` - View file one screen at a time (space to go forward)
- `less` - More advanced than `more`; allows backward/forward scrolling, search (`/`)

## Examples I ran:

```bash
# Create a test file
echo -e "apple\nbanana\napple pie\ncherry\napple juice" > fruits.txt

# head and tail
head -n 2 fruits.txt
tail -n 1 fruits.txt

# nl
nl fruits.txt

# grep
grep "apple" fruits.txt
grep -i "APPLE" fruits.txt   # case insensitive
grep -c "apple" fruits.txt   # count matches

# sed - replace 'apple' with 'orange'
sed 's/apple/orange/g' fruits.txt

# more / less (press q to quit)
less fruits.txt
```

Notes:

.grep is your best friend during log analysis
 (e.g., searching for"failed password"in/var/
 log/auth.log).

.tail -f is amazing for watching live logs:
 tail -f /var/log/syslog.

.sed can edit files in-place with -i
 (dangerous;test without -i first).

.always use less instead of more - it's more
 powerful and allows backward navigation.
