**Admission Controllers** are **Kubernetes control plane components** that **intercept requests to the API server** *after authentication and authorization* but *before the object is persisted*. They enforce **policies and validations** to maintain **security, consistency**, and **governance** within a Kubernetes cluster.

---

## 🎯 Purpose of Admission Controllers

- Enforce **security policies** (e.g., deny privileged containers)
- Validate **resource limits and labels**
- Inject **default configurations** (e.g., sidecars, labels)
- Mutate or reject incoming Kubernetes objects
- Enable **policy as code** frameworks (OPA, Kyverno)

---

## 🔁 Admission Controller Lifecycle

***Client Request*** 
**↓**  
***Authentication*** → ***Authorization***  
**↓**
📩 ***Admission Controllers*** (***Mutating*** → ***Validating***)  
**↓**
***ETCD Storage*** / ***Controller Manager***


---

## 🔧 Types of Admission Controllers

| Type              | Function                                | Notes                                |
|-------------------|-----------------------------------------|--------------------------------------|
| **Mutating**      | Modify requests (e.g., inject defaults) | Run first                            |
| **Validating**    | Accept or reject requests                | Run after mutation                   |
| **Dynamic Webhooks**| Call external webhooks to enforce logic | Used by OPA, Kyverno, custom policies|

---

## 🧱 Common Built-in Admission Controllers

| Controller Name              | Purpose                                              |
|------------------------------|------------------------------------------------------|
| `NamespaceLifecycle`         | Enforces namespace deletion rules                   |
| `LimitRanger`                | Enforces resource limits/requests                   |
| `ServiceAccount`             | Auto-generates service account tokens               |
| `NodeRestriction`            | Prevents node objects from tampering                |
| `PodSecurity` (PSA)          | Enforces pod-level security profiles (v1.23+)       |
| `TaintNodesByCondition`      | Ensures workloads honor node taints                 |
| `DefaultStorageClass`        | Assigns default storage class to PVCs               |

---

## 🔐 Security-Focused Admission Controllers

| Controller            | Function                                               |
|-----------------------|--------------------------------------------------------|
| `PodSecurity`         | Enforces `baseline`, `restricted`, or `privileged` profiles |
| `ImagePolicyWebhook`  | Blocks or allows images based on external validation   |
| `SecurityContextDeny` | Prevents dangerous security context settings (pre-PSA) |
| `OPA / Gatekeeper`    | Enforces Rego-based custom policy-as-code rules        |
| `Kyverno`             | Native YAML policies for validation, mutation, generation|

---

## 🧰 Policy-as-Code (PaC) with Admission Controllers

| Tool           | Language / Approach  | Example Use Cases                                 |
|----------------|----------------------|---------------------------------------------------|
| **OPA/Gatekeeper** | Rego (logic-based)   | Enforce labels, deny root containers, restrict images |
| **Kyverno**        | YAML (declarative)   | Block hostPath, inject default labels, validate resources |
| **K-Rail**         | Golang policies      | Hardcoded policy enforcement for small clusters    |

---

## 💡 Example: Deny Privileged Pods with Gatekeeper

```rego
package kubernetes.admission

violation[{"msg": msg}] {
  input.review.object.spec.containers[_].securityContext.privileged
  msg := "Privileged containers are not allowed"
}
```

## 📦 Managing Admission Controllers

- Most managed Kubernetes platforms (EKS, GKE, AKS) allow **dynamic webhook registration**
- For self-hosted clusters:
    - Add flags to kube-apiserver: `--enable-admission-plugins`
    - Register webhook configs: `MutatingWebhookConfiguration` / `ValidatingWebhookConfiguration`

---

## ⚠️ Best Practices

- ✅ Enable only required admission controllers
- 🔐 Protect webhook endpoints with TLS
- 🧪 Test admission policies before enforcing (`audit` → `enforce`)
- 🚫 Avoid wildcard permissions in webhook RBAC
- 🔁 Regularly review policies for relevance and scope

---

## 📎 Related Topics

- [[Pod Security Policies (PSPs)]]
- [[Policy as Code (OPA & Kyverno)]]
- [[Kubernetes Security]]
- [[Container Escape]]
- [[Runtime Threat Detection]]

---

## 🏷 Tags

#admissioncontrollers #kubernetes #opa #kyverno #policyascode #clustersecurity #Security+