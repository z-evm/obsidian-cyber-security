**Container Escape** is a critical vulnerability where an attacker breaks out of a containerized environment to access the **host system or other containers**. Since containers share the same host kernel, a successful escape can lead to **full system compromise** in poorly configured environments.

---

## 🎯 Why Container Escape Matters

- 🚨 Breaks the **isolation promise** of containers
- 🔓 Grants attacker access to **host resources**
- 📦 Enables **pivoting to other containers**
- 🔥 Impacts **multi-tenant platforms** and CI/CD pipelines

---

## 🧱 How Container Escape Works

| Step                     | Description                                                 |
|--------------------------|-------------------------------------------------------------|
| 1. **Initial Access**     | Attacker compromises a container (e.g., via vulnerable app) |
| 2. **Privilege Escalation**| Exploits container or kernel misconfiguration              |
| 3. **Escape Execution**   | Breaks into host or interacts with host kernel interfaces   |
| 4. **Lateral Movement**   | Accesses other containers or host system resources          |

---

## 🧪 Common Escape Techniques

| Method                     | Description                                                     |
|----------------------------|-----------------------------------------------------------------|
| **Privileged Containers**  | Container runs with elevated host permissions (e.g., `--privileged`) |
| **Mounted Host Paths**     | Sensitive host directories mounted inside the container (e.g., `/proc`, `/etc`) |
| **Kernel Exploits**        | Uses a vulnerability in the shared host kernel                 |
| **cgroup or namespace flaws** | Escapes via misconfigured Linux control groups              |
| **Docker Socket Abuse**    | Exploits mounted Docker socket (`/var/run/docker.sock`)        |

---

## ☠️ Notable Container Escape CVEs

| CVE                 | Description                                       |
|---------------------|---------------------------------------------------|
| **CVE-2019-5736**   | `runc` vulnerability enabling arbitrary code exec on host |
| **CVE-2022-0492**   | Exploit in Linux kernel cgroups allowing privilege escalation |
| **Dirty Pipe (CVE-2022-0847)** | Allows overwriting read-only files, used in container escapes |

---

## 🛡️ Mitigation Strategies

| Strategy                      | Description                                                    |
|-------------------------------|----------------------------------------------------------------|
| **Use Least Privilege**       | Avoid `--privileged`, drop unnecessary Linux capabilities       |
| **Read-only Root Filesystems**| Prevent filesystem tampering                                   |
| **Do Not Mount Sensitive Paths**| Avoid mounting host `/proc`, `/sys`, `/docker.sock`           |
| **Namespace Isolation**       | Use `user`, `pid`, and `network` namespaces                    |
| **Keep Kernel Updated**       | Patch frequently to prevent known escape exploits              |
| **Use Container Security Tools** | Tools like AppArmor, SELinux, Seccomp, gVisor, Kata Containers|

---

## 🧰 Container Security Tools

| Tool              | Function                                |
|-------------------|------------------------------------------|
| **AppArmor / SELinux** | Mandatory Access Control for containers |
| **gVisor / Kata**   | Sandbox container runtimes with extra isolation |
| **Docker Bench**    | Security audit for Docker hosts         |
| **Falco**           | Runtime threat detection for containers |
| **Trivy / Clair**   | Static vulnerability scanning           |

---

## ☁️ Cloud Context

- **Kubernetes** workloads are especially vulnerable without **Pod Security Policies**, **Admission Controllers**, and **RBAC**.
- Cloud providers offer managed runtime protections:
  - AWS: EKS Runtime Protection
  - GCP: GKE Autopilot + Binary Authorization
  - Azure: Defender for Containers

---

## 🧩 Best Practices for Hardening Containers

- 🛑 Never run as `root` inside the container
- ✅ Set `readOnlyRootFilesystem: true` in Kubernetes
- 🚫 Avoid hostPath mounts unless absolutely necessary
- 🔒 Use non-default seccomp and AppArmor profiles
- 🧼 Scan images for vulnerabilities before deployment

---

## 📎 Related Topics

- [[Virtual Machine Escape (VM Escape)]]
- [[Hypervisor Security]]
- [[Kubernetes Security]]
- [[Pod Security Policies (PSPs)]]
- [[Runtime Threat Detection]]

---

## 🏷 Tags

#containerescape #containers #kubernetes #docker #runtime #sandboxing #Security+
