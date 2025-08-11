**Kubernetes (K8s)** is a powerful container orchestration platform—but its complexity and flexibility make it a high-value target. Securing a Kubernetes environment requires hardening at every layer: clusters, nodes, workloads, networking, and access control.

> 🧠 *“Secure by default” does not apply to Kubernetes—every layer must be explicitly hardened.*

---

## 🧱 Kubernetes Security Domains

| Domain         | Focus Area                                           |
|----------------|------------------------------------------------------|
| **Control Plane** | API server, scheduler, etcd, controller manager    |
| **Node Security** | Kubelet, container runtime, OS-level hardening     |
| **RBAC & IAM**    | Role-based access control and user permissions     |
| **Network Security** | Pod communication, ingress/egress, network policies |
| **Workload Security** | Pod/container configs, secrets, image validation |
| **Supply Chain**   | CI/CD pipelines, image signing, provenance         |

---

## 🔐 Core Security Best Practices

### 🔑 1. **RBAC and Access Control**

- Enable **RBAC** and audit role bindings
- Use **least privilege** principles
- Disallow default service account token mounts:
  ```yaml
  automountServiceAccountToken: false
```

### 🔏 2. **Pod & Container Hardening**

- Avoid running as root:
```
securityContext:
  runAsNonRoot: true
```

- Use `readOnlyRootFilesystem: true`
- Drop unnecessary capabilities with `capDrop`
- Set resource limits (CPU, memory)

### 🔐 3. **Network Security**

- Apply **NetworkPolicies** to restrict traffic between pods
- Disable kube-proxy forwarding open ports to the internet
- Encrypt traffic between pods using service mesh (e.g., Istio, Linkerd)

### 📦 4. **Supply Chain Security**

- Scan container images with **Trivy**, **Grype**, or **Clair**
- Use signed images with **Cosign** / **Sigstore**
- Validate manifests against policy engines (OPA, Kyverno)

### 🧪 5. **Secrets Management**

- Avoid storing secrets in ConfigMaps
- Use external secrets providers: HashiCorp Vault, AWS Secrets Manager
- Enable encryption at rest for etcd:

```
encryptionConfig:
  resources:
  - resources:
    - secrets
    providers:
    - aescbc:
        keys: [...]
```

## 🛠 Tools for Kubernetes Security

|Category|Tools|
|---|---|
|**RBAC auditing**|`rbac-lookup`, `rakkess`, `kubeaudit`|
|**Runtime defense**|Falco, Sysdig Secure, AppArmor, seccomp|
|**Static scanning**|kube-score, kube-linter, Polaris|
|**Policy enforcement**|OPA Gatekeeper, Kyverno, PodSecurityAdmission|
|**Benchmarking**|kube-bench (CIS), kube-hunter|

---

## 🧪 Threat Detection & Monitoring

- Enable **audit logging** on the API server
- Monitor kubelet activity and unauthorized execs
- Integrate logs into SIEM or EDR
- Use runtime anomaly detection (e.g., Falco rules)

---

## 🚨 Common Kubernetes Security Mistakes

|Misconfiguration|Risk|
|---|---|
|Unrestricted pod-to-pod traffic|Lateral movement|
|Containers running as root|Privilege escalation|
|Public dashboards or APIs exposed|External control plane takeover|
|Insecure image sources|Supply chain compromise|
|No resource limits|DoS / pod sprawl|

---

## 🧩 Related Topics

- [[Container Security]]
- [[Infrastructure as Code (IaC) Security]]
- [[DevSecOps]]
- [[Policy as Code (OPA & Kyverno)]]
- [[Runtime Threat Detection]]

---

## 🏷 Tags

#kubernetes #k8s #containers #rbac #networkpolicy #opa #kyverno #kubernetessecurity #devsecops #podsecurity #falco #etcd #supplychain