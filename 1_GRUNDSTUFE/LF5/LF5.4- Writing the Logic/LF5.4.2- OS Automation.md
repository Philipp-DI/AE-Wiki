# LF5.4.2: OS Automation

<details>
<summary>Briefing</summary>

## User Story

As a System Administrator, **I** want to write basic Bash scripts, so that **I** can automate repetitive operating system tasks on Linux servers without doing them manually.

## Celebration Criteria

- **I can define** the purpose of a shebang (`#!`). (K1)
- **I know how to write** simple procedural scripts handling variables and user input. (K3)
- **I can apply** execution permissions to a file in Linux. (K3)

## Knowledge Briefing

Bash (Bourne Again Shell) is the default command-line interpreter on most Linux systems (like Ubuntu 24.04). Bash scripting is procedural programming applied directly to the operating system.

**The Anatomy of a Script:**

1. **The Shebang:** The first line must be `#!/bin/bash`. This tells Linux which interpreter to use.
2. **Variables:** `NAME="Alice"` (No spaces around the `=`). Access it with `$NAME`.
3. **Commands:** Any command you type in the terminal (like `mkdir`, `echo`, `ls`) can be put in a script.
4. **Permissions:** A text file cannot just run. You must grant it execution rights using `chmod +x script.sh`.
5. **Execution:** Run it using `./script.sh` from the current directory.

## Common Pitfalls

- Adding spaces around the equals sign when declaring variables (e.g., `VAR = "value"` will cause an error. It must be `VAR="value"`).
- Forgetting `chmod +x` and wondering why Linux says "Permission denied".

## Mandatory Tasks

1. State the exact character sequence of the Bash shebang. (K1)
2. Write the Bash code to declare a variable named `SERVER_PORT` with the value `8080`. (K3)
3. Write a two-line Bash script that outputs the text "Welcome to the system" to the terminal. (K3)
4. State the Linux terminal command required to make a file named `install.sh` executable. (K1)
5. Explain why you must execute a local script using `./script.sh` instead of just typing `script.sh`. (K2)

## Optional Tasks

1. Analyze the security risks of downloading a bash script from the internet and executing it directly with root privileges. (K4)
2. Evaluate the concept of "Exit Codes" (e.g., `exit 0` vs `exit 1`) in Bash scripting and why they are vital for automated CI/CD pipelines. (K5)
3. Design a Bash script that checks if a specific folder exists; if not, it creates it and writes a log entry with the current timestamp into a file. (K6)

## 📺 Web Search Term Liste

| Topic / Term | Recommended Platform | Exact Search Term |
| --- | --- | --- |
| Bash Scripting | YouTube | "Bash Scripting Tutorial for Beginners" |
| Linux Permissions | Studyflix / Google | "Linux chmod explained" |

</details>

:::success
➕ Outstanding submission! Your understanding of Bash scripting, permissions, and system mechanics is top-notch. Your deep dive into the security risks of `curl | bash` and the explanation of exit codes in CI/CD pipelines were highly professional. Furthermore, your Bash script for O3 is production-ready, effectively utilizing safeguards like `set -euo pipefail`. Keep up the excellent work!  
<br/>_This feedback was generated automatically._
:::

## Answers

### M1: State the exact character sequence of the Bash shebang. (K1)

The exact character sequence of the **Shebang** (derived from Hash-Bang) is `#!`. It is used at the **beginning of a script** to run the following commands with the specified interpreter. E.g. `#!/bin/bash` will run the commands and parameters afterwards in the Shell (BASH).

---

### M2: Write the Bash code to declare a variable named SERVER_PORT with the value 8080. (K3)

`SERVER_PORT=8080`

**Important note:** NO spaces around the `=`. Writing `SERVER_PORT = 8080` would make Bash try to _execute_ `SERVER_PORT` as a command with `=` and `8080` as arguments, and throw an error.

Access the value later with the `$` prefix: `echo $SERVER_PORT`.

---

### M3: Write a two-line Bash script that outputs the text "Welcome to the system" to the terminal. (K3)

```bash
#!/bin/bash
echo "Welcome to the system"
```

---

### M4: State the Linux terminal command required to make a file named install.sh executable. (K1)

`chmod +x install.sh`  
`chmod` ("change mode") with `+x` adds the **execute permission** for the file's owner, group, and others. Without it, a script will refuse to run with `Permission denied`.

---

### M5: Explain why you must execute a local script using ./script.sh instead of just typing script.sh. (K2)

When you type a bare command name, Bash searches for it in the directories listed in the `$PATH` **environment variables** (typically `/usr/bin`, `/usr/local/bin`, etc.). Your current working directory (**CWD**) is **deliberately not** on that list.

The `./` prefix means _this_ directory, right here. It tells Bash you really mean the local file and not some program with the same name elsewhere on the system or within the environment variables.

**Why this matters as a security feature:** if the current directory were searched automatically, an attacker could drop a file named `ls` or `cd` into a shared folder. When you’d work in that folder and type any of those commands, the attacker's script runs instead. Forcing `./` makes the user opt in to running a local file, which makes that whole attack class impossible.

---

### O1: Analyze the security risks of downloading a bash script from the internet and executing it directly with root privileges. (K4)

A command like `curl https://example.com/install.sh | sudo bash` could cause real harm. The only protective step before the harmful execution is the sudo password prompt. Another reason why you should always use it and never really use “complete sudo/blind mode”. With root/sudo/admin access pretty much anything could be possible:

- **No inspection before execution.** The script runs the moment it's downloaded. You have no chance to read what it does, no chance to scan it with anything, no chance to ask "should this really be deleting `/var`?" By the time you would have noticed, it has already happened - as root, with no undo.
- **Root means _everything_.** A script run via `sudo` can modify any file on the system, install kernel modules, add itself to systemd as a persistent service, plant SSH keys for backdoor access, disable security tooling, or simply `rm -rf /` and walk away. There is no sandbox.
- **Server-side cloaking.** The server can detect whether the request comes from a human browser or from `curl`, and serve a _different_ script to each. A reviewer who opens the URL in Firefox sees a clean install script. The same URL piped to `bash` delivers the malicious payload. There is a documented proof-of-concept for this (curlpipe.com) - it is not theoretical.
- **Man-in-the-middle on transit.** If the URL is plain `http://` (or HTTPS with a compromised Certificate Authority (CA)), anyone on the network path - hotel Wi-Fi, ISP, compromised proxy - can swap the script's contents in flight. The user sees a normal-looking command and types `y` to the sudo prompt.
- **Supply-chain compromise.** Even if the source you trust is legitimate today, its server could be compromised tomorrow, or the maintainer could turn malicious. This is the same class of risk as the 2024 XZ Utils backdoor - trusted upstream, malicious payload injected over time.

**Safer alternatives:**

- Download first, read, _then_ run: `curl -O https://...` → inspect → `bash ./install.sh`. NO pipe.
- Use the distro package manager (`apt`, `dnf`, `pacman`) where possible - packages are signed and verifiable.
- Verify checksums or GPG signatures published independently of the script itself.
- Run unknown scripts in a throwaway container or VM first.

_Source(s): cisa.gov; owasp.org._

---

### O2: Evaluate the concept of "Exit Codes" (e.g., exit 0 vs exit 1) in Bash scripting and why they are vital for automated CI/CD pipelines. (K5)

**Table from** [**tldp.org**](https://tldp.org/LDP/abs/html/exitcodes.html)**:**

| Exit Code No. | Meaning | Example | Comments |
| --- | --- | --- | --- |
| 0   | Success | ls  |     |
| 1   | Catchall for general errors | let "var1 = 1/0" | Miscellaneous errors, such as "divide by zero" and other impermissible operations |
| 2   | Misuse of shell builtins (according to Bash documentation) | empty_function() {} | [Missing keyword](https://tldp.org/LDP/abs/html/debugging.html#MISSINGKEYWORD) or command, or permission problem (and [_diff_ return code on a failed binary file comparison](https://tldp.org/LDP/abs/html/filearchiv.html#DIFFERR2)). |
| 126 | Command invoked cannot execute | /dev/null | Permission problem or command is not an executable |
| 127 | "command not found" | illegal_command | Possible problem with \$PATH or a typo |
| 128 | Invalid argument to [exit](https://tldp.org/LDP/abs/html/exit-status.html#EXITCOMMANDREF) | exit 3.14159 | **exit** takes only integer args in the range 0 - 255 (see first footnote) |
| 128+n | Fatal error signal "n" | _kill -9_ \$PPID of script | **\$?** returns 137 (128 + 9) |
| 130 | Script terminated by Control-C | _Ctl-C_ | Control-C is fatal error signal 2, (130 = 128 + 2, see above) |
| 255\* | Exit status out of range | exit \-1 | **exit** takes only integer args in the range 0 - 255 |

**Every command, script, and function returns an exit code** when it finishes. You can inspect the most recent one with `$?`:

```bash
ls /nonexistent
echo $?      # prints 2
```

**Chaining commands by exit code:**

```bash
make build && make test && make deploy   # each step runs only if the previous succeeded
backup.sh || alert.sh            # alert runs only if backup failed
```

**Why CI/CD lives or dies on this convention:**

A CI/CD pipeline (GitHub Actions, GitLab CI, Jenkins, etc.) doesn't read your script's output to decide whether it worked. It reads the exit code of the last command. The single line in your pipeline configuration:

```yaml
- run: ./run-tests.sh
```

succeeds or fails entirely based on whether `run-tests.sh` exits `0` or non-zero. From this single signal, the pipeline decides whether to:

- proceed to the next stage (build → test → deploy),
- mark the commit as green or red in the pull request,
- send the deployment to production,
- page the on-call engineer.

This kind of fast feedback makes or brakes Continuous Integration.

**The common failure mode** is a script that catches an error, logs it nicely, and then exits `0` anyway. The pipeline thinks everything succeeded; the broken code gets deployed. This is why production-grade Bash scripts almost always start with:

```bash
#!/bin/bash
set -euo pipefail
```

- `-e` exit on the first failing command
- `-u` exit on unset variables
- `-o pipefail` propagate failure through pipes (so `false | true` exits non-zero)

Without these, Bash would silently swallow errors and lie to the CI.

---

### O3: Design a Bash script that checks if a specific folder exists; if not, it creates it and writes a log entry with the current timestamp into a file. (K6)

```bash
#!/bin/bash
set -euo pipefail

# --- Configuration -----------------------------------------------------------
TARGET_DIR="/var/folder_created"
LOG_FILE="${TARGET_DIR}/folder-creation.log"

# --- Logic -------------------------------------------------------------------
if [ -d "$TARGET_DIR" ]; then
    echo "[$(date '+%Y-%m-%d %H:%M:%S')] Folder already exists: $TARGET_DIR"
    exit 0
fi

# Folder does not exist - create it (parents too, if needed)
mkdir -p "$TARGET_DIR"

# Write the log entry with an ISO-8601-style timestamp
TIMESTAMP="$(date '+%Y-%m-%d %H:%M:%S')"
echo "[${TIMESTAMP}] Created folder: ${TARGET_DIR}" >> "$LOG_FILE"

echo "Done. Logged to ${LOG_FILE}"
```

**What each piece does:**

- `set -euo pipefail`: The safety harness. The script aborts on any error instead of stumbling forward.
- `[ -d "$TARGET_DIR" ]`: The `-d` test returns `true` only if the path exists _and_ is a directory. Quoting `"$TARGET_DIR"` prevents word-splitting if the path contains spaces.
- `mkdir -p`: The `-p` flag means "create parent directories as needed, and do not error if the directory already exists." It is a defensive practice that prevents the script from crashing.
- `date '+%Y-%m-%d %H:%M:%S'`: Produces a sortable timestamp (e.g., `2026-05-22 14:30:05`). ISO-style is preferred over local-format dates because log entries sort correctly as plain text.
- `>> "$LOG_FILE"`: The double `>>` operator appends to the file instead of overwriting it (using a single `>` would erase all prior entries on every run).

**Example output in** `/var/folder_created/folder-creation.log`**:**Plaintext

```
[2026-05-22 14:30:05] Created folder: /var/folder_created
```

**Possible extensions:**

_(Not implemented above)_

- **Pre-flight checks**: Verify write permissions before attempting `mkdir`.
- **System logging**: Send the log line to `syslog` as well via the `logger` command.
- **CI/CD Integration**: Exit with a distinct non-zero code if `mkdir` fails, allowing a calling CI job to detect and report the failure.