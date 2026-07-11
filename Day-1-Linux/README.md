# 🐧 Day 1 - Linux Fundamentals for ASIC Physical Design

Understanding Linux is the first step toward working with Electronic Design Automation (EDA) tools. Most ASIC design tools, including Synopsys ICC2, PrimeTime, Design Compiler, and Cadence Innovus, are primarily used in Linux environments.

---

# 📚 Objectives

By the end of this session, I was able to:

- Understand the Linux operating system
- Navigate the Linux terminal
- Manage files and directories
- Learn essential shell commands
- Prepare the Linux environment for ASIC Physical Design tools

---

# 🖥️ Why Linux in VLSI?

Linux is the industry-standard operating system for semiconductor companies because it provides:

- High stability
- Better performance
- Powerful command-line utilities
- Automation using Shell and TCL scripts
- Easy integration with EDA tools
- Efficient resource management

---


# 📌 Frequently Used Linux Commands

## Navigation Commands

| Command | Description |
|----------|-------------|
| `pwd` | Print current working directory |
| `ls` | List files and directories |
| `ls -l` | Detailed list |
| `ls -a` | Show hidden files |
| `cd` | Change directory |
| `cd ..` | Move one directory up |
| `cd ~` | Go to home directory |

---

## Directory Commands

| Command | Description |
|----------|-------------|
| `mkdir` | Create directory |
| `rmdir` | Remove empty directory |
| `rm -r` | Remove directory recursively |

Example

```bash
mkdir ASIC_Workshop
cd ASIC_Workshop
```

---

## File Commands

| Command | Description |
|----------|-------------|
| `touch` | Create file |
| `cp` | Copy files |
| `mv` | Move or rename files |
| `rm` | Delete file |
| `cat` | Display file contents |
| `less` | View large files |
| `head` | Display first few lines |
| `tail` | Display last few lines |

Example

```bash
touch notes.txt
cat notes.txt
```

---

## Search Commands

| Command | Description |
|----------|-------------|
| `find` | Search files |
| `grep` | Search text inside files |
| `locate` | Locate files quickly |
| `which` | Find executable location |

Example

```bash
find . -name "*.v"
```

---

## Permission Commands

| Command | Description |
|----------|-------------|
| `chmod` | Change permissions |
| `chown` | Change ownership |
| `whoami` | Display current user |

Example

```bash
chmod 755 script.sh
```

---

## Process Commands

| Command | Description |
|----------|-------------|
| `ps` | Display running processes |
| `top` | System monitor |
| `kill` | Terminate process |

---

## Useful Utility Commands

| Command | Description |
|----------|-------------|
| `clear` | Clear terminal |
| `history` | Display command history |
| `date` | Show current date |
| `echo` | Print text |
| `man` | Display command manual |

Example

```bash
history
man ls
```

---

# 📁 Working with Files

Create a directory

```bash
mkdir PD_Workshop
```

Move into the directory

```bash
cd PD_Workshop
```

Create a file

```bash
touch lab1.txt
```

Display current directory

```bash
pwd
```

List files

```bash
ls -l
```

---

# 💻 Environment Variables

Display PATH

```bash
echo $PATH
```

Display current user

```bash
whoami
```

Display hostname

```bash
hostname
```

---

# 🛠 Linux in ASIC Physical Design

Linux is used throughout the ASIC design flow for:

- Running synthesis
- Running ICC2
- Launching PrimeTime
- Managing design databases
- Executing TCL scripts
- Automating repetitive tasks
- Running verification tools

---

# 💡 Best Practices

- Organize project directories clearly.
- Use meaningful file names.
- Keep regular backups of design data.
- Learn keyboard shortcuts to improve productivity.
- Use scripts to automate repetitive tasks.

---

# 📖 Key Takeaways

- Learned basic Linux commands.
- Understood Linux directory structure.
- Practiced file and directory management.
- Learned command-line navigation.
- Prepared the Linux environment for EDA tools.

---

# 🚀 Next Topic

➡️ **Day 2 – Design Planning**

The next module introduces Design Planning, where chip dimensions, utilization, and floorplan constraints are established before placement and routing.

# 📚 Workshop Navigation

➡️ [Day-2-Design_Planning](../Day-2-Design_Planning/)

