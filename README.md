<p align="center">
  <img src="https://img.shields.io/badge/Simple_Shell-ALX_Holberton-blue?style=for-the-badge&logo=gnu-bash" alt="Simple Shell">
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

## 🌌 Why another Shell?

Unix shells have powered tech for decades. This isn't just any shell—it's your shell. Handcrafted from scratch, using pure C and Linux syscalls. No shortcuts, no built-in libraries, no training wheels.



---

## 🛠️ Hardcore Features

- 🔥 Execute commands interactively and non-interactively.
- 🔗 Command chaining: `&&`, `||`, `;`.
- 🧬 Built-ins: `exit`, `env`, `cd`, `alias`, `setenv`, `unsetenv`, `history`, `help`.
- 🧠 Variable replacement (`$?`, `$$`, `$VARIABLE`).
- 🌎 Complete environment variable handling.
- 📜 Persistent command history management.
- 🦾 Bulletproof error handling and memory management.
- 🚦 Signal handling (Ctrl+C interrupts).
- ⚙️ No `system()` calls—pure `fork()`, `execve()`.

---

## 🧩 Built-ins & Examples

```bash
✨ $ cd /usr/bin
✨ $ alias greet='echo Hello, ALX!'
✨ $ greet
Hello, ALX!

✨ $ setenv MY_VAR "Holberton"
✨ $ echo $MY_VAR
Holberton

✨ $ history
1 cd /usr/bin
2 alias greet='echo Hello, ALX!'
3 greet
4 setenv MY_VAR "Holberton"
5 echo $MY_VAR

✨ $ help
✨ $ exit

🌟 Quick Demo
Run commands directly:
./hsh
$ ls -la
$ echo "Unix Wizardry"

Pipe commands into the shell:
echo "pwd" | ./hsh

🚧 Project Structure (Behind the Magic)
.
├── 📂 builtins/
│   ├── builtins.c (exit, cd, help)
│   └── builtins2.c (alias, history)
├── 📂 env/
│   ├── env.c
│   └── environ.c
├── 📂 core/
│   ├── shell.c (main shell loop)
│   └── parser.c (command parsing, PATH lookup)
├── 📂 utils/
│   ├── utils.c (string manipulation & utilities)
│   ├── tokenizer.c (tokenizes commands)
│   └── input.c (input handling & signals)
├── 📂 memory/
│   ├── info.c (memory management)
│   └── history.c (command history)
├── 📂 vars/
│   └── vars.c (variable replacement logic)
├── 📄 shell.h (definitions and prototypes)
└── 📜 man_1_simple_shell (manual page)

📖 Manual Page (Unix style!)
man ./man_1_simple_shell
💡 Design Choices (Why it's awesome)
💪 Efficiency: Direct Linux syscalls, avoiding overhead.

🦅 Portability: Runs smoothly on any Unix-based OS.

🔥 Control: No external libs—every byte is yours.

🛡️ Robustness: Meticulously checked with Valgrind—no leaks.

🌠 Extensible: Easy to add your custom built-ins and commands.

🎯 Tests & Validation
✅ Valgrind leak-free certification

✅ Manual tests covering edge cases

✅ ALX compliance (gcc -Wall -Werror -Wextra -pedantic -std=gnu89)

🙌 Authors & Contributors
Built with ❤️ & caffeine by:

Muhannad — @Muhannad-09
Abdulaziz - @Abdulaziz-Saleh1

<p align="center"> <strong>💻 Code. 🧠 Learn. 🚀 Conquer.</strong> <br><br> <img src="https://media.giphy.com/media/QTfX9Ejfra3ZmNxh6B/giphy.gif" width="200"> </p> ```
