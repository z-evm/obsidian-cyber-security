**Environmental Variables** are dynamic values stored in an operating system's runtime environment, used by the shell and applications to configure behavior and access system-specific information.

They are commonly used in **scripts, security policies, development environments**, and **system configurations**.

---

## 🧭 Purpose of Environmental Variables

- Control **application behavior** (e.g., logging levels, environment modes)
- Specify **paths** to executables or resources
- Store **secrets** (tokens, keys, passwords) in memory
- Allow for **cross-platform scripting and automation**
- Facilitate **secure configuration** in containerized/cloud environments

---

## 🖥 Examples of Common Variables

| Variable         | Description                                     |
|------------------|-------------------------------------------------|
| `PATH`           | Directories to search for executables           |
| `HOME` / `USERPROFILE` | User’s home directory                    |
| `TEMP` / `TMP`   | Temporary file storage path                     |
| `SHELL`          | Default shell (e.g., `/bin/bash`)               |
| `USERNAME`       | Current user ID                                 |
| `PWD`            | Present working directory                       |
| `LANG`           | Default language/locale                         |
| `EDITOR`         | Default CLI text editor                         |

---

## 🔐 Security Implications

| Concern                    | Risk Description                                      |
|----------------------------|-------------------------------------------------------|
| **Privilege Escalation**   | Malicious variables can hijack system behavior        |
| **Secret Leakage**         | Storing sensitive keys/tokens in plaintext variables  |
| **Injection Attacks**      | Unsanitized variables used in scripts/commands        |
| **Misconfigurations**      | Incorrect variables cause insecure or broken states   |

> ❗ Example: An attacker sets a fake `PATH` to run a malicious script instead of a real binary.

---

## 🛡 Best Practices

- Do **not hard-code secrets** in scripts; use secure secret management tools.
- Sanitize and validate environment variable inputs.
- Restrict user ability to modify environment in privileged contexts.
- Use `.env` files **with caution** — especially in shared environments.
- Audit for exposed variables in process dumps (`ps`, `procfs`, logs).

---

## 📦 In Container & Cloud Environments

| Use Case               | Description                                                                 |
|------------------------|-----------------------------------------------------------------------------|
| **Docker**             | `ENV` directive sets variables in container builds                         |
| **Kubernetes**         | Variables defined in `env:` section of deployment YAML files               |
| **Secrets Management** | Use services like AWS Secrets Manager, Vault, Azure Key Vault              |
| **CI/CD Pipelines**    | Store and pass variables via GitHub Actions, GitLab CI, Jenkins, etc.      |

---

## 🔧 Viewing and Setting Variables

### 🐧 Linux/macOS

```bash
printenv           # list all variables
echo $HOME         # show value
export VAR=value   # set a variable
unset VAR          # remove variable
```

### 🪟 Windows CMD/PowerShell

```
set                # list variables (CMD)
echo %TEMP%        # access variable (CMD)
$env:USERNAME      # access variable (PowerShell)
[Environment]::SetEnvironmentVariable("VAR", "value", "User")  # set (PowerShell)
```

## 🧠 Related Topics

- [[Shell Scripting Basics]]
- [[Secure Coding Practices]]
- [[Container Security]]
- [[Secrets Management]]
- [[Access Control]]
- [[Process Injection]]

---

## 🏷 Suggested Tags

#environment_variables #security #shell #devops #configuration #privilege_escalation #secrets

---

## ✅ To Do

-  Document `.env` file handling in secure DevOps pipelines
-  Add secret injection examples with HashiCorp Vault
-  Create sample attack lab: PATH hijacking via env var