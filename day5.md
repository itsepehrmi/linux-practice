# Day 5 - [Day 5 - 12-06-2026]

## Commands learned:

- `chown` - change file owner
- `chgrp` - change group owner
- `chmod` - change permissions (read, write, execute)
- `umask` - set default permissions for new files/dirs
- `SUID` (Set User ID) - run file with owner's privileges
- `SGID` (Set Group ID) - run with group privileges
- `Sticky Bit` - only file owner can delete (on directories like /tmp)

## Examples:

```bash
# Change owner
sudo chown user1 file.txt

# Change group
sudo chgrp group1 file.txt

# chmod numeric: 7=rwx, 6=rw-, 5=r-x, 4=r--
chmod 755 script.sh   # owner: rwx, group: r-x, others: r-x

# SUID (4xxx)
chmod 4755 script.sh

# SGID (2xxx)
chmod 2755 directory/

# Sticky bit (1xxx)
chmod 1777 shared_dir/

# View umask
umask
```
Notes:

· ls -l shows permissions (e.g., -rwxr-xr-x).
· SUID on /bin/passwd lets normal users change passwords.
· Sticky bit on /tmp prevents others from deleting your files.
· Proper permissions are critical for system security.
