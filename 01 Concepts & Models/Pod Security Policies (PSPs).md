**Pod Security Policies (PSPs)** were a Kubernetes feature used to **control the security context of pods**, defining **what a pod can or cannot do** when running in a cluster. PSPs allowed cluster administrators to enforce fine-grained restrictions on containers for **least privilege**, **sandboxing**, and **compliance**.

> 🛑 **Deprecated in Kubernetes v1.21** and **removed in v1.25+**. Replaced by alternatives like **OPA/Gatekeeper**, **Kyverno**, and **Pod Security Admission (PSA)**.

---

## 🎯 Purpose of PSPs

- Enforce **security best practices** for container workloads
- Prevent **privileged container escalation**
- Control **Linux capabilities**, volume types, and host access
- Apply **baseline**, **restricted**, or **custom policies**

---

## 🔐 Key PSP Controls

| Control                      | Description                                             |
|------------------------------|---------------------------------------------------------|
| `privileged`                 | Allow or deny privileged containers                     |
| `allowPrivilegeEscalation`   | Prevent containers from gaining more privileges         |
| `runAsUser`                  | Enforce user ID ranges (e.g., disallow UID 0)           |
| `readOnlyRootFilesystem`     | Enforce immutable root filesystem                       |
| `hostNetwork`, `hostPID`, `hostIPC` | Restrict access to host namespaces             |
| `volumes`                    | Restrict volume types (e.g., block `hostPath`)          |
| `seLinux`, `AppArmor`        | Require specific security profile enforcement           |
| `capabilities`               | Drop unneeded Linux capabilities                        |

---

## 🧰 PSP Example (YAML)

```yaml
apiVersion: policy/v1beta1
kind: PodSecurityPolicy
metadata:
  name: restricted-psp
spec:
  privileged: false
  allowPrivilegeEscalation: false
  runAsUser:
    rule: 'MustRunAsNonRoot'
  readOnlyRootFilesystem: true
  volumes:
    - 'configMap'
    - 'emptyDir'
    - 'secret'
  hostNetwork: false
  hostPID: false
  hostIPC: false
```

## 🧠 PSP Lifecycle in Kubernetes

|Version|Status|
|---|---|
|v1.10|Introduced|
|v1.21|Deprecated|
|v1.25+|Removed|

---

## 🚧 PSP Replacement Options

|Tool|Description|
|---|---|
|**Pod Security Admission (PSA)**|Built-in admission plugin since v1.23|
|**OPA / Gatekeeper**|Policy-as-code with Rego language|
|**Kyverno**|Kubernetes-native YAML-based policy engine|
|**K-Rail**|Lightweight real-time admission controller|

---

## 🔐 Pod Security Admission (PSA) Overview

- Enforces one of three **security profiles**:
    - 🔵 `privileged` (no restrictions)
    - 🟠 `baseline` (minimal restrictions)
    - 🔴 `restricted` (strict least privilege)
- Uses **namespace labels** to assign profiles:
```
kubectl label namespace prod pod-security.kubernetes.io/enforce=restricted
```

## 💡 Security Best Practices

- ✅ Disallow `privileged: true` containers
- ✅ Require `runAsNonRoot`
- ✅ Enforce `readOnlyRootFilesystem`
- ✅ Block `hostPath` and `hostNetwork` by default
- ✅ Drop all Linux capabilities unless explicitly needed
- 🔍 Audit cluster workloads for compliance

---

## 📎 Related Topics

- [[Kubernetes Security]]
- [[Container Escape]]
- [[Runtime Threat Detection]]
- [[Policy as Code (OPA & Kyverno)]]
- [[Cluster Admission Controllers]]

---

## 🏷 Tags

#kubernetes #podsecurity #psp #policyascode #opa #kyverno #containersecurity #Security+