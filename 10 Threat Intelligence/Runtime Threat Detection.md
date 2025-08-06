**Runtime Threat Detection** refers to monitoring and analyzing system behavior in real-time to detect malicious activity, policy violations, or anomalies. It complements static and pre-deployment scans by identifying **active threats** during application and infrastructure execution.

> 🧠 *You can’t secure what you don’t monitor—runtime is where real-world threats emerge.*

---

## 🎯 Why Runtime Detection Is Critical

- Detects **zero-day exploitation**, insider abuse, and lateral movement
- Captures activity not visible during CI/CD or IaC scanning
- Provides **real-time alerts** and audit logs for forensic response
- Essential for **container, VM, and serverless workloads**

---

## 🧱 Detection Surfaces

| Layer               | Threat Examples                          |
|---------------------|-------------------------------------------|
| **Host/OS**         | File tampering, unexpected processes       |
| **Container Runtime** | Escape attempts, root execs, shell spawning |
| **Kubernetes**      | Unauthorized `kubectl exec`, privilege abuse |
| **Cloud Platform**  | IAM privilege escalation, token exfiltration |
| **Application Layer** | Webshell injection, command execution   |

---

## 🔐 Behavioral Detection Techniques

### 🔍 Signature-Based Detection
- Known rules for specific exploits (e.g., CVEs)
- Tools: Falco rules, Suricata

### 🧠 Anomaly-Based Detection
- Detects deviations from learned normal behavior
- May use ML/behavioral baselining (UEBA)

### 📜 Policy Violation Detection
- Detects when a security policy is violated
- Example: container runs as root, host mounts in pod

---

## 🛠 Runtime Threat Detection Tools

| Tool          | Category           | Features                                    |
|---------------|--------------------|---------------------------------------------|
| **Falco**     | OSS runtime monitor| Syscall-level detection, container/K8s aware|
| **Sysdig Secure** | Commercial     | Runtime security + forensics                |
| **AppArmor / SELinux** | Kernel policy | Enforce execution boundaries               |
| **Auditd**    | Linux auditing     | Tracks file access, process creation        |
| **CrowdStrike / SentinelOne** | EDR | Host & cloud workload protection            |
| **Wazuh**     | SIEM + HIDS        | Host-level rules and alerting               |

---

## 🧪 Sample Falco Rules

```yaml
- rule: Unexpected SSH Connection
  desc: Detects SSH access to container
  condition: container and evt.type = execve and proc.name = ssh
  output: "SSH inside container (user=%user.name container=%container.id)"
  priority: WARNING
```

## 🔄 CI/CD & DevSecOps Integration

- Monitor deployed workloads post-pipeline
- Alert on policy violations in staging/prod
- Feed alerts into:
    - Slack / PagerDuty
    - SIEM (Splunk, ELK, Wazuh)
    - SOAR tools for auto-remediation

---

## 🔍 Best Practices

- Write custom rules for app-specific behavior
- Tune out false positives with baselines
- Enable audit logging in:
    - Kubernetes API server
    - Cloud IAM activities
- Regularly update detection rules (e.g., new CVEs)

---

## 🧩 Related Topics

- [[Container Security]]
- [[Kubernetes Security]]
- [[SIEM & SOAR]]
- [[Policy as Code (OPA & Kyverno)]]
- [[Incident Response Planning (IRP)]]

---

## 🏷 Tags

#runtimedetection #falco #sysdig #edr #anomalydetection #containers #kubernetes #siem #devsecops #policyviolation #threatdetection