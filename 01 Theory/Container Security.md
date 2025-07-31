**Container security** focuses on protecting the entire container lifecycle—from image creation to runtime orchestration. Containers introduce new attack surfaces through misconfigurations, vulnerable images, and unregulated inter-container communication.

> 🧠 *Secure once, defend always—container security begins at the Dockerfile and never ends.*

---

## 🔄 Container Lifecycle Phases & Security Concerns

| Phase         | Security Focus                                   |
|---------------|--------------------------------------------------|
| **Build**     | Image hardening, dependency control              |
| **Ship**      | Image signing, scanning, and provenance          |
| **Deploy**    | Least privilege, network segmentation            |
| **Run**       | Runtime controls, monitoring, and alerting       |
| **Decommission** | Image cleanup, credential rotation           |

---

## 🧱 Container Security Risks

| Category          | Example Vulnerability / Risk                         |
|-------------------|------------------------------------------------------|
| **Insecure Images** | Use of outdated, vulnerable base images             |
| **Secrets in Images**| Hardcoded API keys, passwords in Dockerfiles      |
| **Privilege Escalation**| Containers running as root                     |
| **Misconfigured Runtime**| Overly permissive host mounts, capabilities   |
| **Container Breakouts** | Escaping container isolation to host (e.g., CVE-2019-5736) |
| **Uncontrolled Networking**| Open ports, unencrypted traffic             |

---

## 🛡 Container Hardening Best Practices

### 🔨 Build-Time Security

- Use minimal base images (e.g., `distroless`, `alpine`)
- Regularly update dependencies and base layers
- Never store secrets in images or ENV variables
- Pin versions in package managers
- Use multi-stage builds to remove tools not needed at runtime

### 🚢 Image Management

- Scan images with tools like **Trivy**, **Grype**, **Anchore**
- Sign images using **Cosign**, **Notary**, or **Sigstore**
- Enforce policies via **OPA** or **Kyverno**

### 🔐 Runtime Security

- Run containers as **non-root**
- Drop unneeded Linux capabilities (`--cap-drop`)
- Use read-only filesystems where possible
- Limit resource usage with **cgroups**
- Isolate network namespaces
- Use AppArmor, SELinux, or seccomp profiles

---

## 🧰 Container Security Tools

| Function         | Tools                                |
|------------------|--------------------------------------|
| **Image Scanning** | Trivy, Clair, Anchore, Grype        |
| **Runtime Security** | Falco, Sysdig Secure, AppArmor     |
| **Policy Enforcement** | Kyverno, OPA Gatekeeper, PodSecurityPolicy |
| **Image Signing** | Cosign, Notary, Sigstore             |
| **CI/CD Integration** | Docker Bench, Dockle, Checkov     |

---

## ☁️ Orchestrator Security (Kubernetes)

- Use **RBAC** to limit access to pods, secrets, and namespaces
- Isolate workloads in separate namespaces
- Disable default service account tokens
- Protect the Kubernetes API server (e.g., via mTLS)
- Audit with tools like **Kube-Bench**, **Kube-Hunter**
- Enable network policies to restrict inter-pod communication

---

## 🔁 Compliance & Governance

- Enforce CIS Benchmarks for Docker & Kubernetes
- Maintain SBOMs (Software Bill of Materials) for all images
- Integrate SAST/DAST tools into container-based workflows
- Regularly review and rotate secrets (use Vault, Doppler, Sealed Secrets)

---

## 🧩 Related Topics

- [[DevSecOps Pipeline]]
- [[Infrastructure as Code (IaC) Security]]
- [[Secure API Design Guidelines]]
- [[Kubernetes Security]]
- [[Runtime Threat Detection]]

---

## 🏷 Tags

#containersecurity #docker #kubernetes #runtime #devsecops #trivy #falco #imagehardening #opa #cloudnative #dockersecurity #supplychain

