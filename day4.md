# Day 4 - Package Management (Chapter 4)

## Commands learned:

- `apt-cache search` - search for packages
- `apt-get install` - install a package
- `apt-get remove` - remove package (keep config files)
- `apt-get purge` - remove package + config files
- `apt-get update` - update package list from repositories
- `apt-get upgrade` - upgrade all installed packages
- `sources.list` - file that lists repository URLs (`/etc/apt/sources.list`)
- `synaptic` - graphical package manager (install with `sudo apt-get install synaptic`)
- `git clone` - download a repository from GitHub

## Examples:

```bash
# Update package list
sudo apt-get update

# Install a tool (example: nmap)
sudo apt-get install nmap

# Remove but keep config
sudo apt-get remove nmap

# Purge completely
sudo apt-get purge nmap

# Clone a GitHub repo
git clone https://github.com/user/repo.git
```

Notes:

· Always run sudo apt-get update before install or upgrade.
· git clone is how you'll download many hacking tools from GitHub (e.g., git clone https://github.com/pi-hole/pi-hole).
· sources.list is powerful: adding new repositories gives access to more software.
