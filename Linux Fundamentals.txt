# Linux Fundamentals

## 1. File System Navigation
`pwd`: Print Working Directory. Shows the absolute path of the current directory.
`ls`: List directory contents. Common flags: `-l` (long format), `-a` (all files including hidden), `-h` (human-readable sizes).
`cd`: Change Directory. `cd /path/to/dir` moves to that directory. `cd ..` moves up one level. `cd ~` moves to the home directory.

## 2. File & Directory Permissions
Permissions Structure: Read (r=4), Write (w=2), Execute (x=1). Grouped as Owner, Group, Others.
`chmod`: Change Mode. Modifies file permissions.
  Example: `chmod 755 file.txt` (Owner: rwx, Group: rx, Others: rx).
  Example: `chmod +x script.sh` (Make executable).
`chown`: Change Owner. Changes the file owner and group.
  Example: `chown user:group file.txt`.

## 3. Package Management (Debian/Ubuntu based)
`apt`: Advanced Package Tool. High-level package management.
  `sudo apt update`: Updates package lists.
  `sudo apt install <package>`: Installs a package.
  `sudo apt upgrade`: Upgrades installed packages.
`dpkg`: Debian Package. Low-level tool to install .deb files.
  `sudo dpkg -i package.deb`: Install a local .deb file.

## 4. Networking Commands
`ifconfig` (or `ip addr`): Displays network interface configuration (IP address, MAC address).
`ping`: Checks connectivity to a host. `ping google.com`.
`netstat`: Network Statistics. Shows network connections, routing tables, interface statistics.
  Example: `netstat -tuln` (TCP, UDP, Listening, Numeric).
`traceroute`: Traces the path packets take to a network host.
