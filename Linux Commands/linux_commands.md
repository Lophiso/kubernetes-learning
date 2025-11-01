# 🐧 Essential Linux Commands for Tech Enthusiasts (Ubuntu-Friendly)

This document collects essential and frequently used Linux commands — tailored for a **tech enthusiast** and **Internet & Multimedia Engineer**. It includes system operations, file management, software installation, network tools, and developer utilities.

---

## 🗂️ File and Directory Management
```bash
ls                 # List files and directories
ls -la             # List all files including hidden ones
pwd                # Print current working directory
cd <dir>           # Change directory
cd ..              # Go up one directory
mkdir <dir>        # Create a new directory
rmdir <dir>        # Remove an empty directory
rm -rf <dir>       # Remove a directory and its contents
cp <src> <dest>    # Copy file or directory
mv <src> <dest>    # Move or rename file/directory
cat <file>         # Display file content
nano <file>        # Open and edit file using nano editor
xdg-open <file>    # Open file using the default app
xdg-open .         # Open current directory in file manager
```

---

## 📂 File Opening Commands
```bash
xdg-open report.pdf       # Open PDF
xdg-open video.mp4        # Open video
xdg-open song.mp3         # Open audio
xdg-open picture.jpg      # Open image

# Specific apps
evince file.pdf            # GNOME PDF viewer
okular file.pdf            # KDE PDF viewer
vlc video.mp4              # Video/music player
totem video.mp4            # GNOME Videos
```

---

## 💻 System Information and Management
```bash
uname -a                  # Display Linux system info
lsb_release -a            # Display Ubuntu version
df -h                     # Show disk usage
free -h                   # Show memory usage
top                       # View running processes
htop                      # Enhanced process viewer (if installed)
whoami                    # Display current user
id                        # Show user ID and groups
uptime                    # Show how long the system has been running
history                   # Show command history
```

---

## 🔧 Software Installation and Updates
```bash
sudo apt update                          # Update package lists
sudo apt upgrade                         # Upgrade all packages
sudo apt install <package_name>          # Install a package
sudo apt remove <package_name>           # Remove a package
sudo apt autoremove                      # Remove unused dependencies
sudo snap install <package_name>         # Install via Snap
sudo snap refresh <package_name>         # Update Snap package
```

### Example: Install Brave Browser
```bash
# Step 1: Add Brave’s repository key
sudo apt install curl -y
sudo curl -fsSLo /usr/share/keyrings/brave-browser-archive-keyring.gpg https://brave-browser-apt-release.s3.brave.com/brave-browser-archive-keyring.gpg

# Step 2: Add repository
echo "deb [signed-by=/usr/share/keyrings/brave-browser-archive-keyring.gpg] https://brave-browser-apt-release.s3.brave.com/ stable main" | sudo tee /etc/apt/sources.list.d/brave-browser-release.list

# Step 3: Install Brave
sudo apt update
sudo apt install brave-browser -y

# Alternative (Snap)
sudo snap install brave
```

---

## 🌐 Network Commands
```bash
ping <host>                   # Check network connection
ifconfig                      # Display network interfaces (use ip a in new systems)
ip a                          # Show IP addresses
netstat -tuln                 # List listening ports
curl <url>                    # Fetch data from a URL
wget <url>                    # Download a file from the internet
traceroute <host>             # Trace network route
dig <domain>                  # DNS lookup
nslookup <domain>             # DNS query
```

---

## 🧰 Package & Process Utilities
```bash
ps aux                        # Show all processes
kill <pid>                    # Kill a process by PID
killall <process_name>        # Kill process by name
sudo systemctl start <svc>    # Start a service
sudo systemctl stop <svc>     # Stop a service
sudo systemctl restart <svc>  # Restart a service
sudo systemctl status <svc>   # Check service status
```

---

## 🧾 Permissions and Ownership
```bash
chmod 755 <file>              # Give owner full access, others read/execute
chmod +x <file>               # Make file executable
chown <user>:<group> <file>   # Change file ownership
sudo                         # Run a command as administrator
```

---

## 🧱 System Navigation & Shortcuts
```bash
clear                        # Clear terminal screen
ctrl + c                     # Cancel running command
ctrl + l                     # Shortcut for clear
ctrl + r                     # Search command history
!!                            # Repeat last command
```

---

## 💡 About `xdg`
`xdg` = **cross-desktop group** → standard utilities to interact with desktop environments.

Examples:
```bash
xdg-open file.pdf             # Open file in default app
xdg-mime query filetype file.pdf  # Get MIME type
xdg-settings get default-web-browser  # Get default browser
xdg-email someone@example.com      # Open email app
```

---

## 🧮 Developer & Power User Essentials
```bash
git --version                 # Check git version
git clone <repo_url>          # Clone repository
python3 --version             # Check Python version
python3 <script>.py           # Run Python script
code .                        # Open VS Code in current directory
sudo apt install build-essential  # Install compilers and dev tools
```

---

## 🧠 Pro Tip
Use `man <command>` to open the manual page for any command, e.g.:
```bash
man ls
```

---

## 🏁 Summary
You can always extend this document as you explore Linux more deeply — add sections for Docker, Kubernetes, or networking as you progress in your engineering journey.

---

**Author:** Naol Hassen  
**Purpose:** Centralized Linux Command Reference for GitHub Accessibility  
**System:** Ubuntu (24.04 LTS Recommended)

