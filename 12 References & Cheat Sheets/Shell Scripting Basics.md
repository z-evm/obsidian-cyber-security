**Shell scripting** automates tasks in Unix/Linux environments using command-line interpreters like `bash`, `sh`, `zsh`, or `fish`. Scripts streamline administration, automate security checks, and support DevSecOps workflows.

---

## 🔍 What is a Shell Script?

A **shell script** is a plain text file containing a series of shell commands. These are executed sequentially by the shell interpreter.

> 🔧 File Extension: `.sh`  
> 📄 Shebang (first line): `#!/bin/bash`

---

## 🧬 Anatomy of a Shell Script

```bash
#!/bin/bash

# This is a comment
echo "Hello, world!"      # Print text
name="Alice"              # Define variable
echo "User: $name"        # Use variable

if [ "$name" = "Alice" ]; then
  echo "Welcome Alice!"
fi

for file in *.txt; do
  echo "File: $file"
done
```

## 💡 Core Concepts

### 📦 Variables
```
user="bob"
echo $user
```

### 🔄 Conditionals
```
if [ "$user" = "admin" ]; then
  echo "Admin access"
else
  echo "Access denied"
fi
```

### 🔁 Loops
```
for i in 1 2 3; do
  echo "Number: $i"
done

while true; do
  echo "Infinite loop"
  break
done
```

### 🔧 Functions
```
greet() {
  echo "Hi, $1"
}

greet Alice
```

## 🔐 Security Use Cases

|Use Case|Description|
|---|---|
|**Automate Updates**|Schedule patching with `cron` + scripts|
|**Log Parsing**|Analyze logs for anomalies|
|**User Auditing**|Report users with sudo/root access|
|**Backup Tasks**|Scheduled file or DB backups|
|**Security Hardening**|Enforce firewall rules or permissions|

---

## 🛡 Best Practices

- Always start scripts with a **shebang** (`#!/bin/bash`)
- Use `set -e` to exit on error
- Quote all variables (`"$var"`) to prevent word splitting
- Avoid hardcoding secrets in scripts
- Use `chmod +x script.sh` to make the script executable
- Test with `bash -x script.sh` (debug mode)

---

## 🔧 Execution Methods

```
# Method 1: Direct execution
./script.sh

# Method 2: With interpreter
bash script.sh

# Method 3: Scheduled with cron
crontab -e
0 3 * * * /home/user/scripts/backup.sh
```

## 📂 File Permissions

|Command|Description|
|---|---|
|`chmod +x`|Make script executable|
|`chown`|Change script ownership|
|`ls -l`|View permissions and owners|

---

## 🧠 Related Topics

- [[Environment Variables]]
- [[Cron Jobs & Task Scheduling]]
- [[Linux File Permissions Cheat Sheet]]
- [[Command Line Tools for Security]]
- [[Log Analysis]]

---

## 🏷 Suggested Tags

#shell #bash #scripting #linux #automation #devops #sysadmin #security_basics

---

## ✅ To Do

-  Create cheat sheet of common bash commands
    
-  Add reusable functions for log parsing and user audit
    
-  Include common pitfalls (e.g., missing quotes, unescaped input)