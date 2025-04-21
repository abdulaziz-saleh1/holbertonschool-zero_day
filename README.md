<p align="center">
  <img src="https://img.shields.io/badge/Simple_Shell-_Holberton-blue?style=for-the-badge&logo=gnu-bash" alt="Simple Shell">
  <br><br>
  <img src="https://media.giphy.com/media/WoWm8YzFQJg5i/giphy.gif" width="300">
</p>

<h1 align="center">🚀 simple_shell: Rewriting Unix History</h1>

<p align="center">
  <em>✨ A handmade Unix command interpreter built entirely in C ✨</em>
  <br>
  <strong>"Forget Bash. Build your own."</strong>
</p>

---

## 🧠 Project Objectives

By the end of this project, you will be able to:
- Explain how a Unix shell works.
- Distinguish between `pid` and `ppid`.
- Implement system calls like `fork`, `execve`, `wait`, and more.
- Parse and tokenize input commands.
- Handle environment variables programmatically.
- Execute processes and manage them.
- Use file descriptors for redirections.
- Understand PATH lookup.
- Detect and handle EOF.
- Appreciate the difference between library and system calls.

---

## 🛠️ Features

- 🔥 **Interactive & Non-Interactive Mode**
- 🧠 **Built-ins**: `exit`, `env`, `cd`, `setenv`, `unsetenv`, `alias`, `history`, `help`
- 💡 **Variable Replacement**: `$?`, `$$`, `$VAR`
- 📂 **Environment Handling**: getenv, setenv, unsetenv
- 🧮 **Command History**: Save and display previous commands
- 🔗 **Command Chaining**: `&&`, `||`, `;`
- 🧠 **Memory-Safe**: Valgrind tested
- 🚦 **Signal Handling**: Ctrl+C interrupt
- ⚙️ **No `system()` calls** — only `fork`, `execve`, etc.

---

## ✨ Built-ins Example

```bash
$ cd /usr/bin
$ alias greet='echo Hello, ALX!'
$ greet
Hello, ALX!

$ setenv MY_VAR "Holberton"
$ echo $MY_VAR
Holberton

$ history
1 cd /usr/bin
2 alias greet='echo Hello, ALX!'
3 greet
4 setenv MY_VAR "Holberton"
5 echo $MY_VAR

$ help
$ exit
```

### 🧪 Testing Examples
```bash
# Interactive mode
./hsh
($) /bin/ls
($) exit

# Non-interactive
echo "/bin/ls" | ./hsh
cat commands.txt | ./hsh
```

---

## 🗃️ File Structure
```
📁 simple_shell
├── 📁 builtins
│   ├── builtins.c       → handles exit, cd, help
│   └── builtins2.c      → handles alias, history
├── 📁 env
│   ├── env.c            → env handlers
│   └── environ.c        → custom getenv, setenv, unsetenv
├── 📁 core
│   ├── shell.c          → main shell loop
│   ├── parser.c         → tokenizing, PATH resolution
│   ├── input.c          → reading lines, signals
│   └── info.c           → struct & memory mgmt
├── 📁 utils
│   ├── utils.c          → helpers (strlen, isalpha, etc)
│   ├── tokenizer.c      → string split logic
│   └── vars.c           → variable logic
├── history.c            → handles command history
├── shell.h              → prototypes, macros, struct
├── man_1_simple_shell   → manual page (type `man ./man_1_simple_shell`)
```

---

## 🧪 Testing & Requirements

✅ **Memory Leak-Free**: Checked with Valgrind  
✅ **Complies with Holberton Style**: `gcc -Wall -Werror -Wextra -pedantic -std=gnu89`  
✅ **Manual & Automated Testing**: Interactive and pipe input modes

### 📜 Manual Page
Run: `man ./man_1_simple_shell`

---

## 💻 Requirements
- Ubuntu 20.04 LTS
- No memory leaks (Valgrind must pass)
- 5 functions max per file
- Betty style & documentation
- Use only allowed system calls

---

## 📚 System Calls Used
`access`, `chdir`, `close`, `execve`, `exit`, `_exit`, `fflush`, `fork`, `free`, `getcwd`, `getline`, `getpid`, `isatty`, `kill`, `malloc`, `open`, `opendir`, `perror`, `printf`, `fprintf`, `read`, `readdir`, `signal`, `stat`, `lstat`, `fstat`, `strtok`, `wait`, `waitpid`, `wait3`, `wait4`, `write`

---

## 🙌 Authors
- **Muhannad** — [@Muhannad-09](https://github.com/Muhannad-09)
- **Abdulaziz** — [@Abdulaziz-Saleh1](https://github.com/Abdulaziz-Saleh1)

<p align="center">
  <strong>💻 Code. 🧠 Learn. 🚀 Conquer.</strong>
  <br><br>
  <img src="https://media.giphy.com/media/QTfX9Ejfra3ZmNxh6B/giphy.gif" width="200">
</p>

